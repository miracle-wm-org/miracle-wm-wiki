# Newcomer Corner
This document is intended for users who are unfamiliar with window managers, compositors, Wayland, or maybe even Linux in general. It serves as a high-level introduction to why this project exists as I don't expect everyone to be familiar.

We will build our understanding from the bottom to the top of the Linux graphics stack. We'll explore everything from the application layer to the kernel so that we can understand the flow of visual graphics from the application layer to your computer monitor.


## Key Takeways 

- Applications are written with the help pf **GUI Toolkits**, which abstract away common problems (e.g. text rendering, widgets, scale, keyboard & mouse input, etc)
- Applications talk to a **window manager** using the **Wayland** protocol
    - GUI toolkits implement the client side of this protocol
- Wayland is the succesor to **X11** protocol
- Window managers implement the Wayland protocol

## How do desktop applications work on Linux?
Imagine that we would like to build a "Todo list" desktop application for computers that are running the Linux operating system. We might want to build our application with the following features:

- A window on the user's desktop
- A button in this window to add a new item
- A modal that popus up when you click the "new item" button
    - This modal might contain a text input for entering the description of the todo item
- A list of added todo items, with each item containing:
    - Text describing the item
    - A checkbox describing the "done" state of the item
    - A button to delete the item
- And so on...

While this application seems simple, we quickly see that there a number of complicated UI widgets and interactions here (e.g. buttons, modals, dynamic lists, text, etc.). On top of that, we might want to have our application translated into a number of different languges, which means that we'll have to render proper fonts for all different types of languages (including left-to-right and right-to-left written languages). Managing all of this is a very difficult problem, especially when you just want to build your todo app.

This is where **GUI tookits** come into play. These toolkits handle the problems of rendering, widgets, animations, localization, mouse input, keyboard input, and much more for us. When we build our app on top of a toolkit, we're abstracting away a bunch of difficult bits that are better off left to a dedicated team.

!!! note
    Some of the toolkits on Linux that you may be familiar with are *GTK*, *QT*, *Flutter*, and *Electron*. There are many other toolkits, as well, but these ones are particularly popular.
    
## How do GUI toolkits work?
If you look around the screen that you're reading this webpage on, you probably see a number of other applications in addition to your computer browser. You might have a top panel displaying the date and time. You might have a dock showing you icons of the applications that you can open. You might have your favorite text editor like Visual Studio Code open. You might even have a todo app. Each of these application wants to render to the screen, receive mouse and keyboard input, and more. 

Linux orchestrates visual applications using a **window manager** (a.k.a a **display server** or **compositor**). Each application tells the window manager that it wants to render *something* to the screen. The window manager is then responsible for combining the images submitted by each application into one final image that is sent off to your screen. To facilitate this, applications speak a common protocol called **Wayland**. You may think of Wayland in the same way that you think of HTTP. Clients (applications) ask the Server (window manager) to perform some application (e.g. show something on the screen, become fullscreen, etc.). The window manager then has the authority to either accept or deny that request.

The window manager is primarily responsible for the following:

- Placing each application in an appropriate position on the screen
- Stitching together the images displayed by each application and sending the final image off to the screen(s)
- Routing keyboard, mouse, stylus and any other inputs to the proper application (e.g. the currently focused application)
- Maximizing and minimizing applications
- Dragging applications around on the screen
- Switching workspaces
- Alt-tabbing
- Exposing onscreen keyboards
- Handling session locking
- And much, much more


!!! note
    You are probably most familiar with "floating" window managers. These window managers are typical of a baseline "Windows 10" user experience. However, this is not the only way to manage your windows! `miracle-wm` is a tiling window manager, meaning that it treats windows as individual tiles instead of surfaces that are floating in a pool.
    

GUI toolkits abstract the Wayland protocol away from application developers so that they don't have to worry about it. The protocol itself is quite complicated so it is a good thing that they do this. You as an application developer _can_ choose to not use a GUI toolkit and implement the client-side of the Wayland protocol yourself, but this would be incredibly time-consuming. On top of that, you would have to implement all of these previously mentioned aspecs of a GUI toolkit (e.g. widgets, input, animations, text rendering etc.). Needless to say, unless you plan to make it your full-time job (or you're a dedicated hobbyist!) it probably isn't worth your time.

### The history of Wayland
Unfortunately, I doesn't feel right to tell you about Wayland if I don't also provide a quick aside to inform you about its predecessor: **X11**. I won't get into the nitty-gritty details here (as I never developed this protocol myself) but I will explain enough to clear up some confusion. 

For most of its history, Linux applications used the **X11** protocol to render instead of Wayland.. The X ecosystem is much different compared to the Wayland, and I'm afraid it has led to a bit of confusion among people trying to understand Linux applications for the first time. For starters, there existed only one true implementation of X11 on Linux. This was known as the **XOrg Server**. All Linux distributions ran a similar XOrg server underneath the hood. This was known as the "compositor" because it was responsible for "compositing" the final image and sending it off to the displays. The "compositor" was only responsible for compositing however. A separate process usually existed to facilitate the window management aspects of the compositors, which was fittingly called the **window manager**. By "window management aspects", I am refering to featrues such as:

- Placing new windows
- Allowing windows to be dragged around (or not)
- Moving windows based off keyboard input
- Fullscreening windows
- etc.

Hence, if you ever installed the i3 window manager (as an example), you were installing a *window manager* while the XOrg server remained your *compositor*. This is why you will see the terms "window manager" and "compositor" used interchangeably when descibing a Wayland window manager. In the Wayland world, these are no longer two distinct processes like they were before.

Fast forward to some time in the early 2010s, the XOrg developers finally had enough of X11. The entire ecosystem had a lot of cruft and a lot of hacks. On top of that, the security that X11 provided was minimal at best. The X developers figured that it would be much easier to redesign a new protocol from the ground-up. That is when Wayland was born! Unlike X11 whose only real implementation was the XOrg server, Wayland was designed to just be a set of protocol definitions. This means that *anyone* can write their own Wayland server so long as they implement the protocols correctly.

That is as deep as I will go into the history of Wayland. It is obviously much deeper than this and I wasn't around during that time so I can't speak to the specifics. If you ever want to seek out an ex-X11 developer at an XDC conference, I'm sure that they have many horror stories to tell you.

Let's get back to the graphics stack now!


## How do window managers work
Window managers (or "compositors") implement the Wayland protocol. These 

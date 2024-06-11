# miracle-wm-wiki
This repository contains documentation for [miracle-wm](https://github.com/mattkae/miracle-wm).
There will be a no release of this documentation every time that `miracle-wm` has a release.

The docs can be found at: https://mattkae.github.io/miracle-wm-wiki/latest/.

## Setup
```sh
python -m venv venv
pip install -r requirements.txt
```

## Testing
```sh
mkdocs serve
```

Then navigate to `localhost:8000`

## Releasing
- Simply tag a new release as `vX.Y.Z`
- CI will handle publishing the the latest version
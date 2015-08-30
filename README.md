     _________
    |__  / ___|  ___ _ __ ___  ___ _ __
      / /\___ \ / __| '__/ _ \/ _ \ '_ \
     / /_ ___) | (__| | |  __/  __/ | | |
    /____|____/ \___|_|  \___|\___|_| |_|


# Scrot and Imgur/S3 zenity GUI

ZScreen is a simple zenity GUI for _scrot_. It has three modes:

1. Select an area with mouse
2. Immediate screenshot on the entire screen screen
3. Screenshot on the entire screen with configurable delay

You can also select to upload the screenshot to _Amazon S3_ or _imgur_.
After uploading successfully it will automatically open in your browser and
appear in your X selection clipboard.

The deletion links for uploads are stored in `~/.zscreen/deleteURL.txt`.

## Configuration

Configuration for ZScreen is stored in the shell variables defined in the file
`$XDG_CONFIG_HOME/zscreen/config.sh`.

Sample configuration file:

```bash
# Which directory to put screenshots. Default is $HOME/Screenshots.
export ZSCREEN_SCREENSHOT_DIR="$HOME/media/images/screenshots"
# Fileformat to use. Default is '%Y-%m-%d--%s_$wx$h_scrot.png'
export ZSCREEN_FILEFMT='screenshot_%Y-%m-%d-%H%M%S_$wx$h.png'
# Always upload the screenshot? Default is false.
export ZSCREEN_ALWAYS_UPLOAD="true"
# Set upload provider. the value should either be zs3upload or zimgur.
export ZSCREEN_UPLOAD_CMD="zs3upload"
export ZSCREEN_S3_BUCKET="zscreen-bucket"
```

## Issues

Please report bugs to Christian Zucchelli <thewebcha@gmail.com>
or use the GitHub issue tracker.

## Dependencies

* `scrot`
* `zenity`
* `s3cmd`
* `sed`, `bash`

## Authors

* Christian Zucchelli (@Chris_Zeta) <thewebcha@gmail.com>
  * ZScreen Developer (2012.09.02)
  * Twitter: https://twitter.com/#!/Chris_Zeta
  * GitHub: https://github.com/ChrisZeta

* Bart Nagel <bart@tremby.net>
  * imgur Developer

* Erik Westrup <erik.westrup@gmail.com>
  * GitHub: https://github.com/erikw

* Hiroshi Fukada <hiroshi@fukada.us>
  * Stupid Simple S3 Uploader
  * GitHub: https://github.com/hfukada

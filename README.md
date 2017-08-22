# [bumpy]
Generate [adult swim]-style bumps.

Required: `moviepy ffmpeg imagemagick`  
Quick guide:

Create a file test.yml:
```yaml
bump:
# list of captions here (quoted)
# use \n to line-break
    - "Hi."
    - "How's it going there?"
    - "This is a test for [bumpy]"
    - "Edit me pls"
    - "yeah, dass it"

options:
# insert options here, with the caption number first
# available options:
  # duration (seconds)
  # size (default: 42)
  # color (default: "white")
  # bg_color (default: "black")
  # align (default: "center")
  # font (default: "HelveticaNeueCond-Bold")
        1:
            duration: 1.5
        4:
            color: "red"
        5:
            size: 24

audio:
# audio file
    file: "music.mp3"
# where to start playing (seconds)
    subclip: 20.1
```

Then generate the bump:  
`./bumpy test.yml test.mp4`  
or preview it:  
`./bumpy -p test.yml test.mp4`  

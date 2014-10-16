#figlet4go
     _______  __    _______  __       _______ .___________. _  _      _______   ______
    |   ____||  |  /  _____||  |     |   ____||           || || |    /  _____| /  __  \
    |  |__   |  | |  |  __  |  |     |  |__   `---|  |----`| || |_  |  |  __  |  |  |  |
    |   __|  |  | |  | |_ | |  |     |   __|      |  |     |__   _| |  | |_ | |  |  |  |
    |  |     |  | |  |__| | |  `----.|  |____     |  |        | |   |  |__| | |  `--'  |
    |__|     |__|  \______| |_______||_______|    |__|        |_|    \______|  \______/

A port of [figlet](http://www.figlet.org/) to golang.  
Make it easier to use,add some new feature such as colorized outputs.

##Usage

###Install
    go get -u github.com/getwe/figlet4go

###Demo
```go
package main

import (
	"fmt"
	"github.com/fatih/color"
	"github.com/getwe/figlet4go"
)

func main() {
	str := "golang"
	ascii := figlet4go.NewAsciiRender()
	// most simple Usage
	renderStr, _ := ascii.Render(str)
	fmt.Println(renderStr)

	// change the font color
	options := figlet4go.NewRenderOptions()
	options.FontColor = make([]color.Attribute, len(str))
	options.FontColor[0] = color.FgMagenta
	options.FontColor[1] = color.FgYellow
	options.FontColor[2] = color.FgBlue
	options.FontColor[3] = color.FgCyan
	options.FontColor[4] = color.FgRed
	options.FontColor[5] = color.FgWhite
	renderStr, _ = ascii.RenderOpts(str, options)
	fmt.Println(renderStr)

	// change the font
	options.FontName = "larry3d"
	// except the default font,others need to be load from disk
	// here is the font :
	// ftp://ftp.figlet.org/pub/figlet/fonts/contributed.tar.gz
	// ftp://ftp.figlet.org/pub/figlet/fonts/international.tar.gz
	// download and extract to the disk,then specify the file path to load
	ascii.LoadFont("/usr/local/Cellar/figlet/2.2.5/share/figlet/fonts/")

	renderStr, _ = ascii.RenderOpts(str, options)
	fmt.Println(renderStr)

}
```

![screenshot](./screenshot/demo1.jpg)
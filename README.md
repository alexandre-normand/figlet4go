[![Build Status](https://travis-ci.org/alexandre-normand/figlet4go.svg)](https://travis-ci.org/alexandre-normand/figlet4go)

# figlet4go
     _______  __    _______  __       _______ .___________. _  _      _______   ______
    |   ____||  |  /  _____||  |     |   ____||           || || |    /  _____| /  __  \
    |  |__   |  | |  |  __  |  |     |  |__   `---|  |----`| || |_  |  |  __  |  |  |  |
    |   __|  |  | |  | |_ | |  |     |   __|      |  |     |__   _| |  | |_ | |  |  |  |
    |  |     |  | |  |__| | |  `----.|  |____     |  |        | |   |  |__| | |  `--'  |
    |__|     |__|  \______| |_______||_______|    |__|        |_|    \______|  \______/

_This is a fork of the original project from [getwe](https://github.com/getwe) but since 
there wasn't any activity in a while, managing the fork seemed more sensible than opening a PR and waiting, and waiting.
The changes here are meant to make it closer to go conventions and mainly, provide more visibility to the caller
as far as custom font loading (instead of silently falling back to `default`). I'll happily review and merge PRs, too._

A port of [figlet](http://www.figlet.org/) to golang.  
Make it easier to use,add some new feature such as colorized outputs.

## Usage


### Install

```
go get -u github.com/getwe/figlet4go
```

### Demo

```
cd demo/
go build
./demo -str="golang"
#Maybe you have to `brew install figlet` if you need 3D fond in mac osx.
```

see details in `demo/demo.go` .

![screenshot](./screenshot/demo1.jpg)

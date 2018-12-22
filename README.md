spouttest
=========

A Go test program for the github.com/nosuchtim/spout package.
Assuming that mingw-w64 has been installed, the commands below will
get and build everything necessary to run the spouttest program.

This only works on Windows, currently.

```
go get github.com/leadedge/Spout2
# Ignore the message that says: can't load package: ... no Go files...
go get github.com/nosuchtim/spout
cd $(GOPATH)/src/github.com/nosuchtim/spout
makeandinstall.bat
go get github.com/nosuchtim/spouttest
cd $(GOPATH)/src/github.com/nosuchtim/spouttest
go build
spouttest.exe
```
After running spouttest.go, you should see a window with a spinning cube.  If you run github.com/leadedge/Spout2/DEMO/SpoutReceiver, you should see two textures named "gosquare" and "goscreen".

If you want to distribute spouttest.exe to a machine that doesn't have mingw-64 installed, you need to include these 3 DLLs from mingw-64:

	libgcc_s_sjlj-1.dll
	libstdc++-6.dll
	libwinpthread-1.dll
 

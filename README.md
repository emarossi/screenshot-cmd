# screenshot-cmd
Simple command-line tool for making screenshots (for Windows Vista or later)

Fork from https://github.com/chuntaro/screenshot-cmd

Made some changes to compile with MinGW32, a bit more messy (as I couldn't be bothered to get wchar_t and unicode right).
Also need to include libdwmapi.a and headers, for some reason is missing in MinGW32.

To build:
> g++ -Wall -Os -mwindows -m32 screenshot.cpp -lgdiplus -lDwmapi -o screenshot -static

To run:
> screenshot.exe -wh 1e9060a -o screenshot.png

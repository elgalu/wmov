wmov
====

A command line utility to switch virtual desktops and move windows between virtual desktops. Based on wmctrl.


# wmov - switch workspace in ubuntu 12.10
#

#
# SOME CONTEXT
#
# Ubuntu 12.10 represents the different workspace as chuncks of a very large
# virtual screen. Instead of using the standard "desktop" concept used by
# wmctrl, Unity switches desktop by changing the coordinates of the viewport.
#
# If you have 4 workspace arranged in a square (which is the default, you need
# some kind of settings tweaker to change that), this means that:
#
# - 0,0                 is the top left corner of the top left workspace (1)
# - <width>,0           is the top left corner of the top right workspace (2)
# - 0,<height>          is the top left corner of the bottom left workspace (3)
# - <width>,<height>    is the top left corner of the bottom right workspace (4)
#
# Where <width>x<height> is the resolution of your (physical) screen.
#
# USAGE
#
# wmov <num>
#
#   Switch to the designated desktop. The workspaces are numbered from left to
#   right, then from top to bottom, starting at 1.
#
# wmov left|right|up|down|here
#
#   Switch to the desktop in the indicated direction, if any.
#
# wmov mov <title> <num>
#
#   Moves a window whose title contains the substring <title> (case insensitive)
#   to the desktop designated by <num>.nn
#
# wmov mov <title> left|right|up|down|here
#
#   Moves a window whose title contains the substring <title> (case insensitive)
#   to the desktop in the indicated direction, if any.

# dosfstools on OSX

OSX 10.9 Maveric not exist mkfs.vfat.
 
[dosfstools](http://daniel-baumann.ch/software/dosfstools/) - now orphaned Linux version utilities for making and checking MS-DOS FAT filesystems.

OSX users using diskfstool? hdutil and hdiutil.

**Problems**

1. Not worked *ioctl(dev, HDIO_GETGEO, &geometry)* unable to get drive geometry
2. geometry.sectors and geometry.heads you may get from nondirect calculation (sample in the [diskdev-cmds] (http://www.opensource.apple.com/source/diskdev_cmds/diskdev_cmds-557.3.1/)), but geometry.start needed for set hidden_sectros not available

**Porting**

1. Based on last version dosfstools 3.0.26
2. Add some linux headers
3. Remove atari support
4. Remove fatlabel utility
5. mkfs.fat not worked on real drives - only with images -C option and loop devices

**Install with homebrew**

    $brew create https://github.com/sv99/dosfstools-osx.git

```ruby
require "formula"

class Dosfstools < Formula
  homepage ""
  url "https://github.com/sv99/dosfstools-osx.git"
  sha1 ""

  def install
    system "make", "install"   
  end

end
```

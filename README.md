# About foo-Wallpaper-Feh-Gif (Glitching fixed)
This is just a loop script that sets a gif as a wallpaper. Supports transparency. Requires feh or xload or [xwallpaper](https://github.com/stoeckmann/xwallpaper)(uses less cpu).

It's **duplicate wallpaper fixed version** of [foo-Wallpaper-Feh-Gif](https://github.com/thomas10-10/foo-Wallpaper-Feh-Gif). For example, If you are using **i3wm** and you open your gif wallpaper with "exec_always", and for some reason you have opened it two or more times, your wallpaper will be glitching.

**! INCREASES CPU use**

<img src="https://github.com/thomas10-10/foo-Wallpaper-Feh-Gif/raw/master/desktop-animation2.gif"  />
<img src="https://github.com/thomas10-10/foo-Wallpaper-Feh-Gif/raw/master/desktop-animation4.gif"  />

# To run it
Download back4.sh and place your desired gif in the `gif` directory.
For ubuntu/xfce set prog=$select4 in run_wallpaper , You can set stretched style in desktop panel.

```
cd ~
chmod +x run_wallpaper
./run_wallpaper 0.010 gif/name.gif &
#./run_wallpaper speed pathToGif &
```

# select between feh,xload,xwallpaper,ubuntu-xfce
edit back4.sh, set prog=$select2 for xwallpaper, or select4 for ubuntu-xfce

# autostart with i3, in i3 config :

```
exec_always --no-startup-id killall run_wallpaper 
exec_always --no-startup-id $HOME/run_wallpaper 0.03 Downloads/beautycity.gif
```

# To stop it
```
killall run_wallpaper
```

# Alternatively

You can add the speed as a suffix to your desired gif.

```
ls gif/name.gif-0.010
./run_wallpaper gif/name.gif-0.010 &
```


# To clean cache
 ```
rm -rf /tmp/back4
```

I search a lighter alternative than feh in cpu ress




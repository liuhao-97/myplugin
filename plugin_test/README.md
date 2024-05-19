This is an simple example to generate element plugin for gstreamer 1.14.



1. First use gst-plugin-bad to generate an element plugin.
```
git clone https://github.com/GStreamer/gst-plugins-bad.git
git checkout 1.14
cd gst-plugins-bad/tools
./gst-project-maker myfilter videofilter
```

2. build the plugin
```
make
sudo make install
```

3. Test plugin
```
gst-inspect-1.0 myfilter
```



Ref.
1. https://gstreamer.freedesktop.org/documentation/plugin-development/basics/boiler.html?gi-language=python
2. https://developer.ridgerun.com/wiki/index.php/Creating_a_New_GStreamer_Element_or_Application_Using_Templates
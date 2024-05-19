PLUGIN_NAME = myfilter

SRC = gstmyfilter.c

# Include video library flags
CFLAGS += -Wall $(shell pkg-config --cflags gstreamer-1.0 gstreamer-base-1.0 gstreamer-video-1.0)
LDFLAGS += $(shell pkg-config --libs gstreamer-1.0 gstreamer-base-1.0 gstreamer-video-1.0)


all: $(PLUGIN_NAME).so

$(PLUGIN_NAME).so: $(SRC)
	$(CC) -shared -fPIC -o $@ $^ $(CFLAGS) $(LDFLAGS)

clean:
	rm -f *.o *.so

install: all
	install -m 755 $(PLUGIN_NAME).so $(DESTDIR)/usr/lib/aarch64-linux-gnu/gstreamer-1.0


depend:
	sudo apt-get install gstreamer1.0-tools gstreamer1.0-doc libgstreamer1.0-0 libgstreamer1.0-dev graphviz
	sudo apt-get install gstreamer1.0-plugins-base gstreamer1.0-plugins-base-apps gstreamer1.0-plugins-base-doc
	sudo apt-get install gstreamer1.0-plugins-good gstreamer1.0-plugins-good-doc
	sudo apt-get install gstreamer1.0-plugins-ugly gstreamer1.0-plugins-ugly-doc
	sudo apt-get install gstreamer1.0-plugins-bad  gstreamer1.0-plugins-bad-doc
	sudo apt-get install libgstreamer1.0-dev
	sudo apt-get install libgstreamermm-1.0-0v5 libgstreamermm-1.0-dev libgstreamermm-1.0-doc
	sudo apt-get install python-gst-1.0 python3-gst-1.0 python-audioread

exemple-gst-c:depend
	gcc exemple-gst-c.c -o exemple-gst-c `pkg-config --cflags --libs gstreamer-1.0`
	chmod a+x exemple-gst-c
	file exemple-gst-c

exemple-gst-cpp:depend
	g++ exemple-gst-cpp.cpp -o exemple-gst-cpp `pkg-config --cflags --libs gstreamermm-1.0`
	chmod a+x exemple-gst-cpp
	file exemple-gst-cpp

exemple-gst-python:
	chmod a+x exemple-gst-python.py

all: exemple-c exemple-cpp exemple-python

clean:
	rm -f exemple-gst-c
	rm -f exemple-gst-cpp

run-c:exemple-gst-c
	./exemple-gst-c

run-cpp:exemple-gst-cpp
	./exemple-gst-cpp

run-python:exemple-gst-python
	./exemple-gst-python.py

.PHONY: clean all


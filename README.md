# GST-plugin

Set up

```
podman run -ti --privileged --net=host -v `pwd`:/work docker.io/jweng1/gst-python:v1

git clone https://github.com/Streaming-multiple-video-sources-Edge/GST-plugin.git

cd work
cd GST-plugin

python3 -m venv venv
source venv/bin/activate

pip install -U wheel pip setuptools
pip install -r requirements.txt

```


Export plugin

```
export GST_PLUGIN_PATH=$GST_PLUGIN_PATH:$PWD/venv/lib/gstreamer-1.0/:$PWD/gst/ 
gst-inspect-1.0 python

```



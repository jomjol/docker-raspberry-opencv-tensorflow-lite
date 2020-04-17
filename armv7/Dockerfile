FROM jomjol/raspberry-opencv

RUN [ "cross-build-start" ]

WORKDIR /

COPY wheels ./wheels
RUN pip3 install --no-cache-dir ./wheels/tflite_runtime-2.1.0.post1-cp37-cp37m-linux_armv7l
RUN pip3 install --no-cache-dir ./wheels/Pillow-6.2.0-cp37-cp37m-linux_armv7l.whl
RUN pip3 install --no-cache-dir ./wheels/numpy-1.17.4-cp37-cp37m-linux_armv7l.whl

COPY . ./

RUN [ "cross-build-end" ]
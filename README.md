# OpenCV Installer Document for C++

The documentation tested on Kubuntu 19.04 and Lubuntu 18.04.3 LTS.
First of all you need to OpenCV files, you can download last version next step
```
git clone https://github.com/opencv/opencv.git
git clone https://github.com/opencv/opencv_contrib.git
git clone https://github.com/opencv/opencv_extra.git
```
or you can use on the repo files.

Always, you should install to /opt directory, because you can see every details your installation. Well we can continue...
```
sudo mkdir /opt/opencv
sudo mkdir /opt/files
sudo chown -R USERNAME:USERNAME /opt/opencv
sudo chown -R USERNAME:USERNAME /opt/files
mv opencv /opt/files/opencv/
mv opencv_contrib /opt/files/opencv/
mv opencv_extra /opt/files/opencv/
```
Just we create the opencv folder for library and create files for opencv installer files.
```
cd /opt/files/opencv
mkdir release
```
#### Required Install
```
[required] sudo apt-get update
[compiler] sudo apt-get install build-essential
[required] sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
[required] sudo apt install cmake libtbb2 ffmpeg libgtk2.0-dev libavformat-dev libswscale-dev libtbb-dev libjpeg-dev libpng-dev libtiff-dev libdc1394-22-dev
```
If you on **/opt/files/opencv/opencv/release** directory and complated all install, you can make **cmake** files. Follow the text..
```
cmake -DCMAKE_BUILD_TYPE=RELEASE -DCMAKE_INSTALL_PREFIX=/opt/opencv –DOPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules ..
```
You can see output and than complated started install.
```
make -j4
make install
```


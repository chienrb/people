People
======
Algorithms related to detecting and tracking people using various robot sensors.

## Documentation
[http://ros.org/wiki/people](http://ros.org/wiki/people)

## Install Opencv-4.6 from source
```
cd && mkdir opencv && cd opencv

# Install minimal prerequisites (Ubuntu 18.04 as reference)
sudo apt update && sudo apt install -y cmake g++ wget unzip

# Download and unpack sources
wget -O opencv.zip https://github.com/opencv/opencv/archive/4.x.zip
wget -O opencv_contrib.zip https://github.com/opencv/opencv_contrib/archive/4.x.zip
unzip opencv.zip
unzip opencv_contrib.zip

# Create build directory and switch into it
mkdir -p build && cd build

# Configure
cmake -DOPENCV_EXTRA_MODULES_PATH=../opencv_contrib-4.x/modules ../opencv-4.x

# Build
cmake --build .

# make
sudo make install
```

The header files are now locate at ```/usr/local/include/opencv4/opencv2```

Create symlink for opencv

```
cd /usr/local/include && sudo ln -s opencv4/opencv2 opencv2
```

## Installation

Create workspace
```
mkdir -p <catkin-workspace>/src && cd <catkin-workspace> && catkin_make
```

Clone this repository
```
cd src && git clone https://github.com/chienrb/people.git
```

Make
```
cd .. && catkin_make
```

## build on Microsoft Windows with visual studio vc14 2015:

- Edit `win_make_vc14_x64_to_edit.bat` and modify : 
    - QT5_DIR="/path/to/Qt/msvcXXX/lib/cmake"
	- CMAKE_PREFIX_PATH="/path/to/OpenCV/build" the directory that points to the `OpenCVConfig.cmake` file
- Run bat file.

## build and run on linux :

On ubuntu, PixelAnnotationTool need this pacakage (OpenCV and Qt5.9.1): 

```sh
sudo apt-get install mesa-common-dev
sudo apt-get install libopencv-dev python-opencv

```
Ensure you have QT5 installed and get the install path with:

```sh
qmake --version
```

To compile the application : 

```sh
cd ..
mkdir x64
cd x64
cmake -DQT5_DIR=/path/to/Qt5.9.1/5.9.1/gcc_64/lib/cmake -G "Unix Makefiles" ..
make

```

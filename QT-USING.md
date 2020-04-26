# OpenCV using QT/C++
## Add Pro File
Qt using qmake and qmake using `.pro` file format for require parameters. `.pro` file is generally file. So you need to that when you at any OS, platforms, etc. 

```
INCLUDEPATH += "/opt/opencv/include/opencv4"

LIBS += \
    -L/opt/opencv/lib \
    -lopencv_highgui \
    -lopencv_core \
    -lopencv_imgproc \
    -lopencv_imgcodecs \
    -lopencv_videoio
```

then you should import to project library files.

```
#include "opencv2/core/core.hpp"
#include "opencv2/highgui/highgui.hpp"
```
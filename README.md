Darknet for YOLOv3 
Available add-on like screenshot, beep function and GPS Overlay

Screenshot function placed in line 308 of image.c:
    
    system("scrot -e 'mv $f ~/darknet/screenshot'");

Beep function placed in line 309 of image.c:
    
    fprintf(stdout, "\aBeep!\n" );

GPS Overlay placed in line 106 to 109 of image_opencv.cpp:
    
    std::string GPS;
    ifstream FileGPS("GPS.txt");
    FileGPS >> GPS;
    putText(m, GPS, Point(0, 470), FONT_HERSHEY_SIMPLEX, 0.4, CV_RGB(199, 21, 133), 0.1);

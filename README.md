# DSVSCA-Core

## Compile

In the root directory, run the following command:

> make

or

> make debug

The program and all dependencies should automatically build and compile. All build objects output to the build folder.

The make process produces 3 main files: libDSVSCA.a, libDSVSCA.so, and DSVSCA. Both libDSVSCA.a and libDSVSCA.so are the static and shared DSVSCA libraries that can be linked into other programs. These two libraries can be found in the build folder after compilation. Note that you only need to use one of the libraries for DSVSCA to work since they are the same library but compiled differently.

## Running DSVSCA

DSVSCA is a command line program compiled in the example folder and allows for easy use of DSVSCA using the parameters below. Also available in the example folder is the Java DSVSCA GUI. It can be run using ```java -jar DSVSCA.jar``` or double clicking on DSVSCA.jar.

```
Mandatory arguments:
-v, --video=VIDEO-FILE          Specifies the location of the video file to virtualize.
-s, --sofa=SOFA-FILE            Specifies the location of the SOFA file to use during the virtualization process.

Optional arguments:
-h, --help                      Prints out the help menu specifying all required and optional parameters.
-b, --block-size=BLOCK-SIZE     Specifies the block size used when processing the audio. A smaller block size results in better virtualization but takes longer to process. The default size is 256.
-c, --coord-type=TYPE           Specifies the coordinate system used when specifying virtualized speaker placement. The values can be Cartesian or Spherical. The default value used is Cartesian.
-fl, --fl=X,Y,Z                 Specifies the x, y, and z or phi, theta, and radius coordinates of the front left speaker. If this value is not specified, the default value of 1, 1, 0 is used.
-fc, --fc=X,Y,Z                 Specifies the x, y, and z or phi, theta, and radius coordinates of the front center speaker. If this value is not specified, the default value of 1, 0, 0 is used.
-fr, --fr=X,Y,Z                 Specifies the x, y, and z or phi, theta, and radius coordinates of the front right speaker. If this value is not specified, the default value of 1, -1, 0 is used.
-bl, --bl=X,Y,Z                 Specifies the x, y, and z or phi, theta, and radius coordinates of the back left speaker. If this value is not specified, the default value of -1, 1, 0 is used.
-br, --br=X,Y,Z                 Specifies the x, y, and z or phi, theta, and radius coordinates of the back right speaker. If this value is not specified, the default value of -1, -1, 0 is used.
-lfe, --lfe=X,Y,Z               Specifies the x, y, and z or phi, theta, and radius coordinates of the Low-Frequency Efects (subwoofer) speaker. If this value is not specified, the default value of 1, 0, 0 is used.
```


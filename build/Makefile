LIBS:=-lavfilter -pthread -lswscale -lavformat -lavcodec -lswresample -ldl -lm -lavutil -lFFTConvolver -lmysofa -lz

default:
	ar rcs libDSVSCA.a *.o
	g++ -L./ -shared -o libDSVSCA.so *.o -Wl,--whole-archive -lFFTConvolver -lmysofa -Wl,--no-whole-archive
	jar -cfve DSVSCA.jar DSVSCA *.class *.fxml ./dsvsca/*

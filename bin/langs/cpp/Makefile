FLAGSFILE=temp/flags.dat
CFLAGS=$(shell cat ${FLAGSFILE})

temp/prog.out: temp/prog.cpp ${FLAGSFILE}
	${CXX} $< -o $@ $(CXXFLAGS)

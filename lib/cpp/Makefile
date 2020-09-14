FLAGSFILE=temp/flags.dat
CXXFLAGS=$(shell cat ${FLAGSFILE})

temp/prog.out: temp/prog.cpp ${FLAGSFILE}
	${CXX} $< -o $@ $(CXXFLAGS)

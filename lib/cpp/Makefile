FLAGSFILE=temp/flags.dat
SOURCEFILE=$(shell ./src)
CXXFLAGS=$(shell cat ${FLAGSFILE})

temp/prog.out: ${SOURCEFILE} ${FLAGSFILE}
	${CXX} $< -o $@ $(CXXFLAGS)

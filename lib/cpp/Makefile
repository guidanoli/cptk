FLAGSFILE=temp/flags.dat
SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)
CXXFLAGS=$(shell cat ${FLAGSFILE})

${BINFILE}: ${SOURCEFILE} ${FLAGSFILE}
	${CXX} $< -o $@ $(CXXFLAGS)

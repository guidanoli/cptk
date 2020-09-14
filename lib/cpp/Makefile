FLAGSFILE=temp/flags.dat
SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)
CXXFLAGS=$(shell cat ${FLAGSFILE})

.PHONY: run

run: ${BINFILE}
	"$<"

${BINFILE}: ${SOURCEFILE} ${FLAGSFILE}
	${CXX} "$<" -o "$@" $(CXXFLAGS)

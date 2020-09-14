FLAGSFILE=temp/flags.dat
SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)
CSFLAGS=$(shell cat ${FLAGSFILE})

${BINFILE}: ${SOURCEFILE} ${FLAGSFILE}
	mcs -out:$@ $< $(CSFLAGS)

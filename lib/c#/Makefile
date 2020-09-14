FLAGSFILE=temp/flags.dat
SOURCEFILE=$(shell ./src)
CSFLAGS=$(shell cat ${FLAGSFILE})

temp/prog.out: ${SOURCEFILE} ${FLAGSFILE}
	mcs -out:$@ $< $(CSFLAGS)

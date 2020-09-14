FLAGSFILE=temp/flags.dat
SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)
CFLAGS=$(shell cat ${FLAGSFILE})

${BINFILE}: ${SOURCEFILE} ${FLAGSFILE}
	${CC} $< -o $@ $(CFLAGS)

FLAGSFILE=temp/flags.dat
SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)
CFLAGS=$(shell cat ${FLAGSFILE})

.PHONY: run

run: ${BINFILE}
	"$<"

${BINFILE}: ${SOURCEFILE} ${FLAGSFILE}
	${CC} "$<" -o "$@" $(CFLAGS)

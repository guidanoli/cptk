SOURCEFILE=$(shell ./path)
BINFILE=$(addsuffix .out, $(basename ${SOURCEFILE}))

.PHONY: run debug

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb --args mono --debug "$<"

${BINFILE}: ${SOURCEFILE}
	mcs -out:"$@" "$<" ${CSFLAGS}

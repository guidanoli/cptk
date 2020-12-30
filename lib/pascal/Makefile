SOURCEFILE=$(shell ./path)
BINFILE=$(basename ${SOURCEFILE})

.PHONY: run debug

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb "$<"

${BINFILE}: ${SOURCEFILE}
	fpc "$<" $FLAGS 2>&1 | grep -v 'contains output sections'

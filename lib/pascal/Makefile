SOURCEFILE=$(shell ./src)
BINFILE=$(basename ${SOURCEFILE})

.PHONY: run rund

run: ${BINFILE}
	"$<"

rund: ${BINFILE}
	gdb "$<"

${BINFILE}: ${SOURCEFILE}
	fpc "$<" 2>1 | grep -v 'contains output sections'

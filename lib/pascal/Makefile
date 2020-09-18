SOURCEFILE=$(shell ./src)
BINFILE=$(basename ${SOURCEFILE})

.PHONY: run

run: ${BINFILE}
	"$<"

${BINFILE}: ${SOURCEFILE}
	fpc "$<" 2>1 | grep -v 'contains output sections'

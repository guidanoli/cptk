SOURCEFILE=${tempdir}/prog.pas
BINFILE=$(basename ${SOURCEFILE})

.PHONY: path run debug

path:
	echo "${SOURCEFILE}"

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb "$<"

${BINFILE}: ${SOURCEFILE}
	fpc "$<" 2>&1 | grep -v 'contains output sections'

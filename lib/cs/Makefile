SOURCEFILE=$(addprefix ${WD}/, $(shell ./path))
BINFILE=$(basename ${SOURCEFILE})

.PHONY: run debug

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb --args mono --debug "$<"

${BINFILE}: ${SOURCEFILE}
	mcs ${FLAGS} -debug -out:"$@" "$<"

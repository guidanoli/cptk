SOURCEFILE=$(addprefix ${WD}/, $(shell ./path))
BINFILE=$(addsuffix .kexe, $(basename ${SOURCEFILE}))

.PHONY: run

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb "$<"

${BINFILE}: ${SOURCEFILE}
	konanc ${FLAGS} -g "$<" -o "$(basename $@)"

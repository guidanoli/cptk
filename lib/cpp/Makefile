SOURCEFILE=$(shell ./path)
BINFILE=$(addsuffix .out, $(basename ${SOURCEFILE}))

.PHONY: run debug

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb "$<"

${BINFILE}: ${SOURCEFILE}
	g++ "$<" $FLAGS -g -o "$@" -lm

SOURCEFILE=$(shell ./path)
BINFILE=$(basename ${SOURCEFILE})

.PHONY: run debug

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb "$<"

${BINFILE}: ${SOURCEFILE}
	ghc "$<" -g ${HASKELLFLAGS}

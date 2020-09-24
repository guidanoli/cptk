SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)

.PHONY: run

run: ${BINFILE}
	"./$<"

${BINFILE}: ${SOURCEFILE}
	ghc "$<"

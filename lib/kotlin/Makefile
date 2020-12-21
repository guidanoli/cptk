SOURCEFILE=$(shell ./path)
BINFILE=$(shell ./xpath)

.PHONY: run

run: ${BINFILE}
	java -jar "$<"

${BINFILE}: ${SOURCEFILE}
	kotlinc "$<" -include-runtime -d "$@"

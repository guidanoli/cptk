SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)

.PHONY: run

run: ${BINFILE}
	java -jar "$<"

${BINFILE}: ${SOURCEFILE}
	kotlinc "$<" -include-runtime -d "$@"

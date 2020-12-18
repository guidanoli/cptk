SOURCEFILE=temp/$(shell ./path)
BINFILE=temp/$(shell ./xpath)

.PHONY: run

run: ${BINFILE}
	java -jar "$<"

${BINFILE}: ${SOURCEFILE}
	kotlinc "$<" -include-runtime -d "$@"

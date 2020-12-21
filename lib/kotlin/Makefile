SOURCEFILE=$(shell ./path)
BINFILE=$(addsuffix .jar, $(basename ${SOURCEFILE}))

.PHONY: run

run: ${BINFILE}
	java -jar "$<"

${BINFILE}: ${SOURCEFILE}
	kotlinc "$<" -include-runtime -d "$@"

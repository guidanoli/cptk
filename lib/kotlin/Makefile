SOURCEFILE=$(shell ./path)
BINFILE=$(addsuffix .jar, $(basename ${SOURCEFILE}))

.PHONY: run

run: ${BINFILE}
	java -jar "$<"

${BINFILE}: ${SOURCEFILE}
	kotlinc "$<" ${FLAGS} -include-runtime -d "$@"

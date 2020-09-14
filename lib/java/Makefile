SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)

.PHONY: run

run: ${BINFILE}
	java -cp $(dir $<) $(basename $(notdir $<))

${BINFILE}: ${SOURCEFILE}
	javac $<

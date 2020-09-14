SOURCEFILE=$(shell ./src)
BINFILE=$(addsuffix .class, $(basename ${SOURCEFILE}))

.PHONY: run

run: ${BINFILE}
	java -cp "$(dir $<)" "$(basename $(notdir $<))"

${BINFILE}: ${SOURCEFILE}
	javac "$<"

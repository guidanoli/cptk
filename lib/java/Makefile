SOURCEFILE=$(shell ./path)
BINFILE=$(addsuffix .class, $(basename ${SOURCEFILE}))

.PHONY: run debug

run: ${BINFILE}
	java -classpath "$(dir $<)" "$(basename $(notdir $<))"

debug: ${BINFILE}
	jdb -classpath "$(dir $<)" "$(basename $(notdir $<))"

${BINFILE}: ${SOURCEFILE}
	javac "$<"

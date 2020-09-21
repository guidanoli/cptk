SOURCEFILE=$(shell ./src)
BINFILE=$(addsuffix .class, $(basename ${SOURCEFILE}))

.PHONY: run rund

run: ${BINFILE}
	java -classpath "$(dir $<)" "$(basename $(notdir $<))"

rund: ${BINFILE}
	jdb -classpath "$(dir $<)" "$(basename $(notdir $<))"

${BINFILE}: ${SOURCEFILE}
	javac "$<"

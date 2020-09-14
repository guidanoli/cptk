SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)

${BINFILE}: ${SOURCEFILE}
	kotlinc $< -include-runtime -d $@

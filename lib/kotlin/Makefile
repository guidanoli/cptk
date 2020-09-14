SOURCEFILE=$(shell ./src)

temp/prog.jar: ${SOURCEFILE}
	kotlinc $< -include-runtime -d $@

SOURCEFILE=${tempdir}/prog.kt
BINFILE=$(addsuffix .jar, $(basename ${SOURCEFILE}))

.PHONY: path run

path:
	echo "${SOURCEFILE}"

run: ${BINFILE}
	java -jar "$<"

${BINFILE}: ${SOURCEFILE}
	kotlinc "$<" -include-runtime -d "$@"

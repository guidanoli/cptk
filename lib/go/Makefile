SOURCEFILE=${tempdir}/prog.go
BINFILE=$(addsuffix .out, $(basename ${SOURCEFILE}))

.PHONY: path run debug

path:
	echo "${SOURCEFILE}"

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb "$<"

${BINFILE}: ${SOURCEFILE}
	go build -o "$@" "$<"

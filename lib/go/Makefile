SOURCEFILE=$(shell ./path)
BINFILE=$(shell ./xpath)

.PHONY: run debug

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb "$<"

${BINFILE}: ${SOURCEFILE}
	go build -o "$@" "$<"

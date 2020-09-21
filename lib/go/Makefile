SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)

.PHONY: run rund

run: ${BINFILE}
	"$<"

rund: ${BINFILE}
	gdb "$<"

${BINFILE}: ${SOURCEFILE}
	go build -o "$@" "$<"

SOURCEFILE=temp/$(shell ./path)
BINFILE=temp/$(shell ./xpath)

.PHONY: run debug

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb "$<"

${BINFILE}: ${SOURCEFILE}
	go build -o "$@" "$<"

FLAGSFILE=temp/flags
NEWFLAGSFILE=$(addsuffix .new, ${FLAGSFILE})
SOURCEFILE=temp/$(shell ./path)
BINFILE=temp/$(shell ./xpath)
CFLAGS=$(shell cat ${FLAGSFILE})

.PHONY: run debug update-flags

update-flags:
	if ([ -f "${NEWFLAGSFILE}" ] && (! [ -f "${FLAGSFILE}" ] || \
	   (! diff ${NEWFLAGSFILE} ${FLAGSFILE} > /dev/null))); then \
		mv "${NEWFLAGSFILE}" "${FLAGSFILE}"; \
	fi

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb "$<"

${BINFILE}: ${SOURCEFILE} ${FLAGSFILE}
	gcc "$<" -o "$@" -lm $(CFLAGS)

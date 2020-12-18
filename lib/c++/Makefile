FLAGSFILE=temp/flags.dat
NEWFLAGSFILE=$(addsuffix .new, ${FLAGSFILE})
SOURCEFILE=temp/$(shell ./path)
BINFILE=temp/$(shell ./xpath)
CXXFLAGS=$(shell cat ${FLAGSFILE})

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
	g++ "$<" -o "$@" -lm $(CXXFLAGS)

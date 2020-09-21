FLAGSFILE=temp/flags.dat
NEWFLAGSFILE=$(addsuffix .new, ${FLAGSFILE})
SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)
CSFLAGS=$(shell cat ${FLAGSFILE})

.PHONY: run rund update-flags

update-flags:
	if ([ -f "${NEWFLAGSFILE}" ] && (! [ -f "${FLAGSFILE}" ] || \
	   (! diff ${NEWFLAGSFILE} ${FLAGSFILE} > /dev/null))); then \
		mv "${NEWFLAGSFILE}" "${FLAGSFILE}"; \
	fi

run: ${BINFILE}
	"$<"

rund: ${BINFILE}
	gdb --args mono --debug "$<"

${BINFILE}: ${SOURCEFILE} ${FLAGSFILE}
	mcs -out:"$@" "$<" $(CSFLAGS)

FLAGSFILE=${tempdir}/flags
NEWFLAGSFILE=$(addsuffix .new, ${FLAGSFILE})
SOURCEFILE=${tempdir}/prog.cs
BINFILE=$(addsuffix .out, $(basename ${SOURCEFILE}))
CSFLAGS=$(shell cat ${FLAGSFILE})

.PHONY: path run debug update-flags

path:
	echo "${SOURCEFILE}"

update-flags:
	if ([ -f "${NEWFLAGSFILE}" ] && (! [ -f "${FLAGSFILE}" ] || \
	   (! diff ${NEWFLAGSFILE} ${FLAGSFILE} > /dev/null))); then \
		mv "${NEWFLAGSFILE}" "${FLAGSFILE}"; \
	fi

run: ${BINFILE}
	"$<"

debug: ${BINFILE}
	gdb --args mono --debug "$<"

${BINFILE}: ${SOURCEFILE} ${FLAGSFILE}
	mcs -out:"$@" "$<" $(CSFLAGS)

FLAGSFILE=${tempdir}/flags
NEWFLAGSFILE=$(addsuffix .new, ${FLAGSFILE})
SOURCEFILE=${tempdir}/prog.hs
BINFILE=$(basename ${SOURCEFILE})
CFLAGS=$(shell cat ${FLAGSFILE})

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
	gdb "$<"

${BINFILE}: ${SOURCEFILE} ${FLAGSFILE}
	ghc "$<" $(CFLAGS)

FLAGSFILE=temp/flags.dat
NEWFLAGSFILE=$(addsuffix .new, ${FLAGSFILE})
SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)
CXXFLAGS=$(shell cat ${FLAGSFILE})

.PHONY: run update-flags

update-flags:
	if (! [ -f "${FLAGSFILE}" ] || (([ -f "${FLAGSFILE}" ]) && \
	   (! diff ${NEWFLAGSFILE} ${FLAGSFILE} > /dev/null))); then \
		mv "${NEWFLAGSFILE}" "${FLAGSFILE}"; \
	fi

run: ${BINFILE}
	"$<"

${BINFILE}: ${SOURCEFILE} ${FLAGSFILE}
	${CXX} "$<" -o "$@" $(CXXFLAGS)

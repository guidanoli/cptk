NEWFLAGSFILE=temp/newflags.dat
NEWFLAGSFILE=$(addsuffix .new, ${FLAGSFILE})
SOURCEFILE=$(shell ./src)
BINFILE=$(shell ./bin)
CFLAGS=$(shell cat ${FLAGSFILE})

.PHONY: run update-flags

update-flags:
	if [ -f "${NEWFLAGSFILE}" ]; then \
		if ! diff ${NEWFLAGSFILE} ${FLAGSFILE} > /dev/null ; then \
			mv "${NEWFLAGSFILE}" "${FLAGSFILE}"; \
		fi \
	fi

run: ${BINFILE}
	"$<"

${BINFILE}: ${SOURCEFILE} ${FLAGSFILE}
	${CC} "$<" -o "$@" $(CFLAGS)

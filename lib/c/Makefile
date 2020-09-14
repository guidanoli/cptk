FLAGSFILE=temp/flags.dat
CFLAGS=$(shell cat ${FLAGSFILE})

temp/prog.out: temp/prog.c ${FLAGSFILE}
	${CC} $< -o $@ $(CFLAGS)

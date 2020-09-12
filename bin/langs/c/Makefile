CFLAGS=$(file < temp/flags.dat)

temp/prog.out: temp/prog.c temp/flags.dat
	${CC} $< -o $@ $(CFLAGS)

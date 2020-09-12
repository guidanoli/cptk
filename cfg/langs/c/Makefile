CFLAGS=$(file < temp/flags)

temp/prog.out: temp/prog.c temp/flags
	${CC} $< -o $@ $(CFLAGS)

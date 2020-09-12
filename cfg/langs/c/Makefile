CFLAGS=$(file < temp/flags.cfg)

temp/prog.out: temp/prog.c temp/flags.cfg
	${CC} $< -o $@ $(CFLAGS)

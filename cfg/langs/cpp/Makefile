CXXFLAGS=$(file < temp/flags.cfg)

temp/prog.out: temp/prog.cpp temp/flags.cfg
	${CXX} $< -o $@ $(CXXFLAGS)

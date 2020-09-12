CXXFLAGS=$(file < temp/flags.dat)

temp/prog.out: temp/prog.cpp temp/flags.dat
	${CXX} $< -o $@ $(CXXFLAGS)

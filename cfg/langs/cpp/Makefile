CXXFLAGS=$(file < temp/flags)

temp/prog.out: temp/prog.cpp temp/flags
	${CXX} $< -o $@ $(CXXFLAGS)

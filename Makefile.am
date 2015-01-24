#include aminclude.am 
#EXTRA_DIST = doc/manual.html doc/scrm.1 m4/ac_doxygen.m4
bin_PROGRAMS = codeMonkey_scrm codeMonkey_scrm_omp
#man_MANS = doc/scrm.1

#TESTS = unit_tests algorithm_tests 
#check_PROGRAMS = unit_tests algorithm_tests scrm_dbg scrm_prof
PROG = SCRM

#dist-hook:
#	export VERSION=${VERSION}; cd doc; make

#unittests: unit_tests
#	./unit_tests 

#algorithmtests: algorithm_tests
#	./algorithm_tests 

#travis-test: unittests algorithmtests scrm scrm_dbg
#	./tests/test_binaries.sh

nrml_src = scrm/src/param.cc scrm/src/forest.cc scrm/src/node.cc scrm/src/node_container.cc scrm/src/time_interval.cc \
		   scrm/src/model.cc scrm/src/tree_point.cc \
		   scrm/src/param.h scrm/src/forest.h scrm/src/node.h scrm/src/node_container.h scrm/src/time_interval.h \
		   scrm/src/model.h scrm/src/tree_point.h scrm/src/event.h

random_src = scrm/src/random/random_generator.cc scrm/src/random/mersenne_twister.cc \
			 scrm/src/random/fastfunc.cc \
			 scrm/src/random/random_generator.h scrm/src/random/mersenne_twister.h \
			 scrm/src/random/fastfunc.h 

sumstat_src = scrm/src/summary_statistics/tmrca.cc \
			  scrm/src/summary_statistics/seg_sites.cc \
			  scrm/src/summary_statistics/frequency_spectrum.cc \
			  scrm/src/summary_statistics/newick_tree.cc \
			  scrm/src/summary_statistics/tmrca.h \
			  scrm/src/summary_statistics/seg_sites.h \
			  scrm/src/summary_statistics/frequency_spectrum.h \
			  scrm/src/summary_statistics/newick_tree.h \
			  scrm/src/summary_statistics/summary_statistic.h \
			  scrm/src/summary_statistics/first_last_tmrca.cc \
			  scrm/src/summary_statistics/first_last_tmrca.h
 
scrm_src = $(nrml_src) $(random_src) $(sumstat_src)

debug_src = scrm/src/random/constant_generator.cc scrm/src/random/constant_generator.h \
			scrm/src/forest-debug.cc scrm/src/random/constant_generator.h

#unit_test_src = tests/test_forest.cc tests/test_model.cc tests/test_node.cc tests/test_node_container.cc\
#			   	tests/test_runner.cc tests/test_time_interval.cc tests/test_fastfunc.cc tests/test_param.cc\
#				tests/test_random_generator.cc tests/test_summary_statistics.cc 

#alg_test_src = tests/test_runner.cc tests/test_algorithm.cc 


codeMonkey_scrm_SOURCES = $(scrm_src) codeMonkey_scrm.cpp
codeMonkey_scrm_omp_SOURCES = $(scrm_src) codeMonkey_scrm.cpp
#scrm_dbg_SOURCES = $(scrm_src) $(debug_src) scrm/src/scrm.cc
#scrm_prof_SOURCES = $(scrm_src) scrm/src/scrm.cc
#unit_tests_SOURCES = $(scrm_src) $(debug_src) $(unit_test_src)
#algorithm_tests_SOURCES = $(scrm_src) $(alg_test_src)
 
codeMonkey_scrm_CXXFLAGS= -DNDEBUG -std=c++0x -Iscrm/src/
codeMonkey_scrm_omp_CXXFLAGS= -DNDEBUG -std=c++0x -fopenmp -Iscrm/src/
#scrm_dbg_CXXFLAGS= -std=c++0x
#scrm_prof_CXXFLAGS= -pg -DNDEBUG -std=c++0x
#unit_tests_CXXFLAGS = -DUNITTEST -DNDEBUG -std=c++0x 
#algorithm_tests_CXXFLAGS = -DUNITTEST -DNDEBUG -std=c++0x 
#unit_tests_LDADD= -L/opt/local/lib -lcppunit -ldl #link the cppunit unittest library in mac, cppunit was installed via macports
#algorithm_tests_LDADD= -L/opt/local/lib -lcppunit -ldl  #link the cppunit unittest library in mac, cppunit was installed via macports

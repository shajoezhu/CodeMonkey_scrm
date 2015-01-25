bin_PROGRAMS = codeMonkey_scrm codeMonkey_scrm_omp
PROG = SCRM

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

codeMonkey_scrm_SOURCES = $(nrml_src) $(random_src) $(sumstat_src) codeMonkey_scrm.cpp
codeMonkey_scrm_omp_SOURCES = $(codeMonkey_scrm_SOURCES) 
 
codeMonkey_scrm_CXXFLAGS= -DNDEBUG -std=c++0x -Iscrm/src/
codeMonkey_scrm_omp_CXXFLAGS= $(codeMonkey_scrm_CXXFLAGS) -fopenmp 

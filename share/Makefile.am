SAMPLES = samples/configure.ac.libpopt

TEMPLATES = template/top/trunk/AUTHORS \
            template/top/trunk/ChangeLog \
            template/top/trunk/configure.ac \
            template/top/trunk/Makefile.am \
            template/top/trunk/NEWS \
            template/top/trunk/README \
            template/top/trunk/bin/Makefile.am \
            template/top/trunk/bin/projname.sh.in \
            template/top/trunk/include/Makefile.am \
            template/top/trunk/include/projname/projname.h \
            template/top/trunk/share/Makefile.am \
            template/top/trunk/share/projname.txt \
            template/top/trunk/src/libprojname.cc \
            template/top/trunk/src/Makefile.am \
            template/top/trunk/src/projname.cc

nobase_dist_pkgdata_DATA = prep_develop_skeleton.txt \
                           $(SAMPLES) $(TEMPLATES)

install-data-hook:
	mkdir -p @PACKAGE_DATADIR_PATH@/template/top/{branches,tags}

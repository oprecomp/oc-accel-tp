#
# Makefile
#

all:

.PHONY += help
help:
	@echo "SNAP configuration system"
	@echo
	@echo "  Please ensure that you have installed your Linux kernel"
	@echo "  sources and the tools to build and configure it. We are"
	@echo "  using the same infrastructure to generate the SNAP"
	@echo "  configuration files."
	@echo
	@echo "Possible targets are:"
	@echo "  menuconfig - use menuconfig/ncurses"
	@echo "  gconfig    - use gconfig/GTK+"
	@echo "  xconfig    - use xconfig/QT"
	@echo "  config     - use config/command line version"
	@echo "  prepare    - generate configuration specific header."
	@echo

.PHONY += menuconfig gconfig xconfig config oldconfig silentoldconfig prepare clean distclean
menuconfig gconfig xconfig config oldconfig silentoldconfig prepare:
	./snap_cfg -o $@ 2>/dev/null

install:

uninstall:

clean:
	$(RM) build/config build/*~ *~
	$(RM) ide/*.pyc

distclean: clean
	$(RM) ../software/include/autoconf.h

TOP        = ../..
SWIG       = $(TOP)/../preinst-swig
CXXSRCS    = example.cxx
TARGET     = example
INTERFACE  = example.i
SWIGOPT    = -c++
DELPHISRCS = example.pas
DELPHIFLAGS= 

all::	delphi

delphi::
	$(MAKE) -f $(TOP)/Makefile CXXSRCS='$(CXXSRCS)' SWIG='$(SWIG)' \
	SWIGOPT='$(SWIGOPT)' TARGET='$(TARGET)' INTERFACE='$(INTERFACE)' delphi_cpp
	$(MAKE) -f $(TOP)/Makefile DELPHISRCS='$(DELPHISRCS)' delphi_compile
	$(MAKE) -f $(TOP)/Makefile DELPHISRCS='runme.dpr' delphi_compile

clean::
	$(MAKE) -f $(TOP)/Makefile delphi_clean

check: all
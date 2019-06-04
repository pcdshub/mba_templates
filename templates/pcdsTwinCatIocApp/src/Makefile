TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build an ioc application
PROD_IOC = _APPNAME_

# _APPNAME_.dbd will be created and installed
DBD += _APPNAME_.dbd

# _APPNAME_.dbd will be made up from these files:
_APPNAME__DBD += base.dbd
_APPNAME__DBD += iocAdmin.dbd
_APPNAME__DBD += asSupport.dbd
_APPNAME__DBD += ads.dbd
_APPNAME__DBD += asyn.dbd
_APPNAME__DBD += drvAsynIPPort.dbd

ifneq (,$(findstring /,$(CALC)))
  _APPNAME__DBD += calcSupport.dbd
  _APPNAME__LIBS += calc
endif

ifneq (,$(findstring /,$(ADS)))
  _APPNAME__LIBS += ads
  _APPNAME__DBD  += ads.dbd
endif

ifneq (,$(findstring /,$(MOTOR)))
  _APPNAME__DBD += motorSupport.dbd
  _APPNAME__DBD += devSoftMotor.dbd
  _APPNAME__DBD += EthercatMcSupport.dbd

  _APPNAME__LIBS += motor
  _APPNAME__LIBS += softMotor
  _APPNAME__LIBS += EthercatMcSupport
endif

# _APPNAME__registerRecordDeviceDriver.cpp will be created from _APPNAME_.dbd
_APPNAME__SRCS += _APPNAME__registerRecordDeviceDriver.cpp
_APPNAME__SRCS_DEFAULT += _APPNAME_Main.cpp

_APPNAME__LIBS += devIocStats
_APPNAME__LIBS += asyn
_APPNAME__LIBS += autosave
_APPNAME__LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

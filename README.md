PCDS makeBaseApp.pl Templates
=============================

(Only intended for initial development; will not be a standalone repo forever)

To use:

```bash
    $ source /reg/g/pcds/setup/epicsenv-7.0.2-2.0.sh
    $ git clone https://github.com/pcdshub/mba_templates mba_templates
    $ export EPICS_MBA_BASE=$EPICS_BASE
    $ export EPICS_MBA_TEMPLATE_TOP=$PWD/mba_templates/templates
    $ makeBaseApp.pl -l
    Valid application types are:
            pcdsTwinCatIoc
    Valid iocBoot types are:
            pcdsTwinCatIoc
    Valid module types are:
```

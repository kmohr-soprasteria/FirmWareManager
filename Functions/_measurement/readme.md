Measurement functions can be added to this (temporary) _measurement folder for initial grouping.

No chain of functions, like in DPMDP (waterfall), but rather each task is done independently from others
by a function (including its subfunctions).

Measurement:
- measurement admin get informed about the list of updated devices
  - devices get written into manager by dedicated function (incl. subfunctions)
- current state of firmware to be read from devices
  - only read whats needed
    - equipment
    - firmware
  - device-specific information
- current state is input for
  - operationalDataStore
  - but also for RunningDS (equipment part)
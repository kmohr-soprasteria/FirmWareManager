# p1UpdateSelectedMwdiReplica

The p1UpdateSelectedMwdiReplica is cyclically processing:  

- Replicate updated ControlConstructs from the MWDI ES index into the MWDI ES Replica index
  - the function does not replicate the complete ControlConstructs, but rather the subset
    of data required by FirmWareManager
- Adding the list of mountNames with updated ControlConstructs to the MeasurementManager
  - processing of these devices is done by separate, independent functions

## Diagram

<p align="center">
  <img src="./p1UpdateSelectedMwdiReplica.png" alt="p1UpdateSelectedMwdiReplica diagram" width="400" />
</p>

## Interface

Detailed description of the [interface](./interface.yaml).  

## Variables

Detailed description of the [internal variables](./variables.yaml).  
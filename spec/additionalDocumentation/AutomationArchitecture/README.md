# AutomationArchitecture

## Application Design

<p align="center">
  <img src="./diagrams/AutomationArchitecture.png" alt="AutomationArchitecture" width="600"/>
</p>

> [!IMPORTANT]  
> The picture contains annotations from when the architecture was explained.  
> It may not be accurate in regards to when the RunningDS is loaded to CandidateDS
> (see below).

<p align="center">
  <img src="./diagrams/AutomationArchitecture_annotated.png" alt="AutomationArchitectureAnnotated" width="600"/>
</p>



## Example Use Case

_[to be created from 260623 Example FW update.pptx]_

**WIP**

A new firmware version shall be rolled out for a RTN950 device.  
Upon receipt of the request from outside, the CandidateDS shall be initialized with the current content of the RunningDS. The request shall then be interpreted. A successful interpretation leads to an update of the firmware version of the addressed RTN950 device in the CandidateDS.

> [!IMPORTANT]  
> It is unclear when and how the CandidateDS is overwritten with the contents of the RunningDS
> A change from the candidateDS may only be written to the RunningDS (commit), if validation is ok.
> It is also clear how (near-)parallel requests are to be handled?
> Can we have changes for multiple devices in the Candidate at once? - this would be problematic, if some pass validation and some do not...
> If we only allow one change in the Candidate at once (so processing of other change requests is paused), then why does issue 2 have multiple red boxes in the validation....

<p align="center">
  <img src="./diagrams/usecase1_01.png" alt="UseCase1_01" width="600"/>
</p>

<p align="center">
  <img src="./diagrams/usecase1_01.png" alt="UseCase1_02" width="600"/>
</p>

<p align="center">
  <img src="./diagrams/usecase1_02.png" alt="UseCase1_03" width="600"/>
</p>

<p align="center">
  <img src="./diagrams/usecase1_03.png" alt="UseCase1_04" width="600"/>
</p>

<p align="center">
  <img src="./diagrams/usecase1_04.png" alt="UseCase1_05" width="600"/>
</p>

<p align="center">
  <img src="./diagrams/usecase1_05.png" alt="UseCase1_06" width="600"/>
</p>

<p align="center">
  <img src="./diagrams/usecase1_06.png" alt="UseCase1_07" width="600"/>
</p>
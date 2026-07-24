# AutomationArchitecture

## Application Design

<p align="center">
  <img src="./diagrams/AutomationArchitecture.png" alt="AutomationArchitecture" width="600"/>
</p>

<p align="center">
  <img src="./diagrams/AutomationArchitecture_annotated.png" alt="AutomationArchitectureAnnotated" width="600"/>
</p>



## Example Use Case

_[to be created from 260623 Example FW update.pptx]_


A new firmware version shall be rolled out to all RTN950 devices.  
When the request is received, the content of the RunningDS is copied to the CandidateDS. At this point, the CandidateDS still contains firmware version 4.21 for all RTN950 devices. (This initial copy operation is not shown in the figure.)  
The request is then interpreted, and the firmware version of all RTN950 devices in the CandidateDS is updated to 10.26.

<p align="center">
  <img src="./diagrams/usecase1_01.png" alt="UseCase1_01" width="650"/>
</p>




<p align="center">
  <img src="./diagrams/usecase1_02.png" alt="UseCase1_02" width="650"/>
</p>

<p align="center">
  <img src="./diagrams/usecase1_03.png" alt="UseCase1_03" width="650"/>
</p>

<p align="center">
  <img src="./diagrams/usecase1_04.png" alt="UseCase1_04" width="650"/>
</p>

<p align="center">
  <img src="./diagrams/usecase1_05.png" alt="UseCase1_05" width="650"/>
</p>

<p align="center">
  <img src="./diagrams/usecase1_06.png" alt="UseCase1_06" width="650"/>
</p>

<p align="center">
  <img src="./diagrams/usecase1_07.png" alt="UseCase1_07" width="650"/>
</p>
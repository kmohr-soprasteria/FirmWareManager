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

In the next step, the changes contained in the CandidateDS are validated.  
Only if all validation checks are successful does the CandidateDS overwrite the RunningDS, thereby establishing the new approved target state.  

<p align="center">
  <img src="./diagrams/usecase1_02.png" alt="UseCase1_02" width="650"/>
</p>

The pulser triggers the Measurement function to retrieve the current device state from the network and store the relevant information in the OperationalDS.  
At this point, all RTN950 devices are running firmware version 4.21 in the network, and consequently, firmware version 4.21 is recorded in the OperationalDS.

<p align="center">
  <img src="./diagrams/usecase1_03.png" alt="UseCase1_03" width="650"/>
</p>

Next, the pulser triggers the Monitoring function.  
Monitoring compares the desired state stored in the RunningDS with the actual state stored in the OperationalDS.  
Since the RTN950 devices are expected to run firmware version 10.26 but are currently running firmware version 4.21, alarms are created and added to the CurrentAlarms list.

<p align="center">
  <img src="./diagrams/usecase1_04.png" alt="UseCase1_04" width="650"/>
</p>

Triggered by the pulser, the Implementation functions process the entries in the CurrentAlarms list.  
They perform the required firmware upgrades on the affected devices in the network.  

<p align="center">
  <img src="./diagrams/usecase1_05.png" alt="UseCase1_05" width="650"/>
</p>

Once the firmware upgrade has been completed on some devices, those devices are running firmware version 10.26.  
The Measurement function detects the updated firmware version and updates the corresponding entries in the OperationalDS accordingly.  

<p align="center">
  <img src="./diagrams/usecase1_06.png" alt="UseCase1_06" width="650"/>
</p>

The Monitoring function compares the OperationalDS against the RunningDS to identify deviations between the actual and intended states.  
As the first two devices have successfully been upgraded to firmware version 10.26, no discrepancy remains for these devices.  Therefore, the associated alarm entries are cleared from the CurrentAlarms list.

<p align="center">
  <img src="./diagrams/usecase1_07.png" alt="UseCase1_07" width="650"/>
</p>
# MDinterfaceTables
## Overview

This file details NRT interfaces in a per system view.

## Process

To add a new interface, simply add it as a row under the relevant system or subsystem. Be sure to increment the interface ID and add the coresponding interface.

## Rules

* All interface descriptions have two parts with two unique sides
* Interfaces should be kept up to date using version control
* Each individual interface shall have an owner identified (even if temporary)
* Detailed interfaces requiring drawings or detailed software specifications shall have an Interface Control Document (ICD) identified.
* When deleting an interface - simply use line through format on the removed interface and continue incrementing the IDs (they will not necessarily be sequential)
* When editing an interface - ensure the change column is updated with author /change owner

## NRT Interface Tables

### Rotator (RT_ICN_X)
ID | Interface | Description | Responsible | Coresponding ID | Document linking
---|-----------|-------------|-------------|-----------------|-----------------
RT_ICN_1 | M1 Cell mounting | The Rotator assembly shall be mounted to the OSS via the M1 cell bottom face allowing it to meet its functional and performance requirements  | Cesar/ A. Ranjbar | M1C_ICN_3 | na
RT_ICN_2 | A&G Box | The Rotator assembly shall transmit the rotational torque to the A&G box via a slew bearing allowing it to meet its functional and performance requirements | A. Ranjbar | A&G_ICN_1 | na
RT_ICN_3 | TLS | The Rotator shall receive status and control parameters from the TLS and provide diagnostic data as well as guiding data | I. Steele | na

### A&G Box (A&G_ICN_X)
ID | Interface | Description | Responsible | Coresponding ID | Document linking
---|-----------|-------------|-------------|-----------------|-----------------
A&G_ICN_1 | Rotator | The Rotator assembly shall transmit the rotational torque to the A&G box via a slew bearing allowing it to meet its functional and performance requirements | A. Ranjbar | RT_ICN_2 | na
A&G_ICN_2 | Fold mirror assembly | The fold mirror assembly shall be mounted to the A&G box via a linear rail mechanism allowing it to meet its functional and performance requirements | A. Ranjbar | na | na
A&G_ICN_3 | Wave Front Sensor | The fold mirror assembly shall be mounted to the A&G box via a linear rail mechanism allowing it to meet its functional and performance requirements | A. Ranjbar | na | na
A&G_ICN_4 | Autoguider | The Autoguider pickoff mirror shall be mounted to the A&G box within 30 arcmin?? | A. Ranjbar | AG_ICN_1 | na
A&G_ICN_5 | TLS | The A&G shall receive status and control parameters from the TLS and provide diagnostic data as well as guiding data – See AG_TLS_ICD | I. Steele | na | na
A&G_ICN_6 | Instruments | TBD – Is it all handled via the TLS interface or is there direct communication with instruments on the network? | I. Steele | na | na

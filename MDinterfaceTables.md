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

### Autoguider Interface (AGI_ICN_X)
ID | Interface | Description | Responsible | Coresponding ID | Document linking
---|-----------|-------------|-------------|-----------------|-----------------
AGI_ICN_1 | A&G Box | The Autoguider pickoff mirror shall be mounted to the A&G box within 30 arcmin?? | A. Ranjbar | na | na
AGI_ICN_2 | M2 | The AG pick off mirror shall be located to allow a vignetted optical path within the 30arcmin beam from the M2. Focusing on the AG is set by the focus stage (controllable?) | I. Steele | na | na
AGI_ICN_3 | TLS | The AG shall receive status and control parameters from the TLS and provide diagnostic data as well as guiding data – See AG_TLS_ICD | I. Steele | na | na
IGI_ICN_4 | Instruments | TBD – Is the all handled via the TLS interface or is there direct communication with instruments on the network? |  I. Steele | na | na

### Fold Mirror (FM_ICN_X)
ID | Interface | Description | Responsible | Coresponding ID | Document linking
---|-----------|-------------|-------------|-----------------|-----------------
FM_ICN_1 | A&G Box | The fold mirror assembly shall be mounted to the A&G box via a linear rail mechanism allowing it to meet its functional and performance requirements | A. Ranjbar | AGI_ICN_1 | na
FM_ICN_2 | M2 | The fold mirror shall keep the alignment with m2 allowing it to meet its functional and performance requirements | A. Ranjbar | na | na
FM_ICN_3 | TLS | The fold mirror shall receive status and control parameters from the TLS and provide diagnostic data as well as guiding data – See AG_TLS_ICD | I. Steele | na | na
FM_ICN_4 | Instruments | The fold mirror shall keep the alignment with the instruments allowing it to meet its functional and performance requirements | I. Steele | na | na

### FWFS Integration (WS_ICN_X)
ID | Interface | Description | Responsible | Coresponding ID | Document linking
---|-----------|-------------|-------------|-----------------|-----------------
WS_ICN_1 | A&G Box | The Wavefront sensor pickoff mirror shall be mounted to the A&G box within 30 arcmin?? | A. Ranjbar | na | na
WS_ICN_2 | TLS | The WS shall receive status and control parameters from the TLS and provide diagnostic data as well as guiding data –  | I. Steele | na | na

### Autoguider (AG_ICN_X)
ID | Interface | Description | Responsible | Coresponding ID | Document linking
---|-----------|-------------|-------------|-----------------|-----------------
AG_ICN_1 | Mechanical to A&G Box | The AG assemblies (fold mirror and tube/camera assembly) shall be mounted in the A&G box allowing it to meet it’s functional and performance requirements – i.e. mounted to a stable area within the bottom of the A&G with clearance between other instruments, foreoptics and moving mechanisms | A&G Box Mechanical Engineer (AR) | na | na
AG_ICN_2 | Optical to A&G box | The optical path from the M2 shall not be obscured by any mechanism regardless of science fold position. | A&G Box Mechanical Engineer (AR) | na | na
AG_ICN_3 | Services to A&G Box | The AG will receive a standard AC single phase power connection from the A&G box supply distribution as well as a connection to the A&G box ethernet network switch | A&G Box Mechanical Engineer (AR) | na | na
AG_ICN_4 | Software to TLS | The AG shall receive status and control parameters from the TLS and provide diagnostic data as well as guiding data – See AG_TLS_ICD  | DevOps Engineer | na | AG_TLS_ICD
AG_ICN_5 | Software to Data Archive |  AG images will be stored at the telescope data archive  | DevOps Engineer | na | na

### M1 Cell (M1C_ICN_X)
ID | Interface | Description | Responsible | Coresponding ID | Document linking
---|-----------|-------------|-------------|-----------------|-----------------
M1C_ICN_1 | User | The M1 Cell shall allow sufficient access to the bottom of the primary mirror, for maintenance purposes. | J. Gracia / C. Rodríguez | na | na
M1C_ICN_2 | OSS | Stiff connection between centre section and M1 cell required for proper performance | J. Gracia / C. Rodríguez | na | na
M1C_ICN_3 | Focal Station | The bottom of the M1 cell requires to be stiffly connected to the rotator / focal station | J. Gracia / A. Ranjbar | na | na
M1C_ICN_4 | Focal Station | The M1 cell space frame shall provide a clear light path to the rotator. | J. Gracia / C. Rodríguez | na | na
M1C_ICN_5 | M1 Support | The top of the M1 cell shall provide support for the M1 segment subassemblies. | C. Rodríguez / M. Torres

### M2 Sub (M2S_ICN_X)
ID | Interface | Description | Responsible | Coresponding ID | Document linking
---|-----------|-------------|-------------|-----------------|-----------------
M2S_ICN_1 | User | The M2 subassembly shall provide enough access to remove the mirror for maintenance activities. | J. Gracia / C. Rodríguez | M1C_ICN_2 
M2S_ICN_2 | OSS | The M2 subassembly shall interface with the tube at the top section, requiring a stiff connection. | J. Gracia / C. Rodríguez | M2S_ICN_2 
M2S_ICN_3 | M2 Support | The M2 subassembly shall interface with the M2 support and positioning system, providing a stiff mounting point for this system | J. Gracia / C. Rodríguez |
M2S_ICN_4 | M2 | The M2 envelope shall incorporate a small lip to prevent it from falling in case of support failure. | J. Gracia / C. Rodríguez |
M2S_ICN_5 | Enclosure | The M2 subassembly shall interface with the enclosure by guaranteeing a physical separation between the top-most part of the telescope and the enclosure roof, allowing full telescope movement even when the roof is closed. | J. Gracia / C. Rodríguez |

### OSS (OSS_ICN_X)
ID | Interface | Description | Responsible | Coresponding ID | Document linking
---|-----------|-------------|-------------|-----------------|-----------------
OSS_ICN_1 | M1 Cell | Stiff connection between centre section and M1 cell required for proper performance | J. Gracia / C. Rodríguez | M1C_ICN_2 
OSS_ICN_2 | M2 Subassembly | The M2 subassembly shall interface with the tube at the top section, requiring a stiff connection. | J. Gracia / C. Rodríguez | M2S_ICN_2 
OSS_ICN_3 | User | The tube shall provide enough space to access mirrors for disassembly and maintenance. | J. Gracia / C. Rodríguez |
OSS_ICN_4 | Mount | The OSS and the mount shall interface through the elevation trunnion and drive. | J. Gracia / C. Rodríguez |
OSS_ICN_5 | Instruments | The OSS shall be balanced around the elevation axis. It shall incorporate systems that allow a varying instrument load. | J. Gracia / C. Rodríguez |

### Mount (MNT_ICN_X)
ID | Interface | Description | Responsible | Coresponding ID | Document linking
---|-----------|-------------|-------------|-----------------|-----------------
MNT_ICN_1 |
MNT_ICN_2 |
MNT_ICN_3 |
MNT_ICN_4 |
MNT_ICN_5 |

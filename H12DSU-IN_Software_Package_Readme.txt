================================================================================
Supermicro System BIOS & IPMI Firmware Update Package Operation Instructions
================================================================================

Please read this document in it before performing the system BIOS or IPMI
firmware update.  Please verify that your system meets the requirments.


********************************************************************************
This update package includes the following system software updates & utilities:

--- BIOS/IPMI Firmware Update Package ---

  BIOS   - BIOS_H12DSU-1B54_20250922_3.5_STDsp.zip             (REV 3.5)
  BMC    - BMC_H12AST2500-B101MS_20250925_03.10.48_STDsp.zip   (REV 03.10.48)

--- BIOS/Firmware Update Tools ---

  SuperServer Automation Assistant (SAA)       v1.3.0:
  saa_1.3.0-p9_Win_x86_64_20250902.zip            (for Windows)
  saa_1.3.0-p9_Linux_x86_64_20250902.tar.gz       (for Linux)
  saa_1.3.0-p9_BSD_x86_64_20250902.tar.gz         (for FreeBSD)
 
 
  Note: For BIOS update with SAA utility through Out-Of-Band (OOB) channel, the
        SFT-OOB-LIC or SFT-DCMS-Single is no longer required.

--- Supported Products ---

  Supermicro Motherboards:
  MBD-H12DSU-IN
  


*************************************************************************************
                                     Important notes
*************************************************************************************

1. The UEFI version of SAA tool will replace AMI AFU BIOS flash utility in H12 DP
   motherboard BIOS.

2. Using AFU tool will end up with the BIOS corruption.  It should never be used!


*************************************************************************************
                       SYSTEM HARDWARE and FIRMWARE REQUIREMENTS
*************************************************************************************

1) BIOS version R 2.x supports 7002 and 7003 processors.
2) The Flash Utility in the package only supports BIOS update from version R 1.x to R 2.x, and rolling back is not allowed.
3) The default boot mode for BIOS version R2.x has been changed to EFI. If your OS is legacy, please press the <Del> key during POST to enter the BIOS setup to change boot mode after upgrading to R2.x.
4) When updating BIOS from version 2.1 to version 2.3a or above through SUM, don’t preserve the BIOS settings because some BIOS settings are modified after version 2.3a.
5) In the event of a BIOS rescue failure, please use your previous BIOS version and put it on your boot drive to boot, or you could recover it through the IPMI WebUI.


*************************************************************************************
                                         Warning
*************************************************************************************

1. Do not interrupt, reboot or remove power from your system during the update.
   Doing so may cause the system failure.

2. If the software update fails, you may contact our RMA Department to have the BIOS/
   IPMI firmware chip reprogrammed.  This will require shipping the board to Supermicro
   for repair.  Please submit your RMA request at:
   http://www.supermicro.com/support/rma/.

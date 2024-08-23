# Siemens v2.2 HBCD Protocol Release Notes

## Installation Instructions

For HBCD sites, please make sure to follow the HBCD protocol upgrade SOP which will help ensure there are records of when each protocol update is applied at your site.

Before importing the HBCD protocol, please ensure you have received and installed the necessary C2P sequence packages for access to the latest versions of each sequence:

- **[Multiband EPI (University of Minnesota) Sequence Download and Installation Instructions](https://www.cmrr.umn.edu/multiband/)**

- **[vNav Morphometry (University of Pennsylvania) Instructions](https://mri-motion-correction-vnav-morphometry.readthedocs-hosted.com/en/nxva30a_162141/requesting.html)**

- **QALAS (Boston Children’s Hospital):** Please contact Borjan Gagoski (Borjan.Gagoski@childrens.harvard.edu)

- **ISTHMUS spectroscopy (Johns Hopkins University):** Please contact Richard Edden (edden@jhu.edu)

Without these C2P packages installed, the protocol cannot be imported.

**IMPORTANT DIRECTIONS BEFORE SEQUENCE INSTALLATION:** Siemens has identified a bug in NXVA30A SP02 (the software baseline used for this study) that may cause your scanner to become non-responsive during the installation of the certificates required for custom sequences. Please ensure you have SP02 SD05 installed on your scanner before proceeding, as this fixes the bug and allows you to install custom sequences.

**IMPORTANT UPGRADE NOTE FOR v2.2:** The HBCD vNav Structural sequence package from University of Pennsylvania has been updated since the HBCD v2.1 protocol. To enable full compatibility with the FIRMM tablet, please install the latest version of the HBCD vNav Structural sequence package on your scanner. The latest version can be requested from Dylan Tisdall (mtisdall@pennmedicine.upenn.edu)

**N4VE11C (a.k.a., VE11C) systems**<br>
This software baseline is no longer supported. All scanners must upgrade to NXVA30A SP02 to run the v2.0 or later protocol.

**NXVA30A (a.k.a., XA30) systems**<br>
1.	This package can only be installed on systems with the SP02 service pack installed. To confirm this is installed, go to the "?" menu in the top-right corner of the scanner console, then select "About", then click on “System Info”; a window should pop up with the following version information:

      Numaris/X VA30A-03GR<br>
      syngo OAK_v7QR2201

      or

      Numaris/X VA30A-03MV<br>
      syngo OAK_v7QR2301B

If you double click the "VA30A-03GR" (or “VA30A-03MV”), it shows the build stamp, which should be

    Numaris/X VA30A.Night_20220414.2 C228547

    or

    Numaris/X VA30A.Night_20230910.1 C338286

If your version and/or build stamp do not match these values, please contact Siemens to upgrade to the SP02 or SP03 service pack.

2.	Note that this protocol requires the CS_SPACE, SMS, and SVS licenses from Siemens be activated on your scanner. If you do not have these licenses, protocols will not import or run correctly. HBCD has negotiated group pricing for the CS_SPACE and SVS licenses if you do not already have them activated.

3.	Please put the files “DiffusionVectors_HBCD_pe1_03142022.dvs” and “DiffusionVectors_HBCD_pe2_03142022.dvs” into:

C:\ProgramData\Siemens\Numaris\MriCustomer\CustomerSeq\DiffusionVectorSets\

Note, the “ProgramData” directory may not be visible in Windows Explorer, but can be accessed by typing the path into the address bar. You may have to create the “DiffusionVectorSets” directory if it does not already exist.

4.	If the file does not already exist, please create an empty text file at the location:

C:\ProgramData\Siemens\Numaris\MriCustomer\MriSiteData\Paradigms\Local\PresentationSystemAvailable.txt

This file is needed to ensure the pre-configured integration with the FIRMM tablet operates correctly within our protocol.

5.	Please import “HBCD_NXVA30A_v2.2_32ch.exar1” and/or “HBCD_NXVA30A_v2.2_64ch.exar1” files, and copy the “HBCD_v2.2_32ch” and/or “HBCD_v2.2_64ch” protocol to your scanner’s sequence tree.

6.	If you have a non-standard installation of your FIRMM tablet, where the tablet has a non-standard IP address or port, please contact Turing for directions on how to update the BOLD Add-In for the structural, fMRI and Diffusion sequences in the protocol to match your specific configuration. As distributed, the HBCD protocol assumes the FIRMM tablet is attached to the default IP address and port.

![image](https://github.com/user-attachments/assets/ee82e79e-22ae-45b9-9ca2-b3203f738eca)



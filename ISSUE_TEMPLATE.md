Make sure you have provided the following information:

 - [ ] link to your code branch cloned from rhboot/shim-review in the form user/repo@tag
 - [ ] completed README.md file with the necessary information
 - [ ] shim.efi to be signed
 - [ ] public portion of your certificate embedded in shim (the file passed to VENDOR_CERT_FILE)
 - [ ] any extra patches to shim via your own git tree or as files
 - [ ] any extra patches to grub via your own git tree or as files
 - [ ] build logs


###### What organization or people are asking to have this signed:
Advanced Design Corp. (https://www.a-d.co.jp/)


###### What product or service is this for:
DataSweeper (This refers to methods of totally erasing data from storage media that can then be reused.)


###### What is the origin and full version number of your shim?
15
https://github.com/rhboot/shim/releases/tag/15


###### What's the justification that this really does need to be signed for the whole world to be able to boot it:
The loader is used to load and start our native UEFI based pre-boot authentication.
It's essential to be able to provide software that works with every machine that has Secure Boot enabled.


###### How do you manage and protect the keys used in your SHIM?
Only public keys are in SHIM as it verifies signatures of loaded components.


###### Do you use EV certificates as embedded certificates in the SHIM?
No


###### What is the origin and full version number of your bootloader (GRUB or other)?
GRUB2 


###### If your SHIM launchers any other components, please provide further details on what is launched
No

###### How do the launched components prevent execution of unauthenticated code?
N/A

###### Does your SHIM load any loaders that support loading unsigned kernels (e.g. GRUB)?
GRUB2

###### What kernel are you using? Which patches does it includes to enforce Secure Boot?
Currently targeted to ship with 4.14.xx kernel.
No additional modifications or patches applied.

###### What changes were made since your SHIM was last signed?
N/A

###### What is the hash of your final SHIM binary?
(sha256) ad49b4afbec5cf763b9ea97347c7a397802f0ba79412d2e4caa2e0b7776ca9b5  shimx64.efi

This repo is for review of requests for signing shim.  To create a request for review:

- clone this repo
- edit the template below
- add the shim.efi to be signed
- add build logs
- commit all of that
- tag it with a tag of the form "myorg-shim-arch-YYYYMMDD"
- push that to github
- file an issue at https://github.com/rhboot/shim-review/issues with a link to your branch

Note that we really only have experience with using grub2 on Linux, so asking
us to endorse anything else for signing is going to require some convincing on
your part.

Here's the template:

-------------------------------------------------------------------------------
What organization or people are asking to have this signed:
-------------------------------------------------------------------------------
Advanced Design Corp. (https://www.a-d.co.jp/)

-------------------------------------------------------------------------------
What product or service is this for:
-------------------------------------------------------------------------------
DataSweeper (This refers to methods of totally erasing data from storage media that can then be reused.)

-------------------------------------------------------------------------------
What's the justification that this really does need to be signed for the whole world to be able to boot it:
-------------------------------------------------------------------------------
The loader is used to load and start our native UEFI based pre-boot authentication.
It's essential to be able to provide software that works with every machine that has Secure Boot enabled.

-------------------------------------------------------------------------------
Who is the primary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name:Takashi Ueda
- Position:Developer
- Email address:ueda@a-d.co.jp
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:N/A

-------------------------------------------------------------------------------
Who is the secondary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name:Yoshiyuki Hori
- Position:Product Manager
- Email address:hori@a-d.co.jp
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:N/A

-------------------------------------------------------------------------------
What upstream shim tag is this starting from:
-------------------------------------------------------------------------------
https://github.com/rhboot/shim/tree/15

-------------------------------------------------------------------------------
URL for a repo that contains the exact code which was built to get this binary:
-------------------------------------------------------------------------------
https://github.com/rhboot/shim/tree/15

-------------------------------------------------------------------------------
What patches are being applied and why:
-------------------------------------------------------------------------------
None

-------------------------------------------------------------------------------
What OS and toolchain must we use to reproduce this build?  Include where to find it, etc.  We're going to try to reproduce your build as close as possible to verify that it's really a build of the source tree you tell us it is, so these need to be fairly thorough. At the very least include the specific versions of gcc, binutils, and gnu-efi which were used, and where to find those binaries.
-------------------------------------------------------------------------------
ÅEUbuntu 18.04.1 LTS (Kernel 4.15.0-34-generic)
ÅEgcc (Ubuntu 7.3.0-16ubuntu3) 7.3.0
ÅEgnu-efi 3.0.8-0ubuntu1~18.04.1

-------------------------------------------------------------------------------
Which files in this repo are the logs for your build?   This should include logs for creating the buildroots, applying patches, doing the build, creating the archives, etc.
-------------------------------------------------------------------------------
bulid-log.txt

-------------------------------------------------------------------------------
Add any additional information you think we may need to validate this shim
-------------------------------------------------------------------------------
None


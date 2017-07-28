Cloud plugin v1.08 final for Total Commander

This is the Cloud file system plugin for Total Commander
It allows to access the following clouds:
- Box
- Dropbox
- Google Drive
- Windows Live SkyDrive
- Yandex Drive

It is possible to create multiple accounts on all the
services except for Yandex Drive.

WARNING:
========
This plugin uses the Internet Explorer control to log
into the cloud services. Unfortunately the services
use cookies to save the login. Therefore it is NOT
recommended to use this plugin on other people's
computers, e.g. when running TC from USB stick.

=========================================================
Automatic Installation
======================
Just double click on the plugin ZIP file within Total
Commander and follow the instructions.

Manual Installation
===================
1) Create subdirectory "Cloud" somewhere on your harddisk
2) Extract all the files from this archive to the Cloud directory
3) Select Configuration -> Options -> Operation
4) Click on FS-plugins and add cloudplugin.wfx

You can now use the plugin via Network Neighborhood

=========================================================
History
=======
20160526 Public release version 1.08 final
20160526 Added: Suppress script errors when logging in to Windows Live/OneDrive
20160525 Added: OneDrive: Use client_updated_time instead of updated_time for displayed timestamps
20151026 Public release version 1.07 final
20151025 Added: Google Drive: Configuration dialog to let the user choose the type of Google Docs downloads (e.g. OpenOffice, MS Office, HTML...)
20151025 Added: Google Drive: Download Google Docs documents, for now only as MS Office files
20151025 Added: Google Drive: Access files shared by other users
20150830 Public release version 1.06 final
20150830 Fixed: Google Drive: Problems with renaming/remote copying files, the timestamp was lost
20150811 Public release version 1.05 with Chromium
20150811 Added: Standalone version using Chromium instead of Internet Explorer control, also works on Windows XP
20150607 Public release version 1.05 final
20150607 Fixed: Yandex: No accents or cyrillic except for uploads and downloads
20150607 Fixed: OneDrive: Problems renaming file when name contained spaces or accented characters
20150601 Public release version 1.04 final
20150531 Fixed: Google Drive, rename/remote copy: Fail if target name already exists to avoid 2 files with same name
20150531 Fixed: Verify that a directory is empty before calling remove directory, because most clouds would delete all the content too!
20150529 Added: Copy and move files between folders directly on the server (not between accounts)
20150521 Public release version 1.03 final
20150521 Fixed: Upload to Microsoft OneDrive: Overwriting files on the server didn't work
20150413 Public release version 1.02 final
20150413 Fixed: File timestamp wrong after upload to Google Drive due to bug in its time parser. Milliseconds were interpreted as time zone offset
20150330 Public release version 1.01 final
20150330 Added: Properties of a file (Alt+Enter): Copy value under cursor, all URLs or everything to clipboard
20150301 Public release version 1.0 final
20150301 Fixed: Login to Yandex not working on XP -> use different OAUTH login method
20150216 Public release version 0.3 beta
20150215 Fixed: Could not see file sizes > 2GB
20141216 Public release version 0.2 beta
20141216 Fixed: Dropbox: Could not login on XP unless logged in on newer Windows first (problem with app auth)
20141216 Fixed: OneDrive: Could not rename file twice (file id was not updated)
20141211 Initial public release version 0.1 beta
=========================================================
Used components
===============

This Cloud plugin is using the following sources:
- vjson library for parsing json responses
  from https://code.google.com/p/vjson/
  Distributed under the MIT license.
  Copyright (c) 2010, Ivan Vashchaev 
- WinInet libary: Requires an installed Internet
  Explorer 8 or newer
- CVTUTF.C and CVTUTF.H: Used to convert to/from UTF-8.
  Copyright 1994-1999 IBM Corp.. All rights reserved.
  See below.
- My own code: See below (currently no source available)

Author: Christian Ghisler, www.ghisler.com

======================================================================
Legal documents:
======================================================================
CVTUTF.C and CVTUTF.H:
/*
File:	ConvertUTF.h, ConvertUTF.C
Author: Mark E. Davis
 * Copyright 1994-1999 IBM Corp.. All rights reserved.
 * 
 * IBM Corp. grants the user a nonexclusive right and license to use, execute,
 * display, modify, and prepare and/or have prepared derivative works of the
 * code, including but not limited to creating software products which
 * incorporate the code or derivative works thereof.
 * 
 * IBM Corp. grants the user a right and license to reproduce and distribute
 * the code as long as this entire copyright notice is reproduced in the code
 * or reproduction.
 * 
 * The code is provided AS-IS, and IBM Corp. disclaims all warranties,
 * either express or implied, including, but not limited to implied
 * warranties of merchantability and fitness for a particular purpose.
 * In no event will IBM Corp. be liable for any damages whatsoever (including,
 * without limitation, damages for loss of business profits, business
 * interruption, loss of business information, or other pecuniary
 * loss) arising out of the use or inability to use this code, even
 * if IBM Corp. has been advised of the possibility of such damages.
 * Because some states do not allow the exclusion or limitation of
 * liability for consequential or incidental damages, the above
 * limitation may not apply to you.
*/
======================================================================
My own code:
The cloud plugin is copyrighted freeware. It may be used freely
for commercial and non-commercial purposes. You may not charge
for this software, except with our written permission (via e-mail).
support@ghisler.com

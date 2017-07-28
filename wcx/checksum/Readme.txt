MD5/SHA1 checksum generator/checker v0.2b for Total Commander
=============================================================


 * How to install this plugin (32 bit only):
--------------------------------------------

 1. Unzip the "checksum.wcx" to the Total Commander or plugins directory
 2. In Windows Commander 4.0 (or newer) or Total Commander,
   choose 'Configuration => Options'
 3. Open the 'Packer' page
 4. Click 'Configure packer extension WCXs'
 5. Type 'md5' as the extension
 6. Click 'New type', and select the "checksum.wcx" file
 7. Click OK and then 'Configure packer extension WCXs'
 8. Now type 'sha' as the extension
 9. Click 'New type', and select the "checksum.wcx" file again
10. Click OK


 * What it does:
----------------

Provides MD5 and SHA1 checksum generator/checker from within Total Commander
packer interface. It is able to generate ".md5" and ".sha" list files
acceptable by GNU respectively md5sum and sha1sum utilities. There is also
'virtual' browser for these list files. You can "enter" into listing as it
were archive, test it and use Lister to see original/computed MD5/SHA1
checksums *BUT* it is only possible if ".md5" or ".sha" file is stored in
root path of all files listed inside it. See "Usage" section for details.


 * Usage:
---------

(This section uses MD5 checksums as example; for SHA1 the procedure is the
same, just replace every "md5" you see by "sha" :)

 I) Generate MD5 checksum:
   1. Select files you wish to compute checksum.
   2. Then go to "Files => Pack".
   3. Select "md5" as packer.
   4. PLEASE NOTE THAT ARCHIVE PATH WILL BE IGNORED!!!
      ".md5" 'archive' is *ALWAYS* generated in current directory
      (where checked files are), and NOT in opposite panel!
      The only exception is creating checksum of files stored on CD-ROM
      media as there's no way to create files there.
   5. Press OK and check CURRENT directory for ".md5" list generated.

 II) Verify MD5 checksum:
   1. Certify that ".md5" list is in it's right place (filenames listed
      in it should be relative to current directory).
   2. Select it and do "Files => Test Archive(s)".
   3. If any file doesn't matches stored MD5 checksum then
      "CRC error" message box appears.
   4. If everything's clear Total Commander remains quiet.

 III) Browse MD5 checksum list:
   1. Certify that ".md5" list is in it's right place (filenames listed
      in it should be relative to current directory).
   2. Select it and enter it as it were normal archive.
   3. If any file is present in ".md5" list but wasn't found in current
      directory then "?" is displayed instead of file date/time and size.
   4. PLEASE NOTE THAT FILES CAN NOT BE EXTRACTED AS ALREADY SHOULD BE
      ON YOUR DISK! If you try to extract ".md5" 'contents' over real
      files YOU LOOSE IT.
   5. Select file you wish to check and press F3 (call Lister).
   6. Lister will show complete file name, expected checksum and generated
      checksum. If both checksum matches then the last line is
      "MD5 checksum OK!".


* Bugs:
-------

 o You can mess MD5 with SHA1 checksums in same file. This has some funny
   consequences... Try adding both SHA1 & MD5 sums for same filename :P
 o Total Commander integration is a mess.
 o NOT overwriting sensitive data is user's responsability :)
 o I tried to make the best ".md5" parser I could with no Perl regexp.
   But I still miss regexp so very weird files may not be parsed correctly.
 o If file is present in listing but not in current directory then "?" is
   displayed instead of file date/time and size... But if you take a look
   at file "Properties"... You see amazing size of 4,294,967,295 Bytes,
   date 15/31/2107 and time 31:63:62. Guess why :)


* ChangeLog:
------------

 - v0.1 
	* first public release
 - v0.2
	* added support for SHA1
	* renamed to "checksum.wcx"
 - v0.2a
	* checksum.wcx size dropped from 25.5 Kb to 8 Kb (!!!)
	* replaced is*() functions from runtime by c00l macro hacks
	* fixed memory leak in parser
	* added ChangeLog :)
 - v0.2b
	* removed FILE_SHARE_DELETE flag from CreateFile() as it's NT-specific


* TODO:
-------

 o Improve Total Commander integration


* Not-TODO:
-------

 o Modify/delete support. I suggest you to use Notepad for such operations
   on ".md5" list files :)
 o Improve algorithms coding critic parts in assembly... Certainly your
   storage media is slower than your CPU anyway :)


 * References:
--------------

 o MD5 and STA1 implementations for PuTTY. Written directly from the spec by
   Simon Tatham. http://www.chiark.greenend.org.uk/~sgtatham/putty/
 o "WCX Writer's Reference" by Christian Ghisler & Jiri Barton
 o PACK Plugin for Windows Commander by DarkOne


 * License:
-----------

/****************************************************************************
	This file is part of MD5/SHA1 checksum generator/checker plugin for
	Total Commander.
	Copyright (C) 2003  Stanislaw Y. Pusep

	This program is free software; you can redistribute it and/or modify
	it under the terms of the GNU General Public License as published by
	the Free Software Foundation; either version 2 of the License, or
	(at your option) any later version.

	This program is distributed in the hope that it will be useful,
	but WITHOUT ANY WARRANTY; without even the implied warranty of
	MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
	GNU General Public License for more details.

	You should have received a copy of the GNU General Public License
	along with this program; if not, write to the Free Software
	Foundation, Inc., 675 Mass Ave, Cambridge, MA 02139, USA.

	E-Mail:	stanis@linuxmail.org
	Site:	http://sysdlabs.hypermart.net/
****************************************************************************/


 * Author:
----------

Stanislaw Y. Pusep (a.k.a. Stas)

    E-Mail:	stanis@linuxmail.org
    Site:	http://sysdlabs.hypermart.net/
(here you can find this program & other cool things)

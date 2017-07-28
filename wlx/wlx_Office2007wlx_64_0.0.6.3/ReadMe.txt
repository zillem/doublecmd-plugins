Office2007.wlx plugin (0.0.6.3)
2013.04.26
--------------------------------

= About =

Office2007.wlx plugin allows to Microsoft Ofice files as plain text in the lister window.


= Supported files extensions =

+ Word 2007 XML
  - .docx - Document
+ Excel 2007 XML
  - .xlsx - Workbook
+ PowerPoint 2007 XML
  - .pptx - Presentation
  - .ppsx - Presentation
  
 = Installation =
 
 Add Office2007.wlx file as lister plugin into your Total Commander instance. 
 
 = Known issues =
 
 Office2007.wlx plugin has been only tested with four default filetypes.
 Headers and footnotes does not work yet.
 
 If you found a bug, please, send me problematic file (if it's possible) attached to e-mail.

 = Additional file types =
 
 It is possible to use plugin with following files extensions:
 
  - docm, dotm, dotx,
  - potm, potx, ppam, ppsm, pptm,
  - xlam, xlsm, xltm, xltx.
  
 You can enable them by wincmd.ini only using proper syntax, similar to:
 
  25_detect="ext="DOCM" |ext="DOCX" | ext="PPTX" | ext="XLSX""
 
 *PLEASE NOTE THAT ADDITIONAL FILES FORMATS HAVE NOT BEEN TESTED*
 
 = Author =
 
 Implemented by Karol Kaminski aka fenixproductions.
 
 fenixproductions at o2 dot pl
 http://fenixproductions.qsh.eu
 
 64-bit build and minor modifications by Konstantin Vlasov
 support at flint-inc dot ru
 http://flint-inc.ru/
 
   
 = Credits =
 
 Office2007.wlx plugin is using:
 
 + tinyXML engine
   - copyright (c) 2000-2006 Lee Thomason (www.grinninglizard.com)
   - http://www.sourceforge.net/projects/tinyxml   
 
 + XUnzip library
 - written by Hans Dietrich
   - http://www.codeproject.com/KB/cpp/xzipunzip.aspx   
 
 
 = Licence =
 
 This plugin is released under The Code Project Open License (CPOL) 1.02.
 
 For more information, please, read "licence.txt" file.
 
 = History =
 0.0.6.3 (by Konstantin Vlasov)
 - 64-bit build
 - minor fixes and improvements
 0.0.6.2
 - added (test only) - images and WordArt objects in whole documents (Word only)
 0.0.6.1
 - added (test only) - support for tables in Word documents
 0.0.6
 - ulocked more documents extensions
 0.0.5 (private)
 - small Unicode issues fix
 0.0.4
  - fixed national characters display (for systems without Unicode fonts),
 0.0.3
  - better Unicode support,
 0.0.2
  - fixed "Access Violation" errors,
  - added support for empty files,
  - added/fixed UTF-8 to ANSII conversion,
  - added / fixed Excel files shows proper text (instead of numeric reference)
 0.0.1
  - first release
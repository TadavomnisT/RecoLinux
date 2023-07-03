## GCK'S FILE SIGNATURES TABLE

#### 03 June 2023

> This table of file signatures (aka "magic numbers") is a continuing
> work-in-progress. I had found little information on this in a single
> place, with the exception of the table in _Forensic Computing: A Practitioner's Guide_ by T. Sammes & B. Jenkinson (Springer, 2000); that was my inspiration to start this list in 2002. See also Wikipedia's [List of file signatures](http://en.wikipedia.org/wiki/List_of_file_signatures). Comments, additions, and queries can be sent to Gary Kessler at [gck@garykessler.net](mailto:gck@garykessler.net).
>
> This list is not exhaustive although I add new files as I find them or
> someone contributes signatures. Interpret the table as a one-way
> function: the magic number generally indicates the file type whereas the
> file type does not always have the given magic number. If you want to
> know to what a particular file extension refers, check out some of these
> sites:
>
> - [File Extension Seeker: Metasearch engine for file extensions](http://file-extension.net/seeker/)
> - [FILExt.com](http://filext.com/)
> - [FileInfo.com](http://www.fileinfo.com/)
> - [Wotsit.org](http://www.wotsit.org/), The Programmer's File and Data Resource
> - [DOT.WHAT?](http://www.dotwhat.net/)
> - [File-Extensions.org](http://www.file-extensions.org/)
>
> Some other useful information:
>
> - My [software utility](https://www.garykessler.net/software/index.html#filesigs)
>    page contains a custom signature file based upon this list, for use
>   with FTK, Scalpel, Simple Carver, Simple Carver Lite, and TrID. There is
>    also a raw CSV file and JSON file of signatures.
>
> - The [File Signatures](http://www.filesignatures.net/) Web site searches a database based upon file extension or file signature.
>
> - Tim Coakley's [Filesig.co.uk](http://www.filesig.co.uk/) site, with Filesig Manager and Simple Carver. Also, see Tim's [SQLite Database Catalog](http://www.filesig.co.uk/sqlitedatabasecatalog/) page, "a repository of information used to identify specific SQLite databases and properties for research purposes."
>
> - Marco Pontello's [TrID - File Identifier](http://mark0.net/soft-trid-e.html) utility designed to identify file types from their binary signatures.
>
> - The National Archives' [PRONOM](http://apps.nationalarchives.gov.uk/PRONOM/Default.aspx)
>    site provides on-line information about data file formats and their
>   supporting software products, as well as their multi-platform [DROID (Digital Record Object Identification)](http://www.nationalarchives.gov.uk/information-management/manage-information/preserving-digital-records/droid/) software.
>
> - Additional details on graphics file formats can be found at [The Graphics File Formats Page](http://www.dcs.ed.ac.uk/home/mxr/gfx/2d-hi.html) and the [Sustainability of Digital Formats Planning for Library of Congress Collections](http://www.digitalpreservation.gov/formats/fdd/still_fdd.shtml) site.
>
> - Additional details on audio and video file formats can be found at the [Sustainability of Digital Formats Planning for Library of Congress Collections](http://www.digitalpreservation.gov/formats/fdd/browse_list.shtml) site.
>
>
> If you are using a Linux/MacOS/Unix system, you can use the [file](http://en.wikipedia.org/wiki/File_%28command%29) command to determine the file type based upon the file signature, per the system's _magic_ file.
>
> And, one last and final item — if you are searching for network traffic
> in raw binary files (e.g., RAM or unallocated space), see [Hints About Looking for Network Packet Fragments](https://www.garykessler.net/library/netsig.html).
>
> * * *
>
> [ACKNOWLEDGEMENTS & COPYRIGHT NOTICE](#acks)
>
> * * *
>
> Hex SignatureÂ  Â  Â  Â  Â  Â ASCII SignatureFile ExtensionÂ  Â  Â  Â  Â  Â File Description
>
> TGATruevision Targa Graphic file
>
> **Trailer:**
>
> 54 52 55 45 56 49 53 49 Â  TRUEVISI
>
> 4F 4E 2D 58 46 49 4C 45 Â  ON-XFILE
>
> 2E 00 Â  Â  Â  Â  Â  Â  Â  Â  Â  Â  ..
>
> 00.PICIBM Storyboard bitmap fileMOVApple QuickTime movie filePIFWindows Program Information FileSEAMac Stuffit Self-Extracting ArchiveYTRIRIS OCR data file
>
> 00 00 00...AVIF Alliance for Open Media (AOMedia) Video 1 (AV1) Image File
>
> 00 00 00 00 00 00 00 00
>
> 00 00 00 00 00 00 00 00........
>
> ........XXXCompucon/Singer embroidery design file
>
> [11 byte offset]
>
> 00 00 00 00 00 00 00 00
>
> 00 00 00 00 00 00 00 00
>
> 00 00 00 00 00 00 00 00[11 byte offset]
>
> ........
>
> ........
>
> ........PDBPalmpilot Database/Document File
>
> [512 (0x200) byte offset]
>
> 00 00 00 00 00 00 00 00[512 (0x200) byte offset]
>
> ........RVTRevit Project File subheader
>
> 00 00 00 00 14 00 00 00........TBIWindows Disk Image file
>
> 00 00 00 20 66 74 79 70
>
> 68 65 69 63... ftyp
>
> heicHEICHigh Efficiency Image Container (HEIC), holding one or more High Efficiency Image File (HEIF)
>
> — aka H.265 — images, created using the High Efficiency Video Coding (HEVC) algorithm.
>
> Developed by the Moving Pictures Experts Group (MPEG) and adopted by Apple as the standard image
>
> file format in 2017.
>
> [8 byte offset]
>
> 00 00 00 00 62 31 05 00
>
> 09 00 00 00 00 20 00 00
>
> 00 09 00 00 00 00 00 00[8 byte offset]
>
> ....b1..
>
> ..... ..
>
> ........DATBitcoin Core wallet.dat file
>
> 00 00 00 0C 6A 50 20 20
>
> 0D 0A....jP
>
> ..JP2Various JPEG-2000 image file formats
>
> 00 00 01 00....ICOWindows icon fileSPLWindows NT/2000/XP printer spool file
>
> 00 00 01 Bx....MPEG, MPGMPEG video file
>
> **Trailer:**
>
> 00 00 01 B7 (...·)
>
> 00 00 01 BA....ºMPG, VOBDVD Video Movie File (video/dvd, video/mpeg) or DVD MPEG2
>
> **Trailer:**
>
> 00 00 01 B9 (...¹)
>
> 00 00 02 00...... CURWindows cursor fileWB2QuattroPro for Windows Spreadsheet file
>
> 00 00 02 00 06 04 06 00
>
> 08 00 00 00 00 00........
>
> ......WK1Lotus 1-2-3 spreadsheet (v1) file
>
> 00 00 03 F3...ón/aAmiga [Hunk](https://en.wikipedia.org/wiki/Amiga_Hunk) executable file
>
> 00 00 1A 00 00 10 04 00
>
> 00 00 00 00........
>
> ....WK3Lotus 1-2-3 spreadsheet (v3) file
>
> 00 00 1A 00 02 10 04 00
>
> 00 00 00 00........
>
> ....WK4, WK5Lotus 1-2-3 spreadsheet (v4, v5) file
>
> 00 00 1A 00 05 10 04
> .......123Lotus 1-2-3 spreadsheet (v9) file
>
> 00 00 49 49 58 50 52 **_or_**..IIXPR00 00 4D 4D 58 50 52..MMXPRQXDQuark Express document (Intel & Motorola, respectively)
>
> **NOTE:** It appears that the byte following the 0x52 ("R") is
>
> the language indicator; 0x33 ("3") seems to indicate English
>
> and 0x61 ("a") reportedly indicates Korean.
>
> 00 00 FE FF..þÿn/aByte-order mark for 32-bit Unicode Transformation Format/
>
> 4-octet Universal Character Set (UTF-32/UCS-4), big-endian files.
>
> (See the [Unicode Home Page](http://www.unicode.org/).)
>
> [6 byte offset]
>
> 00 00 FF FF FF FF[6 byte offset]
>
> ..ÿÿÿÿHLPWindows Help file
>
> 00 01 00 00 00.....TTFTrueType font file
>
> 00 01 00 00 4D 53 49 53
>
> 41 4D 20 44 61 74 61 62
>
> 61 73 65....MSIS
>
> AM Datab
>
> aseMNYMicrosoft Money file
>
> 00 01 00 00 53 74 61 6E
>
> 64 61 72 64 20 41 43 45
>
> 20 44 42....Stan
>
> dard ACE
>
> Â DBACCDBMicrosoft Access 2007 file
>
> 00 01 00 00 53 74 61 6E
>
> 64 61 72 64 20 4A 65 74
>
> 20 44 42....Stan
>
> dard Jet
>
> Â DBMDBMicrosoft Access file
>
> 00 01 00 08 00 01 00 01
>
> 01........
>
> .IMGVentura Publisher/GEM VDI Image Format Bitmap file
>
> 00 01 01...FLTOpenFlight 3D file
>
> 00 01 42 41..BAABAPalm Address Book Archive file
>
> 00 01 42 44..BDDBAPalm DateBook Archive file
>
> 00 06 15 61 00 00 00 02
>
> 00 00 04 D2 00 00 10 00...a....
>
> ...Ò....DBNetscape Navigator (v4) database file
>
> 00 0D BB A0..»Â n/aMbox table of contents file. ( **NOTE:** The next four bytes
>
> appear to be the number of e-mails in the associated _mbox_ file.)
>
> 00 11 AF..¯FLIFLIC Animation file
>
> 00 14 00 00 01 02 xx xx
>
> 03........
>
> .n/aBIOS details in RAM images
>
> 00 1E 84 90 00 00 00 00..„.....SNMNetscape Communicator (v4) mail folder
>
> 00 20 AF 30. ¯0TPLWii images container
>
> 00 3B 05 00 01 00 00 00.;......DBPaessler PRTG Monitoring System database file
>
> 00 5C 41 B1 FF.\\A±ÿ ENCMujahideen Secrets 2 encrypted file
>
> [512 (0x200) byte offset]
>
> 00 6E 1E F0[512 (0x200) byte offset]
>
> .n.ðPPTPowerPoint presentation subheader (MS Office)
>
> 00 BF.¿SOLAdobe Flash shared object file (e.g., Flash cookies)
>
> 00 FF FF FF FF FF FF FF
>
> FF FF FF 00 00 02 00 01.ÿÿÿÿÿÿÿ
>
> ÿÿÿ.....MDFAlcohol 120% CD image
>
> 01 00 00 00....EMFExtended (Enhanced) Windows Metafile Format, printer spool file
>
> (0x18-17 & 0xC4-36 is Win2K/NT; 0x5C0-1 is WinXP)
>
> 01 00 00 00 01.....PICUnknown type picture file
>
> 01 00 09 00 00 03......WMFWindows Metadata file (Win 3.x format)
>
> 01 00 02 00....ARFWebex Advanced Recording Format files.
>
> 01 00 39 30..90FDB, GDBFirebird and Interbase database files, respectively. See
>
> [IBPhoenix](http://www.ibphoenix.com/resources/documents/design/doc_24) for more information.
>
> 01 01 47 19 A4 00 00 00
>
> 00 00 00 00..G.#xA4...
>
> ....TBI[The Bat!](https://www.ritlabs.com/en/products/thebat/) secure e-mail Message Base Index file
>
> 01 0F 00 00....MDFMicrosoft SQL Server 2000 database
>
> 01 10..TR1Novell LANalyzer capture file
>
> 01 DA 01 01 00 03.Ú....RGBSilicon Graphics RGB Bitmap
>
> 01 FF 02 04 03 02.ÿ....DRWMicrografx vector graphic file
>
> 02 64 73 73.dssDSSDigital Speech Standard (Olympus, Grundig, & Phillips), v2
>
> 03.DATMapInfo Native Data FormatDB3dBASE III file
>
> 03 00 00 00....NFCNokia PC Suite Content Copier file
>
> QPHQuicken price history file
>
> 03 00 00 00 41 50 50 52....APPRADXApproach index file
>
> 03 64 73 73.dssDSSDigital Speech Standard, v3
>
> 04.DB4dBASE IV data file
>
> 04 00 00 00 xx xx xx xx
>
> xx xx xx xx 20 03 00 00 _**or**_........
>
> .... ...05 00 00 00 xx xx xx xx
>
> xx xx xx xx 20 03 00 00........
>
> .... ...n/a[INFO2 Windows recycle bin](http://downloads.sourceforge.net/project/odessa/ODESSA/White%20Papers/Recycler_Bin_Record_Reconstruction.pdf) file. NOTE: Bytes 12-13
>
> indicate the size of each INFO2 record; the most common
>
> value is 0x20-03 (0x0320 = 800 bytes).
>
> 06 06 ED F5 D8 1D 46 E5
>
> BD 31 EF E7 FE 74 B7 1D..íõØ.Få
>
> ½1ïçþt·.INDDAdobe InDesign document
>
> 06 0E 2B 34 02 05 01 01
>
> 0D 01 02 01 01 02..+4....
>
> ......MXF[Material Exchange Format](https://www.loc.gov/preservation/digital/formats/fdd/fdd000013.shtml) file
>
> 07.DRWA common signature and file extension for many drawing
>
> programs.
>
> 07 53 4B 46.SKFSKFSkinCrafter skin file
>
> 07 64 74 32 64 64 74 64.dt2ddtdDTDDesignTools 2D Design file
>
> 08.DBdBASE IV or dBFast configuration file
>
> 08 00 45..En/aPossibly, maybe, might be a fragment of an Ethernet frame carrying
>
> an IPv4 packet. See [Hints About Looking for Network Packet Fragments](https://www.garykessler.net/library/netsig.html).
>
> [512 (0x200) byte offset]
>
> 09 08 10 00 00 06 05 00[512 (0x200) byte offset]
>
> ........XLSExcel spreadsheet subheader (MS Office)
>
> 0A nn 01...PCX[ZSOFT Paintbrush file](https://www.fileformat.info/format/pcx/egff.htm)
>
> (where Version ( _nn_) = 0x00, 0x02, 0x03, 0x04, or 0x05)
>
> 0A 16 6F 72 67 2E 62 69
>
> 74 63 6F 69 6E 2E 70 72..org.bi
>
> tcoin.prWALLETMultiBit Bitcoin wallet file
>
> 0C ED.íMPMonochrome Picture TIFF bitmap file (unconfirmed)
>
> 0D 44 4F 43.DOCDOCDeskMate Document file
>
> 0E 4E 65 72 6F 49 53 4F.NeroISONRINero CD Compilation
>
> 0E 57 4B 53.WKSWKSDeskMate Worksheet
>
> [512 (0x200) byte offset]
>
> 0F 00 E8 03[512 (0x200) byte offset]
>
> ..è.PPTPowerPoint presentation subheader (MS Office)
>
> 0F 53 49 42 45 4C 49 55
>
> 53.SIBELIU
>
> SSIB Sibelius Music - Score file
>
> 10 00 00 00....CL5Easy CD Creator 5 Layout file
>
> 1A 00 00...NTFLotus Notes database template
>
> 1A 00 00 04 00 00......NSFLotus Notes database
>
> 1A 0x..ARCLH archive file, old version
>
> (where x = 0x2, 0x3, 0x4, 0x8 or 0x9
>
> for types 1-5, respectively)
>
> 1A 0B..PAKCompressed archive file
>
> (often associated with Quake Engine games)
>
> 1A 35 01 00.5..ETHGN Nettest WinPharoah capture file
>
> 1A 45 DF A3.Eß£MKVMatroska stream fileWEBMWebM video file
>
> 1A 52 54 53 20 43 4F 4D
>
> 50 52 45 53 53 45 44 20
>
> 49 4D 41 47 45 20 56 31
>
> 2E 30 1A.RTS COM
>
> PRESSED
>
> IMAGE V1
>
> .0.DATRuntime Software compressed disk image
>
> 1D 7D.}WSWordStar Version 5.0/6.0 document
>
> 1F 8B 08.‹.GZ, TGZGZIP archive fileVLTVLC Player Skin file
>
> 1F 8B 08 00.‹..DSSSynology router configuration backup file
>
> 1F 9D..TAR.ZCompressed tape archive file using standard (Lempel-Ziv-Welch) compression
>
> 1F A0.Â TAR.ZCompressed tape archive file using LZH (Lempel-Ziv-Huffman) compression
>
> 21!BSBPitney Bowes' MapInfo Sea Chart format
>
> 21 0D 0A 43 52 52 2F 54
>
> 68 69 73 20 65 6C 65 63
>
> 74 72 6F 6E 69 63 20 63
>
> 68 61 72 74 20 77 61 73
>
> 20 70 72 6F 64 75 63 65
>
> 64 20 75 6E 64 65 72 20
>
> 74 68 65 20 61 75 74 68
>
> 6F 72 69 74 79 20 6F 66
>
> 20 55 53 41 2D 4E 4F 41
>
> 41 2F 4E 4F 53 2E 0D 0A!..CRR/T
>
> his elec
>
> tronic c
>
> hart was
>
> Â produce
>
> d under
>
> the auth
>
> ority of
>
> Â USA-NOA
>
> A/NOS...BSBNOAA Raster Navigation Chart (RNC®) file ( [https://charts.noaa.gov/RNCs/RNCs.shtml](https://charts.noaa.gov/RNCs/RNCs.shtml)).
>
> See also the [BSB/KAP File Format](https://opencpn.org/wiki/dokuwiki/doku.php?id=opencpn:supplementary_software:chart_conversion_manual:bsb_kap_file_format&do=export_pdf) specification
>
> 21 12!.AINAIN Compressed Archive
>
> 21 3C 61 72 63 68 3E 0A!<arch>.LIBUnix archiver (ar) files and Microsoft Program Library
>
> Common Object File Format (COFF)
>
> 21 42 44 4E!BDNMicrosoft Outlook [Personal Folder Files (PFF)](https://www.forensicswiki.org/wiki/Personal_Folder_File_(PAB,_PST,_OST)):
>
> OSTMicrosoft Outlook Offline Storage Folder File
>
> PABMicrosoft Outlook Personal Address Book File
>
> PSTMicrosoft Outlook [Personal Folder File](http://www.file-recovery.com/pst-signature-format.htm)
>
> 23 20\# MSICerius2 file
>
> 23 20 44 69 73 6B 20 44
>
> 65 73 63 72 69 70 74 6F\# Disk D
>
> escriptoVMDKVMware 4 Virtual Disk description file (split disk)
>
> 23 20 4D 69 63 72 6F 73
>
> 6F 66 74 20 44 65 76 65
>
> 6C 6F 70 65 72 20 53 74
>
> 75 64 69 6F\# Micros
>
> oft Deve
>
> loper St
>
> udioDSPMicrosoft Developer Studio project file
>
> 23 20 54 68 69 73 20 69
>
> 73 20 61 6E 20 4B 65 79\# This i
>
> s an KeyETAGoogle Earth Keyhole Placemark file
>
> 23 21 41 4D 52#!AMRAMRAdaptive Multi-Rate ACELP (Algebraic Code Excited Linear Prediction)
>
> Codec, commonly audio format with GSM cell phones. (See [RFC 4867](http://www.rfc-editor.org/rfc/rfc4867.txt).)
>
> 23 21 53 49 4C 4B 0A#!SILK.SIL[Audio compression format](http://tools.ietf.org/html/draft-spittka-silk-payload-format-00) developed by Skype; also used by other applications.
>
> 23 3F 52 41 44 49 41 4E
>
> 43 45 0A#?RADIAN
>
> CE.HDRRadiance High Dynamic Range image file
>
> 23 40 7E 5E#@~^VBEVBScript Encoded script
>
> 23 4E 42 46#NBFNBFNVIDIA Scene Graph binary file
>
> 23 50 45 43 30 30 30 31
>
> 4C 41 3A#PEC0001
>
> LA:PECBrother/Babylock/Bernina Home Embroidery file
>
> 23 50 45 53 30#PES0PESBrother/Babylock/Bernina Home Embroidery file
>
> 24 46 4C 32 40 28 23 29
>
> 20 53 50 53 53 20 44 41
>
> 54 41 20 46 49 4C 45$FL2@(#)
>
>  Â SPSS DA
>
> TA FILESAVSPSS Statistics (née Statistical Package for the Social Sciences, then
>
> Statistical Product and Service Solutions) data file
>
> 25 21 50 53 2D 41 64 6F
>
> 62 65 2D%!PS-Ado
>
> be-PSPostScript file
>
> 25 21 50 53 2D 41 64 6F
>
> 62 65 2D 33 2E 30 20 45
>
> 50 53 46 2D 33 20 30%!PS-Ado
>
> be-3.0 E
>
> PSF-3.0EPSAdobe encapsulated PostScript file
>
> (If this signature is not at the immediate
>
> beginning of the file, it will occur early
>
> in the file, commonly at byte offset 30 [0x1E])
>
> 25 50 44 46%PDFPDF, FDF, AIAdobe Portable Document Format, Forms Document Format, and Illustrator graphics files
>
> **Trailers:**
>
> 0A 25 25 45 4F 46 (.%%EOF)
>
> 0A 25 25 45 4F 46 0A (.%%EOF.)
>
> 0D 0A 25 25 45 4F 46 0D 0A (..%%EOF..)
>
> 0D 25 25 45 4F 46 0D (.%%EOF.)
>
> **NOTE:** There may be multiple end-of-file marks within the
>
> file. When carving, be sure to get the last one.
>
> 25 62 69 74 6D 61 70%bitmapFBMFuzzy bitmap (FBM) file
>
> 28 54 68 69 73 20 66 69
>
> 6C 65 20 6D 75 73 74 20
>
> 62 65 20 63 6F 6E 76 65
>
> 72 74 65 64 20 77 69 74
>
> 68 20 42 69 6E 48 65 78
>
> 20(This fi
>
> le must
>
> be conve
>
> rted wit
>
> h BinHex
>
> HQXMacintosh BinHex 4 Compressed Archive
>
> 2A 2A 2A 20 20 49 6E 73
>
> 74 61 6C 6C 61 74 69 6F
>
> 6E 20 53 74 61 72 74 65
>
> 64 20\*\*\*Â Â Ins
>
> tallatio
>
> n Starte
>
> d LOGSymantec Wise Installer log file
>
> [2 byte offset]
>
> 2D 6C 68[2 byte offset]
>
> -lhLHA, LZHCompressed archive file
>
> 2E 52 45 43.RECIVRRealPlayer video file (V11 and later)
>
> 2E 52 4D 46.RMFRM, RMVBRealMedia streaming media file
>
> 2E 52 4D 46 00 00 00 12
>
> 00.RMF....
>
> .RARealAudio file
>
> 2E 72 61 FD 00.raý.RARealAudio streaming media file
>
> 2E 73 6E 64.sndAUNeXT/Sun Microsystems µ-Law audio file
>
> 2F 2F 20 3C 21 2D 2D 20
>
> 3C 6D 64 62 3A 6D 6F 72
>
> 6B 3A 7A// <!\-\-
>
> <mdb:mor
>
> k:zMSFThunderbird\|Mozilla Mail Summary File
>
> 300CATMicrosoft security catalog file
>
> 30 00 00 00 4C 66 4C 650...LfLeEVTWindows Event Viewer file
>
> 30 20 48 45 41 440 HEADGED[GEnealogical Data COMmunication (GEDCOM)](https://www.thoughtco.com/genealogy-gedcom-basics-1421891) file
>
> 30 26 B2 75 8E 66 CF 11
>
> A6 D9 00 AA 00 62 CE 6C0&²u.fÏ.
>
> ¦Ù.ª.bÎlASF, WMA, WMVMicrosoft Windows Media Audio/Video File
>
> ( [Advanced Systems Format](http://www.digitalpreservation.gov/formats/fdd/fdd000067.shtml))
>
> 30 31 4F 52 44 4E 41 4E
>
> 43 45 20 53 55 52 56 45
>
> 59 20 20 20 20 20 20 2001ORDNAN
>
> CE SURVE
>
> YÂ Â Â Â Â Â Â NTFNational Transfer Format Map File
>
> 30 37 30 37 30 nn07070.n/aArchive created with the cpio utility (where _nn_
>
> values 0x37 ("7"), 0x31 ("1"), and 0x32 ("2") refer to the
>
> standard ASCII format, new ASCII (aka SVR4) format, and CRC
>
> format, respectively. (The [swpackage(8)](http://www.gnu.org/software/swbis/swpackage_8.html) page has additional
>
> information.) (Thanks to F. Webber for this....)
>
> 31 BE **_or_**1¾32 BE2¾WRIMicrosoft Write file
>
> 32 03 10 00 00 00 00 00
>
> 00 00 80 00 00 00 FF 002.......
>
> ......ÿ.PCSPfaff Home Embroidery file
>
> 34 CD B2 A14Í²¡n/aExtended tcpdump (libpcap) capture file (Linux/Unix)
>
> 37 7A BC AF 27 1C7z¼¯'.7Z7-Zip compressed file
>
> 37 E4 53 96 C9 DB D6 077äS–ÛÖ.n/azisofs compression format, recognized by some Linux kernels. See the
>
> [libburnia](http://libburnia-project.org/wiki/zisofs) page for additional information.
>
> 38 42 50 538BPSPSDPhotoshop image file
>
> 3A 56 45 52 53 49 4F 4E:VERSIONSLESurfplan kite project file
>
> 3C<ASXAdvanced Stream redirector fileXDRBizTalk XML-Data Reduced Schema fileWSFWindows Script Component
>
> 3C 21 64 6F 63 74 79 70<!doctypDCIAOL HTML mail file
>
> 3C 3F<?WSCWindows Script Component
>
> 3C 3F 78 6D 6C 20 76 65
>
> 72 73 69 6F 6E 3D<?xml ve
>
> rsion=MANIFESTWindows Visual Stylesheet XML file
>
> 3C 3F 78 6D 6C 20 76 65
>
> 72 73 69 6F 6E 3D 22 31
>
> 2E 30 22 3F 3E<?xml ve
>
> rsion="1
>
> .0"?>XULXML User Interface Language file
>
> 3C 3F 78 6D 6C 20 76 65
>
> 72 73 69 6F 6E 3D 22 31
>
> 2E 30 22 3F 3E 0D 0A 3C
>
> 4D 4D 43 5F 43 6F 6E 73
>
> 6F 6C 65 46 69 6C 65 20
>
> 43 6F 6E 73 6F 6C 65 56
>
> 65 72 73 69 6F 6E 3D 22<?xml ve
>
> rsion="1
>
> .0"?>..<
>
> MMC\_Cons
>
> oleFile
>
> ConsoleV
>
> ersion="MSCMicrosoft Management Console Snap-in Control file
>
> 3C 43 54 72 61 6E 73 54
>
> 69 6D 65 6C 69 6E 65 3E<CTransT
>
> imeline>MXFPicasa movie project file
>
> 3C 43 73 6F 75 6E 64 53
>
> 79 6E 74 68 65 73 69 7A<CsoundS
>
> ynthesizCSDCsound music file
>
> 3C 4B 65 79 68 6F 6C 65 3E<Keyhole>ETAGoogle Earth Keyhole Overlay file
>
> 3C 4D 61 6B 65 72 46 69
>
> 6C 65 20<MakerFi
>
> le FM, MIFAdobe FrameMaker file
>
> 3C 67 70 78 20 76 65 72
>
> 73 69 6F 6E 3D 22 31 2E
>
> 31<gpx ver
>
> sion="1.
>
> 1GPX[GPS eXchange file (v1.1 schema)](http://www.topografix.com/GPX/1/1/)
>
> 3C 7E 36 3C 5C 25 5F 30
>
> 67 53 71 68 3B<~6<\\%\_0
>
> gSqh;B85[ASCII85](http://en.wikipedia.org/wiki/Ascii85) (aka BASE85) encoded file, sometimes used with PostScript and PDF.
>
> **Trailer:** 7E 3E 0A (~>.)
>
> [24 (0x18) byte offset]
>
> 3E 00 03 00 FE FF 09 00
>
> 06[24 (0x18) byte offset]
>
> >...þÿ..
>
> .WB3Quatro Pro for Windows 7.0 Notebook file
>
> 3F 5F 03 00?\_..GIDWindows Help index fileHLPWindows Help file
>
> [32 (0x20) byte offset]
>
> 40 40 40 20 00 00 40 40
>
> 40 40[32 (0x20) byte offset]
>
> @@@ ..@@
>
> @@ENLEndNote Library File
>
> 41 42 6F 78ABoxABOX2[Analog Box](https://sites.google.com/site/analogbox2/home) circuit files
>
> 41 43ACDWGGeneric [AutoCAD](https://en.wikipedia.org/wiki/AutoCAD) drawing file
>
> > **NOTES on AutoCAD file headers:** The 0x41-43 (AC) is a generic header, occupying the first
> >
> > two bytes in the file. The next [three or four bytes](https://en.wikipedia.org/wiki/.dwg) give further indication about the version
> >
> > (see also [_DWG file specifications released by OpenDesign_](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)):
> >
> > - 0x31-2E-32 (1.2) — AutoCAD v1.2 (Release 2)
> > - 0x31-2E-33 (1.3) — AutoCAD v1.3 (Release 3)
> > - 0x31-2E-34-30 (1.40) — AutoCAD v1.40 (Release 4)
> > - 0x31-2E-35-30 (1.50) — AutoCAD v2.05 (Release 5)
> > - 0x32-2E-31-30 (2.10) — AutoCAD v2.10 (Release 6)
> > - 0x31-30-30-32 (1002) — AutoCAD v2.5 (Release 7)
> > - 0x31-30-30-33 (1003) — AutoCAD v2.6 (Release 8)
> > - 0x31-30-30-34 (1004) — AutoCAD v9.0 (Release 9)
> > - 0x31-30-30-36 (1006) — AutoCAD v10.0 (Release 10)
> > - 0x31-30-30-39 (1009) — AutoCAD v11.0 (Release 11)/v12.0 (Release 12)
> > - 0x31-30-31-32 (1012) — AutoCAD v13.0 (Release 13)
> > - 0x31-30-31-34 (1014) — AutoCAD v14.0 (Release 14)
> > - 0x31-30-31-35 (1015) — AutoCAD 2000 (v15.0)/2000i (v15.1)/2002 (v15.2) -- (Releases 15-17)
> > - 0x31-30-31-38 (1018) — AutoCAD 2004 (v16.0)/2005 (v16.1)/2006 (v16.2) -- (Releases 18-20)
> > - 0x31-30-32-31 (1021) — AutoCAD 2007 (v17.0)/2008 (v17.1)/2009 (v17.2) -- (Releases 21-23)
> > - 0x31-30-32-34 (1024) — AutoCAD 2010 (v18.0)/2011 (v18.1)/2012 (v18.2) -- (Releases 24-26)
> > - 0x31-30-32-37 (1027) — AutoCAD 2013 (v19.0)/2014 (v19.1)/2015 (v20.0)/2016 (v20.1)/2017 (v20.2) -- (Releases 27-31)
> > - 0x31-30-33-32 (1032) — AutoCAD 2018 (v22.0) (Release 32)
>
> 41 43 76ACLSLESteganos Security Suite virtual secure drive
>
> 41 43 53 44ACSDn/aMiscellaneous AOL parameter and information files
>
> 41 45 53AESAES[AES Crypt](http://www.aescrypt.com/) file format. (The fourth byte is the version number.)
>
> 41 4D 59 4FAMYOSYWHarvard Graphics symbol graphic
>
> 41 4F 4C 20 46 65 65 64
>
> 62 61 67AOL Feed
>
> bagBAGAOL and AIM buddy list file
>
> 41 4F 4C 44 42AOLDBABY, IDXAOL database files: address book (ABY) and user configuration
>
> data (MAIN.IDX)
>
> 41 4F 4C 49 44 58AOLIDXINDAOL client preferences/settings file (MAIN.IND)
>
> 41 4F 4C 49 4E 44 45 58AOLINDEXABIAOL address book index file
>
> 41 4F 4C 56 4D 31 30 30AOLVM100ORG, PFCAOL personal file cabinet (PFC) file
>
> **NOTE:** See [PFC-Details.zip](http://web.archive.org/web/20050420101922/http://members.aol.com/fvongordon/pfc/PFC-Details.zip) for PFC file format information.
>
> 41 56 47 36 5F 49 6E 74
>
> 65 67 72 69 74 79 5F 44
>
> 61 74 61 62 61 73 65AVG6\_Int
>
> egrity\_D
>
> atabaseDATAVG6 Integrity database file
>
> 41 72 43 01ArC.ARCFreeArc compressed file
>
> 42 41 41 44BAADn/aNTFS Master File Table (MFT) entry (1,024 bytes)
>
> 42 44 69 63BDicBDICGoogle Chrome dictionary file
>
> 42 45 47 49 4E 3A 56 43
>
> 41 52 44 0D 0ABEGIN:VC
>
> ARD..VCFvCard file
>
> 42 4C 49 32 32 33BLI223BLI, RBIThomson Speedtouch series WLAN router firmware
>
> > **NOTES on BLI/RBI file headers:** The signature above is correct for the generic first six bytes.
> >
> > Reportedly, the 7th & 8th bytes vary by version, and the 9th byte is always 0x30.
> >
> > - v6.0.7.1 (.bli) — 0x42-4C-49-32-32-33-51-4B-30 (BLI223QK0)
> > - v7.4.1.7 (.bli) — 0x42-4C-49-32-32-33-51-48-30 (BLI223QH0)
> > - v8.2.2.5 (.bli) — 0x42-4C-49-32-32-33-55-46-30 (BLI223UF0)
> > - v8.4.3 (.bli/.rbi) — 0x42-4C-49-32-32-33-57-31-30 (BLI223W10)
>
> 42 4DBMBMP, DIBWindows (or device-independent) bitmap image
>
> **NOTE:** Bytes 2-5 contain the file length in little-endian order.
>
> 42 4F 4F 4B 4D 4F 42 49BOOKMOBIPRCPalmpilot resource file
>
> 42 50 47 FBBPG#xFB;BPG[Better Portable Graphics](http://bellard.org/bpg/) image format
>
> 42 5A 68BZhBZ2, TAR.BZ2, TBZ2, TB2[bzip2](http://en.wikipedia.org/wiki/Bzip) compressed archiveDMG Mac Disk image (BZ2 compressed)
>
> 42 65 67 69 6E 20 50 75
>
> 66 66 65 72 20 44 61 74
>
> 61 0D 0ABegin Pu
>
> ffer Dat
>
> a..APUF[Puffer](http://www.briggsoft.com/puffer.htm) ASCII-armored encrypted archive
>
> 42 6C 69 6E 6B 20 62 79
>
> 20 44 2E 54 2E 53Blink by
>
>  D.T.SBLIBLINK compressed archive
>
> 43 23 2B 44 A4 43 4D A5
>
> 48 64 72C#+D¤CM¥
>
> HdrRTDRagTime document file
>
> 43 41 54 20CAT IFFElectronic Arts' [Interchange Format Files (IFF)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000115.shtml) format.
>
> 43 42 46 49 4C 45CBFILECBDWordPerfect dictionary file (unconfirmed)
>
> 43 44 30 30 31CD001ISOISO-9660 CD Disc Image
>
> This signature usually occurs at byte offset 32769 (0x8001),
>
> 34817 (0x8801), or 36865 (0x9001).
>
> More information can be found at [MacTech](http://www.mactech.com/articles/develop/issue_03/high_sierra.html) or at [ECMA](http://www.ecma-international.org/publications/files/ECMA-ST/Ecma-119.pdf).
>
> 43 49 53 4FCISOCSOCompressed ISO (CISO) CD image
>
> 43 4D 4D 4D 15 00 00 00CMMM....DBWindows 7 thumbcache\_sr.db or other thumbcache file
>
> (except thumbcache\_idx.db)
>
> 43 4D 58 31CMX1CLBCorel Binary metafile
>
> 43 4F 4D 2BCOM+CLBCOM+ Catalog file
>
> 43 4F 57 44COWDVMDKVMware 3 Virtual Disk (portion of a split disk) file
>
> 43 50 54 37 46 49 4C 45CPT7FILECPTCorel Photopaint file
>
> 43 50 54 46 49 4C 45CPTFILECPTCorel Photopaint file
>
> 43 52 45 47CREGDATWindows 9x registry hive
>
> 43 52 55 53 48 20 76CRUSH vCRUCrush compressed archive
>
> 43 57 53CWSSWFMacromedia Shockwave Flash player file (zlib compressed, SWF 6 and later).
>
> See [SWF File Format Specification](https://www.adobe.com/content/dam/acom/en/devnet/pdf/swf-file-format-spec.pdf).
>
> 43 61 6C 63 75 6C 75 78
>
> 20 49 6E 64 6F 6F 72 20Calculux
>
>  Indoor CINCalculux Indoor lighting design software project file
>
> 43 61 74 61 6C 6F 67 20
>
> 33 2E 30 30 00Catalog
>
> 3.00.CTFWhereIsIt Catalog file
>
> 43 6C 69 65 6E 74 20 55
>
> 72 6C 43 61 63 68 65 20
>
> 4D 4D 46 20 56 65 72 20Client U
>
> rlCache
>
> MMF Ver DATMicrosoft Internet Explorer cache file ( [index.dat](http://sourceforge.net/projects/odessa/files/ODESSA/White%20Papers/IE_Internet_Activity_Reconstruction.pdf/download)) file
>
> 43 72 32 34Cr24CRXGoogle Chrome Extension
>
> 43 72 4F 44CrODCRXGoogle Chromium patch update
>
> 43 72 65 61 74 69 76 65
>
> 20 56 6F 69 63 65 20 46Creative
>
>  Voice FVOCCreative Voice audio file
>
> 44 41 41 00 00 00 00 00DAA.....DAAPowerISO Direct-Access-Archive image
>
> 44 41 58 00DAX.DAXDAX Compressed CD image
>
> 44 42 46 48DBFHDBPalm Zire photo database
>
> 44 4D 53 21DMS!DMSAmiga DiskMasher compressed archive
>
> 44 4F 53DOSADFAmiga disk file
>
> 44 53 44 20DSD DSF[DSD Storage Facility](http://dsd-guide.com/sites/default/files/white-papers/DSFFileFormatSpec_E.pdf) audio file
>
> 44 53 54 62DSTbDSTDST compressed file
>
> 44 56 44DVDDVRDVR-Studio stream fileIFODVD info file
>
> 45 4C 49 54 45 20 43 6F
>
> 6D 6D 61 6E 64 65 72 20ELITE Co
>
> mmander CDRElite Plus Commander saved game file
>
> 45 4E 54 52 59 56 43 44
>
> 02 00 00 01 02 00 18 58ENTRYVCD
>
> .......XVCDVideoVCD (GNU VCDImager) file
>
> 45 52 02 00 00CD...ISOApple ISO 9660/HFS hybrid CD image
>
> 45 52 46 53 53 41 56 45
>
> 44 41 54 41 46 49 4C 45ERFSSAVE
>
> DATAFILEDATKroll EasyRecovery Saved Recovery State file
>
> 45 50EPMDIMicrosoft Document Imaging file
>
> 45 56 46 09 0D 0A FF 00EVF...ÿ.E _nn_ (where _nn_ are numbers)Expert Witness Compression Format (EWF) file, including EWF-E01
>
> and EWF-S01, as used in EnCase and SMART evidence files. Byte
>
> offset 9 (i.e., byte #10) contains the segment number, starting with 0x01.
>
> See the [EWF specification](http://www.forensicswiki.org/wiki/ASR_Data%27s_Expert_Witness_Compression_Format).
>
> 45 56 46 32 0D 0A 81EVF2...Ex _nn_ (where _nn_ are numbers)EnCase® Evidence File Format Version 2 (Ex01).
>
> See the [EVFv2 specification](http://www.guidancesoftware.com/DocumentRegistration.aspx?did=1000018246).
>
> 45 6C 66 46 69 6C 65 00ElfFile.EVTXWindows Vista event log file
>
> 45 86 00 00 06 00E†....QBBIntuit QuickBooks backup file
>
> 46 41 58 43 4F 56 45 52
>
> 2D 56 45 52 FAXCOVER
>
> -VERCPEMicrosoft Fax Cover Sheet
>
> 46 44 42 48 00FDBH.FDBFiasco database definition file
>
> 46 45 44 46FEDFSBV(Unknown file type)
>
> 46 49 4C 45FILEn/aNTFS Master File Table (MFT) entry (1,024 bytes)
>
> 46 4C 56 01FLV.FLVFlash video file
>
> 46 4F 52 4DFORMANM IFF ANIM (Amiga delta/RLE encoded bitmap animation) fileIFFElectronic Arts' [Interchange Format Files (IFF)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000115.shtml) format.
>
> 46 4F 52 4D 00FORM.AIFFAudio Interchange FileDAXDAKX Compressed Audio
>
> 46 57 53FWSSWFMacromedia Shockwave Flash player file (uncompressed). See
>
> [SWF File Format Specification](https://www.adobe.com/content/dam/acom/en/devnet/pdf/swf-file-format-spec.pdf).
>
> 46 72 6F 6D 20 20 20 **_or_**From 46 72 6F 6D 20 3F 3F 3F **_or_**From ???46 72 6F 6D 3A 20From: EMLA commmon file extension for e-mail files. Signatures shown here
>
> are for Netscape, Eudora, and a generic signature, respectively.
>
> EML is also used by Outlook Express and QuickMail.
>
> 47GTS, TSA, TSV[MPEG transport stream](https://en.wikipedia.org/wiki/MPEG_transport_stream) file. (This is not a lot to go on, but MPEG-2 Part 1
>
> Transport (MP2T) files are reportedly broken into 188-byte packets and the
>
> 0x47 byte is the sync byte, so should repeat every 188 bytes in the file.)
>
> 47 46 31 50 41 54 43 48GF1PATCHPATAdvanced Gravis Ultrasound patch file
>
> 47 49 46 38 37 61 **_or_**GIF87a47 49 46 38 39 61GIF89aGIFGraphics interchange format file
>
> **Trailer:** 00 3B (.;)
>
> 47 50 41 54GPATPATGIMP (GNU Image Manipulation Program) pattern file
>
> 47 52 49 42GRIBGRBGRIdded Binary or General Regularly-distributed Information in Binary file, commonly used in
>
> meteorology to store historical and forecast weather data
>
> 47 58 32GX2GX2Show Partner graphics file (not confirmed)
>
> 47 65 6E 65 74 65 63 20
>
> 4F 6D 6E 69 63 61 73 74Genetec
>
> OmnicastG64Genetec video archive
>
> 48 44 52 2A 50 6F 77 65
>
> 72 42 75 69 6C 64 65 72HDR\*Powe
>
> rBuilderPBDSAP PowerBuilder integrated development environment file
>
> 48 45 41 44 45 52 20 52
>
> 45 43 4F 52 44 2A 2A 2AHEADER R
>
> ECORD\*\*\*XPTSAS Transport dataset file format
>
> 48 48 47 42 31HHGB1SH3Harvard Graphics presentation file
>
> 49 20 49I ITIF, TIFFTagged Image File Format file
>
> 49 44 33ID3MP3MPEG-1 Audio Layer 3 (MP3) audio file
>
> 49 44 33 03 00 00 00ID3....KOZSprint Music Store audio file (for mobile devices)
>
> 49 49 1A 00 00 00 48 45
>
> 41 50 43 43 44 52 02 00II....HE
>
> APCCDR..CRW[Canon digital camera RAW file](http://www.sno.phy.queensu.ca/~phil/exiftool/canon_raw.html)
>
> 49 49 2A 00II\*.TIF, TIFFTagged Image File Format file (little
>
> endian, i.e., LSB first in the byte; Intel)
>
> 49 49 2A 00 10 00 00 00
>
> 43 52II\*.....
>
> CRCR2[Canon digital camera RAW file](http://lclevy.free.fr/cr2/)
>
> 49 4D 4D 4D 15 00 00 00IMMM....DBWindows 7 thumbcache\_idx.db file
>
> 49 53 63 28ISc(CAB, HDRInstall Shield v5.x or 6.x compressed file
>
> 49 54 4F 4C 49 54 4C 53ITOLITLSLITMicrosoft Reader eBook file
>
> 49 54 53 46ITSFCHI, CHMMicrosoft Compiled HTML Help File
>
> 49 6E 6E 6F 20 53 65 74
>
> 75 70 20 55 6E 69 6E 73
>
> 74 61 6C 6C 20 4C 6F 67
>
> 20 28 62 29Inno Set
>
> up Unins
>
> tall Log
>
>  Â (b)DATInno Setup Uninstall Log file
>
> 49 6E 74 65 72 40 63 74
>
> 69 76 65 20 50 61 67 65Inter@ct
>
> ive PageIPDInter@ctive Pager Backup (BlackBerry) backup file
>
> (See also this [IPD File Format](http://www.blackberry.com/developers/journal/jan_2006/ipd_file_format.shtml) paper)
>
> 4A 41 52 43 53 00JARCS.JARJARCS compressed archive
>
> 4A 47 03 0E **_or_**JG..4A 47 04 0EJG..ARTAOL ART file
>
> **Trailers:**
>
> For 0x4A-47-03-0E: D0 CB 00 00 (ÐË..)
>
> For 0x4A-47-04-0E: CF C7 CB (ÏÇË)
>
> 4B 44 4DKDMVMDKVMware 4 Virtual Disk (portion of a split disk) file
>
> 4B 44 4D 56KDMVVMDKVMware 4 Virtual Disk (monolitic disk) file
>
> 4B 47 42 5F 61 72 63 68
>
> 20 2DKGB\_arch
>
> Â -KGBKGB archive
>
> 4B 49 00 00KI..SHDWindows 9x printer spool file
>
> 4B 57 41 4A 88 F0 27 D1KWAJˆð'Ñn/aKWAJ file format used by DOS COMPRESS.EXE and EXPAND.EXE commands.
>
> This command compresses a single file, replacing the last character in the file name
>
> with an underscore or dollar sign, e.g., FOO.BAZ would be renamed FOO.BA\_ or
>
> FOO.BA$. (See the [SZDD/KWAJ](http://www.cabextract.org.uk/libmspack/doc/szdd_kwaj_format.html) page for more information.)
>
> 4C 00 00 00 01 14 02 00L.......LNK[Windows shell link (shortcut) file](http://msdn.microsoft.com/en-us/library/dd871305). See also [_The Meaning of Linkfiles in Forensic Examinations_](http://computerforensics.parsonage.co.uk/downloads/TheMeaningofLIFE.pdf)
>
> and [Evidentiary Value of Link Files](http://www.forensicfocus.com/link-file-evidentiary-value).
>
> 4C 01L.OBJMicrosoft [Common Object File Format (COFF)](http://www.microsoft.com/whdc/system/platform/firmware/PECOFF.mspx) relocatable
>
> object code file for an Intel 386 or later/compatible processors
>
> 4C 41 3ALA:DSTTajima embroidery sticj image file
>
> 4C 49 53 54LISTIFFElectronic Arts' [Interchange Format Files (IFF)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000115.shtml) format.
>
> 4C 4E 02 00LN..GIDWindows Help index fileHLPWindows Help file
>
> 4C 50 46 20 00 01LPF ..ANMDeluxePaint Animation file
>
> 4C 56 46 09 0D 0A FF 00LVF...ÿ.E _nn_ (where _nn_ are numbers)Logical File Evidence Format (EWF-L01) as used in later versions of
>
> EnCase evidence files. See the [EWF specification](https://github.com/libyal/libewf/blob/master/documentation/Expert%20Witness%20Compression%20Format%20(EWF).asciidoc).
>
> 4D 2D 57 20 50 6F 63 6B
>
> 65 74 20 44 69 63 74 69M-W Pock
>
> et DictiPDBMerriam-Webster Pocket Dictionary file
>
> 4D 41 52 31 00MAR1.MARMozilla archive
>
> 4D 41 52 43MARCMARMicrosoft/MSN MARC archive
>
> 4D 41 54 4C 41 42 20 35
>
> 2E 30 20 4D 41 54 2D 66
>
> 69 6C 65MATLAB 5
>
> .0 MAT-f
>
> ileMATMATLAB v5 workspace file (includes creation timestamp)
>
> 4D 41 72 30 00MAr0.MARMAr compressed archive
>
> 4D 43 57 20 54 65 63 68
>
> 6E 6F 67 6F 6C 69 65 73MCW Tech
>
> nogoliesMTETargetExpress target file
>
> 4D 44 4D 50 93 A7MDMP“§HDMPWindows heap dump fileDMPWindows minidump file
>
> 4D 49 4C 45 53MILESMLSMilestones v1.0 project management and scheduling software
>
> (Also see "MV2C" and "MV214" signatures)
>
> 4D 4C 53 57MLSWMLSSkype localization data file
>
> 4D 4D 00 2AMM.\*TIF, TIFFTagged Image File Format file (big
>
> endian, i.e., LSB last in the byte; Motorola)
>
> 4D 4D 00 2BMM.+TIF, TIFFBigTIFF files; Tagged Image File Format files >4 GB
>
> 4D 4D 4D 44 00 00MMMD..MMFYamaha Corp. Synthetic music Mobile Application Format (SMAF)
>
> for multimedia files that can be played on hand-held devices.
>
> 4D 52 56 4EMRVNNVRAMVMware BIOS (non-volatile RAM) state file
>
> 4D 53 43 46MSCFCABMicrosoft cabinet fileONEPKG[OneNote Package file](https://blogs.msdn.microsoft.com/descapa/2006/09/07/other-onenote-file-types-onenote-package-table-of-contents/)PPZPowerpoint Packaged PresentationSNPMicrosoft Access Snapshot Viewer file
>
> 4D 53 46 54 02 00 01 00MSFT....TLBOLE, SPSS, or Visual C++ type library file
>
> 4D 53 48 7C 5E 7E 5C 26
>
> 7CMSH\|^~\\&
>
> \|HL7Health Level-7 data (pipe delimited) file
>
> 4D 53 57 49 4DMSWIMWIMMicrosoft Windows Imaging Format file
>
> 4D 53 5F 56 4F 49 43 45MS\_VOICECDR, DVFSony Compressed Voice FileMSVSony Memory Stick Compressed Voice file
>
> 4D 54 68 64MThdMID, MIDIMusical Instrument Digital Interface (MIDI) sound filePCSYamaha Piano sound file
>
> 4D 56MVDSNCD Stomper Pro label file
>
> 4D 56 32 31 34MV214MLSMilestones v2.1b project management and scheduling software
>
> (Also see "MILES" and "MV2C" signatures)
>
> 4D 56 32 43MV2CMLSMilestones v2.1a project management and scheduling software
>
> (Also see "MILES" and "MV214" signatures)
>
> 4D 5AMZCOM, DLL, DRV, EXE, PIF, QTS, QTX, SYSWindows/DOS executable file
>
> (See [The MZ EXE File Format](http://www.fileformat.info/format/exe/corion-mz.htm) page for the structure of an EXE file,
>
> with coverage of NE, TLINK, PE, self-extracting archives, and more.)
>
> **Note:** MZ are the initals of Mark Zbikowski, designer of the DOS executable file format.ACMMS audio compression manager driverAXLibrary cache fileCPLControl panel applicationFONFont fileOCXActiveX or OLE Custom ControlOLBOLE object librarySCRScreen saverVBXVisualBASIC applicationVXD, 386Windows virtual device drivers
>
> 4D 5A 90 00 03 00 00 00MZ......APIAcrobat plug-inAXDirectShow filterFLTAudition graphic filter file (Adobe)
>
> 4D 5A 90 00 03 00 00 00
>
> 04 00 00 00 FF FFMZ......
>
> ....ÿÿZAPZoneAlam data file
>
> 4D 69 63 72 6F 73 6F 66
>
> 74 20 43 2F 43 2B 2B 20Microsof
>
> t C/C++ PDBMicrosoft C++ debugging symbols file
>
> 4D 69 63 72 6F 73 6F 66
>
> 74 20 56 69 73 75 61 6C
>
> 20 53 74 75 64 69 6F 20
>
> 53 6F 6C 75 74 69 6F 6E
>
> 20 46 69 6C 65Microsof
>
> t Visual
>
>  Â Studio
>
> Solution
>
>  Â FileSLNVisual Studio .NET Solution file
>
> [84 (0x54) byte offset]
>
> 4D 69 63 72 6F 73 6F 66
>
> 74 20 57 69 6E 64 6F 77
>
> 73 20 4D 65 64 69 61 20
>
> 50 6C 61 79 65 72 20 2D
>
> 2D 20[84 (0x54) byte offset]
>
> Microsof
>
> t Window
>
> s Media
>
> Player -
>
> \- WPLWindows Media Player playlist
>
> 4D 73 52 63 66MsRcfGDBVMapSource GPS Waypoint Database
>
> 4E 41 56 54 52 41 46 46
>
> 49 43NAVTRAFF
>
> ICDATTomTom traffic data file
>
> 4E 42 2A 00NB\*.JNT, JTPMS Windows journal file
>
> 4E 45 53 4D 1A 01NESM..NSFNES Sound file
>
> 4E 49 54 46 30NITF0NTFNational Imagery Transmission Format (NITF) file
>
> 4E 61 6D 65 3A 20Name: CODAgent newsreader character map file
>
> 4F 50 43 4C 44 41 54OPCLDATattachment1Password 4 Cloud Keychain encrypted attachment
>
> 4F 50 4C 44 61 74 61 62
>
> 61 73 65 46 69 6C 65OPLDatab
>
> aseFileDBFPsion Series 3 Database file
>
> 4F 54 54 4F 00OTTO.OTFOpenType font file
>
> 4F 67 67 53 00 02 00 00
>
> 00 00 00 00 00 00OggS....
>
> ......OGA, OGG, OGV, OGXOgg Vorbis Codec compressed Multimedia file
>
> 4F 7BO{DW4Visio/DisplayWrite 4 text file (unconfirmed)
>
> 50 00 00 00 20 00 00 00P... ...IDXQuicken QuickFinder Information File
>
> 50 35 0AP5.PGMPortable Graymap Graphic
>
> 50 41 43 4BPACKPAKQuake archive file
>
> 50 41 47 45 44 55 36 34PAGEDU64DMPWindows 64-bit memory dump
>
> 50 41 47 45 44 55 4D 50PAGEDUMPDMPWindows memory dump
>
> 50 41 58PAXPAXPAX password protected bitmap
>
> 50 45 53 54PESTDATPestPatrol data/scan strings
>
> 50 47 50 64 4D 41 49 4EPGPdMAINPGDPGP disk image
>
> 50 49 43 54 00 08PICT..IMGADEX Corp. ChromaGraph Graphics Card Bitmap Graphic file
>
> 50 4B 03 04PK..ZIPPKZIP archive file ( [Ref. 1](http://members.tripod.com/~petlibrary/ZIP.HTM) \| [Ref. 2](http://www.pkware.com/documents/casestudies/APPNOTE.TXT))
>
> **Trailer:** _filename_ 50 4B _17 characters_ 00 00 00
>
> **Trailer:** ( _filename_ PK _17 characters_...)
>
> **Note:** PK are the initals of Phil Katz, co-creator of the ZIP file format and author of PKZIP.ZIPApple Mac OS X Dashboard Widget, Aston Shell theme, Oolite eXpansion Pack,
>
> Opera Widget, Pivot Style Template, Rockbox Theme package, Simple Machines
>
> Forums theme, SubEthaEdit Mode, Trillian zipped skin, Virtual Skipper skinAPKAndroid packageJARJava archive; compressed file package for classes and dataKMZGoogle Earth saved working session fileKWDKWord documentODT, ODP, OTTOpenDocument text document, presentation, and text document template, respectively.OXPSMicrosoft Open XML paper specification fileSXC, SXD, SXI, SXWOpenOffice spreadsheet (Calc), drawing (Draw), presentation (Impress),
>
> and word processing (Writer) files, respectively.SXCStarOffice spreadsheetWMZWindows Media compressed skin fileXPIMozilla Browser ArchiveXPSXML paper specification fileXPTeXact Packager Models
>
> 50 4B 03 04 0A 00 02 00PK......EPUBOpen Publication Structure eBook file. (Should also include the string:
>
> mimetypeapplication/epub+zip)
>
> 50 4B 03 04 14 00 01 00
>
> 63 00 00 00 00 00PK......
>
> c.....ZIPZLock Pro encrypted ZIP
>
> 50 4B 03 04 14 00 06 00PK......DOCX, PPTX, XLSXMicrosoft Office Open XML Format (OOXML) Document
>
> **NOTE:** There is no subheader for MS OOXML files as there is with
>
> DOC, PPT, and XLS files. To better understand the format of these files,
>
> rename any OOXML file to have a .ZIP extension and then unZIP the file;
>
> look at the resultant file named _[Content\_Types].xml_ to see the content
>
> types. In particular, look for the _<Override PartName=_ tag, where you
>
> will find _word_, _ppt_, or _xl_, respectively.
>
> **Trailer:** Look for 50 4B 05 06 (PK..) followed by 18 additional bytes
>
> at the end of the file.
>
> 50 4B 03 04 14 00 08 00
>
> 08 00PK......
>
> ..JARJava archive
>
> 50 4B 05 06PK..ZIPPKZIP empty archive file
>
> 50 4B 07 08PK..ZIPPKZIP multivolume archive file
>
> [30 (0x1E) byte offset]
>
> 50 4B 4C 49 54 45[30 (0x1E) byte offset]
>
> PKLITEZIPPKLITE compressed ZIP archive (see also PKZIP)
>
> [526 (0x20E) byte offset]
>
> 50 4B 53 70 58[526 (0x20E) byte offset]
>
> PKSFXZIPPKSFX self-extracting executable compressed file (see also PKZIP)
>
> 50 4D 43 43PMCCGRPWindows Program Manager group file
>
> 50 4E 43 49 55 4E 44 4FPNCIUNDODATNorton Disk Doctor undo file
>
> 50 4D 4F 43 43 4D 4F 43PMOCCMOCDATMicrosoft® Windows® User State Migration Tool (USMT). [USMT 3.0](http://technet.microsoft.com/en-us/library/cc722032%28v=ws.10%29.aspx)
>
> applies to Windows XP and Windows Vista®, and [USMT 4.0](http://technet.microsoft.com/en-us/library/dd560801.aspx) is for Windows 7.
>
> 50 53 46 12PSF.DSF Dreamcast Sound Format file, a subset of the [Portable Sound Format](https://en.wikipedia.org/wiki/Portable_Sound_Format).
>
> 50 55 46 58PUFXPUF[Puffer](http://www.briggsoft.com/puffer.htm) encrypted archive
>
> 50 61 56 45PaVEn/aParrot Video Encapsulation file
>
> [92 (0x5C) byte offset]
>
> 51 45 4C 20[92 (0x5C) byte offset]
>
> QEL QELQuicken data file
>
> 51 46 49 FBQFIûIMGQEMU Qcow Disk Image
>
> 51 57 20 56 65 72 2E 20QW Ver. ABD, QSDQuicken data file
>
> [512 (0x200) byte offset]
>
> 52 00 6F 00 6F 00 74 00
>
> 20 00 45 00 6E 00 74 00
>
> 72 00 79 00[512 (0x200) byte offset]
>
> R.o.o.t.
>
>  .E.n.t.
>
> r.y.MSGOutlook/Exchange message subheader (MS Office)
>
> 52 41 5A 41 54 44 42 31RAZATDB1DATShareaza (Windows P2P client) thumbnail
>
> 52 44 58 32 0ARDX2.RDATAR (programming language) saved work space
>
> 52 45 47 45 44 49 54REGEDITREG, SUDWindows NT Registry and Registry Undo files
>
> 52 45 56 4E 55 4D 3A 2CREVNUM:,ADFAntenna data file
>
> 52 49 46 46RIFFANIWindows animated cursorCMXCorel Presentation Exchange (Corel 10 CMX) MetafileCDRCorelDraw documentDATVideo CD MPEG or MPEG1 movie fileDS4Micrografx Designer v4 graphic file4XM4X Movie video
>
> 52 49 46 46 xx xx xx xx
>
> 41 56 49 20 4C 49 53 54RIFF....
>
> AVI LISTAVIResource Interchange File Format -- [Windows Audio Video\
> \
> Interleave file](http://msdn.microsoft.com/en-us/library/aa931363.aspx), where _xx xx xx xx_ is the file size (little endian)
>
> 52 49 46 46 xx xx xx xx
>
> 43 44 44 41 66 6D 74 20RIFF....
>
> CDDAfmt CDAResource Interchange File Format -- Compact Disc Digital
>
> Audio (CD-DA) file, where _xx xx xx xx_ is the file size (little endian)
>
> 52 49 46 46 xx xx xx xx
>
> 51 4C 43 4D 66 6D 74 20RIFF....
>
> QLCMfmt QCPResource Interchange File Format -- Qualcomm
>
> PureVoice, where _xx xx xx xx_ is the file size (little endian)
>
> 52 49 46 46 xx xx xx xx
>
> 52 4D 49 44 64 61 74 61RIFF....
>
> RMIDdataRMIResource Interchange File Format -- [Windows Musical\
> \
> Instrument Digital Interface file](http://www.digitalpreservation.gov/formats/fdd/fdd000120.shtml), where _xx xx xx xx_ is the file
>
> size (little endian)
>
> 52 49 46 46 xx xx xx xx
>
> 57 41 56 45 66 6D 74 20RIFF....
>
> WAVEfmt WAVResource Interchange File Format -- [Audio for Windows\
> \
> file](http://www-mmsp.ece.mcgill.ca/Documents/AudioFormats/WAVE/WAVE.html), where _xx xx xx xx_ is the file size (little endian)
>
> 52 49 46 46 xx xx xx xx
>
> 57 45 42 50RIFF....
>
> WEBPWEBPGoogle [WebP image file](https://developers.google.com/speed/webp/docs/riff_container), where _xx xx xx xx_ is the file size
>
> 52 54 53 53RTSSCAPWindows NT Netmon capture file
>
> 52 61 72 21 1A 07 00Rar!...RARRAR (v4.x) compressed archive file
>
> 52 61 72 21 1A 07 01 00Rar!....RAR[RAR (v5)](http://www.rarlab.com/technote.htm) compressed archive file
>
> 52 65 74 75 72 6E 2D 50
>
> 61 74 68 3A 20Return-P
>
> ath: EMLA commmon file header for e-mail files.
>
> [4 byte offset]
>
> 53 43 43 41[4 byte offset]
>
> SCCAPF[Windows prefetch file](http://www.forensicswiki.org/wiki/Windows_Prefetch_File_Format). The first four bytes indicate the OS:
>
> 0x11-00-00-00 = XP, 0x17-00-00-00 = Vista/Win7,
>
> and 0x1A-00-00-00 = Win8.1 (and probably Win8, as well).
>
> 53 43 48 6CSCHlASTNeed for Speed: Underground Audio file
>
> 53 43 4D 49SCMIIMGImg Software Set Bitmap
>
> 53 44 50 58SDPXDPXSociety of Motion Picture and Television Engineers (SMPTE)
>
> Digital Picture Exchange (DPX) image file (big endian)
>
> 53 48 4F 57SHOWSHWHarvard Graphics DOS Ver. 2/x Presentation file
>
> 53 49 45 54 52 4F 4E 49
>
> 43 53 20 58 52 44 20 53
>
> 43 41 4ESIETRONI
>
> CS XRD S
>
> CANCPISietronics CPI XRD document
>
> 53 49 4D 50 4C 45 20 20
>
> 3D 20 20 20 20 20 20 20
>
> 20 20 20 20 20 20 20 20
>
> 20 20 20 20 20 54
> SIMPLE
>
> =
>
> Â  Â  Â TFITS[Flexible Image Transport System (FITS), Version 3.0](http://www.digitalpreservation.gov/formats/fdd/fdd000317.shtml) file
>
> 53 49 54 21 00SIT!.SITStuffIt compressed archive
>
> 53 4D 41 52 54 44 52 57SMARTDRWSDRSmartDraw Drawing file
>
> 53 50 46 49 00SPFI.SPFStorageCraft ShadownProtect backup file
>
> 53 50 56 42SPVBSPVCHAINMultiBit Bitcoin blockchain file
>
> 53 51 4C 4F 43 4F 4E 56
>
> 48 44 00 00 31 2E 30 00SQLOCONV
>
> HD..1.0.CNVDB2 conversion file
>
> 53 51 4C 69 74 65 20 66
>
> 6F 72 6D 61 74 20 33 00SQLite f
>
> ormat 3.DBSQLite database file
>
> 53 5A 20 88 F0 27 33 D1SZ ˆð'3Ñn/aQBASIC SZDD file header variant. (See the SZDD or KWAJ format entries
>
> for additional information.)
>
> 53 5A 44 44 88 F0 27 33SZDDˆð'3n/aSZDD file format used by DOS COMPRESS.EXE and EXPAND.EXE commands.
>
> This command compresses a single file, replacing the last character in the file name
>
> with an underscore or dollar sign, e.g., FOO.BAZ would be renamed FOO.BA\_ or
>
> FOO.BA$. (See the [SZDD/KWAJ](http://www.cabextract.org.uk/libmspack/doc/szdd_kwaj_format.html) page for more information.)
>
> 53 6D 62 6CSmblSYM(Unconfirmed file type. Likely type is Harvard Graphics
>
> Version 2.x graphic symbol or Windows SDK graphic symbol)
>
> 53 74 75 66 66 49 74 20
>
> 28 63 29 31 39 39 37 2DStuffIt
>
> (c)1997-SITStuffIt compressed archive
>
> 53 75 70 65 72 43 61 6C
>
> 63SuperCal
>
> cCALSuperCalc worksheet
>
> 54 48 50 00THP.THP[Wii/GameCube video](http://www.amnoid.de/gc/thp.txt) file
>
> 54 68 69 73 20 69 73 20This isINFOUNIX GNU Info Reader File
>
> 55 43 45 58UCEXUCEUnicode extensions
>
> 55 46 41 C6 D2 C1UFAÆÒÁUFAUFA compressed archive
>
> 55 46 4F 4F 72 62 69 74UFOOrbitDATUFO Capture v2 map file
>
> 55 6E 46 69 6E 4D 46UnFinMFMF4Unfinalized [Measurement Data Format (MDF)](https://www.asam.net/standards/detail/mdf/) file
>
> 56 43 50 43 48 30VCPCH0PCHVisual C PreCompiled header file
>
> 56 45 52 53 49 4F 4E 20VERSION CTLVisual Basic User-defined Control file
>
> 56 65 72 73 69 6F 6E 20Version MIFMapInfo Interchange Format file
>
> 57 04 00 00 53 50 53 53
>
> 20 74 65 6D 70 6C 61 74W...SPSS
>
>  templatSCTSPSS Statistics (née Statistical Package for the Social Sciences, then
>
> Statistical Product and Service Solutions) template file
>
> 57 4D 4D 50WMMPDATWalkman MP3 container file
>
> 57 53 32 30 30 30WS2000WS2WordStar for Windows Ver. 2 document
>
> [29,152 (0x71E0) byte offset]
>
> 57 69 6E 5A 69 70[29,152 (0x71E0) byte offset]
>
> WinZipZIPWinZip compressed archive
>
> 57 6F 72 64 50 72 6FWordProLWPLotus WordPro document.
>
> 58 2DX-EMLA commmon file extension for e-mail files. This variant is
>
> for Exchange.
>
> 58 43 50 00XCP.CAPCinco NetXRay, Network General Sniffer, and
>
> Network Associates Sniffer capture file
>
> 58 50 43 4F 4D 0A 54 79
>
> 70 65 4C 69 62XPCOM.Ty
>
> peLibXPTXPCOM type libraries for the XPIDL compiler
>
> 58 50 44 53XPDSDPXSociety of Motion Picture and Television Engineers (SMPTE)
>
> Digital Picture Exchange (DPX) image file (little endian)
>
> 58 54XT..BDRMS Publisher border
>
> 5A 4F 4F 20ZOO ZOOZOO compressed archive
>
> 5A 57 53ZWSSWFMacromedia Shockwave Flash player file (LZMA compressed, SWF 13 and later).
>
> See [SWF File Format Specification](https://www.adobe.com/content/dam/acom/en/devnet/pdf/swf-file-format-spec.pdf).
>
> 5B 47 65 6E 65 72 61 6C
>
> 5D 0D 0A 44 69 73 70 6C
>
> 61 79 20 4E 61 6D 65 3D
>
> 3C 44 69 73 70 6C 61 79
>
> 4E 61 6D 65[General
>
> ]..Displ
>
> ay Name=
>
> <Display
>
> NameECFMS Exchange 2007 extended configuration file
>
> 5B 4D 53 56 43[MSVCVCWMicrosoft Visual C++ Workbench Information File
>
> 5B 50 68 6F 6E 65 5D[Phone]DUNDial-up networking file
>
> 5B 56 45 52 5D **_or_**[VER]5B 76 65 72 5D **_or_**[ver]SAMLotus AMI Pro document
>
> 5B 56 4D 44 5D **_or_**[VMD]VMDVocalTec VoIP media file
>
> [2 byte offset]
>
> 5B 56 65 72 73 69 6F 6E[2 byte offset]
>
> [VersionCIF(Unknown file type)
>
> 5B 57 69 6E 64 6F 77 73
>
> 20 4C 61 74 69 6E 20[Windows
>
>  Â Latin CPXMicrosoft Code Page Translation file
>
> 5B 66 6C 74 73 69 6D 2E
>
> 30 5D[fltsim.
>
> 0]CFGFlight Simulator Aircraft Configuration file
>
> 5B 70 6C 61 79 6C 69 73
>
> 74 5D[playlis
>
> t]PLSWinAmp Playlist file
>
> 5D FC C8 00]üÈ.HUSHusqvarna Designer I Embroidery Machine file
>
> 5F 27 A8 89\_'¨‰JARJar archive
>
> 5F 43 41 53 45 5F\_CASE\_CAS, CBKEnCase case file (and backup)
>
> 60 EA\`êARJCompressed archive file
>
> 62 65 67 69 6Ebeginn/aUUencoded files start with a string:
>
>  Â  begin _mode path_
>
> where _mode_ is the set of permissions as used in
>
> Linux/Unix and _path_ is the name given to the decoded
>
> file. (See this [uuencode](http://www.mkssoftware.com/docs/man4/uuencode.4.asp) page for more information.)
>
> 62 65 67 69 6E 2D 62 61
>
> 73 65 36 34begin-ba
>
> se64b64UUencoded BASE64 file
>
> **Trailer:** 0A 3D 3D 3D 3D 0A (.====.)
>
> 62 70 6C 69 73 74bplistplistBinary property list (plist)
>
> (NOTE: Next two bytes are the version number, currently
>
> 0x30-30, or "00")
>
> 63 61 66 66
> caffCAF[Apple Core Audio File](https://developer.apple.com/library/mac/documentation/musicaudio/Reference/CAFSpec/CAF_intro/CAF_intro.html)
>
> 63 64 73 61 65 6E 63 72cdsaencrDMGMacintosh encrypted Disk image (v1)
>
> 63 6F 6E 65 63 74 69 78
> conectixVHD[Virtual PC Virtual HD image](https://github.com/libyal/libvhdi/blob/main/documentation/Virtual%20Hard%20Disk%20(VHD)%20image%20format.asciidoc)
>
> 63 75 73 68 00 00 00 02
>
> 00 00 00cush....
>
> ...CSHPhotoshop Custom Shape
>
> 64 00 00 00d...P10Intel PROset/Wireless Profile
>
> 64 38 3A 61 6E 6E 6F 75
>
> 6E 63 65d8:annou
>
> nceTORRENTTorrent file
>
> 64 65 78 0Adex.dexDalvik executable file (Android)
>
> 64 6E 73 2Edns.AUAudacity audio file
>
> 64 73 77 66 69 6C 65dswfileDSWMicrosoft Visual Studio workspace file
>
> 65 6E 63 72 63 64 73 61encrcdsaDMGMacintosh encrypted Disk image (v2)
>
> 66 49 00 00fI..SHDWindows NT printer spool file
>
> 66 4C 61 43 00 00 00 22fLaC..."FLACFree Lossless Audio Codec file
>
> [4 byte offset]
>
> 66 74 79 70 33 67 70[4 byte offset]
>
> ftyp3gp3GG, 3GP, 3G23rd Generation Partnership Project 3GPP multimedia files
>
> [4 byte offset]
>
> 66 74 79 70 4D 34 41 20[4 byte offset]
>
> ftypM4A M4AApple Lossless Audio Codec file
>
> [4 byte offset]
>
> 66 74 79 70 4D 34 56 20[4 byte offset]
>
> ftypM4V FLV, M4VISO Media, MPEG v4 system, or iTunes AVC-LC file
>
> [4 byte offset]
>
> 66 74 79 70 4D 53 4E 56[4 byte offset]
>
> ftypMSNVMP4MPEG-4 video file
>
> [4 byte offset]
>
> 66 74 79 70 69 73 6F 6D[4 byte offset]
>
> ftypisomMP4ISO Base Media file (MPEG-4) v1
>
> [4 byte offset]
>
> 66 74 79 70 6D 70 34 32[4 byte offset]
>
> ftypmp42M4VMPEG-4 video\|QuickTime file
>
> [4 byte offset]
>
> 66 74 79 70 71 74 20 20[4 byte offset]
>
> ftypqt MOVQuickTime movie file
>
> 67 49 00 00gI..SHDWindows 2000/XP printer spool file
>
> 67 69 6d 70 20 78 63 66
>
> 20gimp xcf
>
> XCFGNU Image Manipulation Program (GIMP) eXperimental Computing Facility (XCF)
>
> image file
>
> 68 49 00 00hI..SHDWindows Server 2003 printer spool file
>
> 69 63 6E 73icnsICNSMacOS icon file
>
> 6C 33 33 6Cl33lDBBSkype user data file (profile and contacts)
>
> [4 byte offset]
>
> 6D 6F 6F 76[4 byte offset]
>
> moovMOVQuickTime movie file
>
> > .MOV files have a complicated file signature. The string "moov" is the most common but I have also seen:
> >
> >  Â  0x66-72-65-65 Â  free
> >
> >  Â  0x6D-64-61-74 Â  mdat
> >
> >  Â  0x77-69-64-65 Â  wide
> >
> > And the following have been reported to me:
> >
> >  Â  0x70-6E-6F-74 Â  pnot
> >
> >  Â  0x73-6B-69-70 Â  skip
> >
> > Furthermore, if you look at byte position xxxxxxxx+4 (where xxxxxxxx is bytes 0-3 of the header), you
> >
> > will find one (or more!) of these strings repeated; the string "free" **seems** to be the most common. For
> >
> > more information, see the [QuickTime File Format](http://www.digitalpreservation.gov/formats/fdd/fdd000052.shtml) page. (Thanks to D. Wright for getting me started on this!)
>
> 6D 73 46 69 6C 74 65 72
>
> 4C 69 73 74msFilter
>
> ListTPLInternet Explorer v11 Tracking Protection List file
>
> 6D 75 6C 74 69 42 69 74
>
> 2E 69 6E 66 6FmultiBit
>
> .infoINFOMultiBit Bitcoin wallet information file
>
> 6F 3Co<n/aShort Message Service (SMS), or text, message stored on a
>
> Subscriber Identification Module (SIM).
>
> 6F 70 64 61 74 61 30 31opdata01n/a1Password 4 Cloud Keychain encrypted data
>
> 72 65 67 66regfDATWindows NT registry hive file
>
> 72 69 66 66riffACDSonic Foundry Acid Music File (Sony)
>
> 72 74 73 70 3A 2F 2Frtsp://RAMRealMedia metafile
>
> 73 6C 68 21 _**or**_slh!DATAllegro Generic Packfile Data file (compressed)
>
> 73 6C 68 2Eslh.DATAllegro Generic Packfile Data file (uncompressed)
>
> 73 6D 5Fsm\_PDBPalmOS SuperMemo file
>
> 73 6F 6C 69 64solidSTLASCII [STL (STereoLithography) file](https://en.wikipedia.org/wiki/STL_%28file_format%29) for 3D printing.
>
> 73 72 63 64 6F 63 69 64
>
> 3Asrcdocid
>
> :CALCALS raster bitmap file
>
> 73 7A 65 7AszezPDBPowerBASIC Debugger Symbols file
>
> [60 (0x3C) byte offset]
>
> 74 42 4D 50 4B 6E 57 72[60 (0x3C) byte offset]
>
> tBMPKnWrPRCPathWay Map file, used with GPS devices
>
> 74 72 75 65 00true.TTFTrueType font file
>
> [257 (0x101) byte offset]
>
> 75 73 74 61 72[257 (0x101) byte offset]
>
> ustarTARTape Archive file ( [http://www.mkssoftware.com/docs/man4/tar.4.asp](http://www.mkssoftware.com/docs/man4/tar.4.asp))
>
> 76 2F 31 01v/1.EXROpenEXR bitmap image format
>
> 76 32 30 30 33 2E 31 30
>
> 0D 0A 30 0D 0Av2003.10
>
> ..0..FLTQimage filter
>
> 77 4F 46 32wOF2WOFF2Web Open Font Format 2
>
> 77 4F 46 46wOFFWOFFWeb Open Font Format
>
> 78 01 73 0D 62 62 60x.s.bb\`DMGMac OS X Disk Copy Disk Image file
>
> 78 61 72 21xar!XAR[eXtensible ARchive](https://code.google.com/p/xar/wiki/xarformat) file
>
> 7A 62 65 78zbexINFOZoomBrowser Image Index file (ZbThumbnal.info)
>
> 7B 0D 0A 6F 20{..o LGC, LGDWindows application log
>
> 7B 22 75 72 6C 22 3A 20
>
> 22 68 74 74 70 73 3A 2F{"url":
>
> "https:/GDOCGoogle Drive Document link
>
> GDRAWGoogle Drive Drawing link
>
> 7B 5C 70 77 69{\\pwiPWIMicrosoft Windows Mobile personal note file
>
> 7B 5C 72 74 66{\\rtfRTFRich text format word processing file
>
> **Trailer:** 7D (})
>
> 7C 4B C3 74 E1 C8 53 A4
>
> 79 B9 01 1D FC 4F DD 13\|KÃtáÈS¤
>
> y¹..üOÝ.CSDHuskygram, Poem, or Singer embroidery design file
>
> 7E 42 4B 00~BK.PSPCorel Paint Shop Pro image file
>
> 7E 45 53 44 77 F6 85 3E
>
> BF 6A D2 11 45 61 73 79
>
> 20 53 74 72 65 65 74 20
>
> 44 72 61 77~ESDwö…>
>
> ¿jÒ.Easy
>
> Â Street
>
> DrawESDEasy Street Draw diagram file
>
> 7E 74 2C 01 50 70 02 4D
>
> 52 01 00 00 00 08 00 00
>
> 00 01 00 00 31 00 00 00
>
> 31 00 00 00 43 01 FF 00
>
> 01 00 08 00 01 00 00 00
>
> 7e 74 2c 01~t,.Pp.M
>
> R.......
>
> ....1...
>
> 1...C.ÿ.
>
> ........
>
> ~t,.IMGReportedly a proprietary recording system, possibly a
>
> Digital Watchdog DW-TP-500G unit.
>
> 7F 45 4C 46.ELFn/a[Executable and Linking Format executable file (Linux/Unix)](http://www.skyfree.org/linux/references/ELF_Format.pdf)
>
> 80.OBJRelocatable object code
>
> 80 00..ADX[ADX](https://en.wikipedia.org/wiki/ADX_(file_format)) lossy compressed audio file
>
> 80 2A 5F D7.\*\_.CINKodak Cineon image file
>
> 81 32 84 C1 85 05 D0 11
>
> B2 90 00 AA 00 3C F6 76.2„Á….Ð.
>
> ²..ª.<övWABOutlook Express address book (Win95)
>
> 81 CD AB.Í«WPFWordPerfect text file
>
> 86 DD 6x†Ý **{lower\_case letter}**n/aPossibly, maybe, might be a fragment of an Ethernet frame carrying
>
> an IPv6 packet. See [Hints About Looking for Network Packet Fragments](https://www.garykessler.net/library/netsig.html).
>
> 89 50 4E 47 0D 0A 1A 0A‰PNG....PNG[Portable Network Graphics file](http://www.libpng.org/pub/png/spec/)
>
> **Trailer:** 49 45 4E 44 AE 42 60 82 (IEND®B\`‚...)
>
> 8A 01 09 00 00 00 E1 08
>
> 00 00 99 19Š.....á.
>
> ..™.AWMS Answer Wizard file
>
> 91 33 48 46‘3HFHAPHamarsoft HAP 3.x compressed archive
>
> 95 00 **_or_**•.95 01•.SKRPGP secret keyring file
>
> 97 4A 42 32 0D 0A 1A 0A—JB2....JB2JBIG2 image file
>
> **Trailer:** 03 33 00 01 00 00 00 00 (.3......)
>
> 99™GPGGNU Privacy Guard (GPG) public keyring
>
> 99 01™.PKRPGP public keyring file
>
> 9C CB CB 8D 13 75 D2 11
>
> 91 58 00 C0 4F 79 56 A4œËË..UÒ.
>
> ‘X.ÀOyV¤WABOutlook address file
>
> [512 (0x200) byte offset]
>
> A0 46 1D F0[512 (0x200) byte offset]
>
> Â F.ðPPTPowerPoint presentation subheader (MS Office)
>
> A1 B2 C3 D4¡²ÃÔn/atcpdump (libpcap) capture file (Linux/Unix)
>
> A1 B2 CD 34¡²Í4n/aExtended tcpdump (libpcap) capture file (Linux/Unix)
>
> A9 0D 00 00 00 00 00 00©.......DATAccess Data FTK evidence file
>
> AB 4B 54 58 20 31 31 BB
>
> 0D 0A 1A 0A«KTX 11»
>
> ....KTX[Khronos texture file](https://www.khronos.org/opengles/sdk/tools/KTX/file_format_spec/) for OpenGL and OpenGL ES applications
>
> AC 9E BD 8F 00 00¬.½...QDFQuicken data file
>
> AC ED¬ín/aJava serialization data (see [Object Serialization Stream Protocol](http://java.sun.com/j2se/1.5.0/docs/guide/serialization/spec/protocol.html#10258))
>
> AC ED 00 05 73 72 00 12
>
> 62 67 62 6C 69 74 7A 2E¬í..sr..
>
> bgblitz.PDBBGBlitz (professional Backgammon software) position database file
>
> B0 4D 46 43°MFCPWLWindows 95 password file
>
> B1 68 DE 3A±hÞ:DCXGraphics Multipage PCX bitmap file
>
> B4 6E 68 44´nhdTIBAcronis True Image file (early versions)
>
> B5 A2 B0 B3 B3 B0 A5 B5µ¢°³³°¥µCALWindows calendar file
>
> B8 C9 0C 00¸É..INSInstallShield Script
>
> BE 00 00 00 AB 00 00 00
>
> 00 00 00 00 00¾...«...
>
> ....WRIMS Write file
>
> BE BA FE CA 0F 50 61 6C
>
> 6D 53 47 20 44 61 74 61¾ºþÊ.Pal
>
> mSG DataDATPalm Desktop DateBook file
>
> C3 AB CD ABÃ«Í«ACSMS Agent Character file
>
> C5 D0 D3 C6ÅÐÓÆEPSAdobe encapsulated PostScript file
>
> C8 00 79 00È.y.LBKJeppesen FliteLog file
>
> CA FE BA BEÊþº¾CLASSJava bytecode file (also used by Apple iOS apps)
>
> CC 52 33 FC E9 2C 18 48
>
> AF E3 36 30 1A 39 40 06ÌR3üé,.H
>
> ¯ã60.9@.NBUNokia phone backup file
>
> CD 20 AA AA 02 00 00 00Í ªª....n/aNorton Anti-Virus quarantined virus file
>
> CE 24 B9 A2 20 00 00 00Î$¹¢ ...TIBAcronis True Image file (current versions)
>
> CE CE CE CEÎÎÎÎJCEKS[Java Cryptography Extension keystore](https://zgrepcode.com/java/openjdk/10.0.2/java.base/com/sun/crypto/provider/jcekeystore.java) file
>
> CE FA ED FEÎúíþn/aApple [OS X ABI Mach-O](https://github.com/aidansteele/osx-abi-macho-file-format-reference/blob/master/Mach-O_File_Format.pdf) binary file (32-bit, where target system has reverse byte
>
> ordering from host running compiler)
>
> CF 11 E0 A1 B1 1A E1 00Ï.à¡±.á.DOCPerfect Office document
>
> [Note similarity to MS Office header, below]
>
> CF AD 12 FEÏ­.þDBXOutlook Express e-mail folder
>
> CF FA ED FEÏúíþn/aApple [OS X ABI Mach-O](https://github.com/aidansteele/osx-abi-macho-file-format-reference/blob/master/Mach-O_File_Format.pdf) binary file (64-bit, where target system has reverse byte
>
> ordering from host running compiler)
>
> D0 CF 11 E0 A1 B1 1A E1ÐÏ.à¡±.á[DOC](http://www.forensicswiki.org/wiki/Word_Document_%28DOC%29), DOT, PPS, [PPT](http://www.forensicswiki.org/wiki/Powerpoint_Presentation_%28PPT%29), XLA, [XLS](http://www.forensicswiki.org/wiki/Excel_Spreadsheet_%28XLS%29), WIZAn Object Linking and Embedding (OLE) Compound File (CF) (i.e., [OLECF](http://www.forensicswiki.org/wiki/OLE_Compound_File))
>
> file format, known as _Compound Binary File format_ by Microsoft, used by
>
> Microsoft Office 97-2003 applications (Word, Powerpoint, Excel, Wizard). Part of
>
> Microsoft's [Structured Storage (MSS)](https://docs.microsoft.com/en-us/windows/win32/stg/structured-storage-start-page) architecture for Component Object Model (COM)-based
>
> operating systems.
>
> [See also Excel, Outlook, PowerPoint, and Word "subheaders" at byte offset 512 (0x200).]
>
> - There appear to several subheader formats and a dearth of documentation.
> - There have been reports that there are different subheaders for Windows and Mac
>
>   versions of MS Office but I cannot confirm that.]
> - Password-protected DOCX, XLSX, and PPTX files also use this signature those files
>
>   are saved as OLECF files.
> - _[Note the similarity between D0 CF 11 E0 and the word "DOCFILE"!]_
>
> AC\_CaseWare Working Papers compressed client fileADPAccess project fileAPRLotus/IBM Approach 97 fileDBMSWorks database fileMSCMicrosoft Common Console DocumentMSGMicrosoft Outlook/Exchange MessageMSIMicrosoft Installer packageMSPWindows Installer PatchMTWMinitab data fileMXDArcMap GIS project fileOPTDeveloper Studio File Workspace Options filePUBMS Publisher fileQBMQuickBooks Portable Company FileRVTRevit Project fileSOUVisual Studio Solution User Options fileSPOSPSS output fileVSDVisio fileWPSMSWorks text document
>
> D2 0A 00 00Ò...FTRGN Nettest WinPharoah filter file
>
> D4 2AÔ\*ARL, AUTAOL history (ARL) and typed URL (AUT) files
>
> D4 C3 B2 A1ÔÃ²¡n/aWinDump (winpcap) capture file (Windows)
>
> D7 CD C6 9A×ÍÆšWMFWindows graphics metafile
>
> DB A5 2D 00Û¥-.DOCWord 2.0 file
>
> DC DCÜÜCPLCorel color palette file
>
> DC FEÜþEFXeFax file format
>
> E3 10 00 01 00 00 00 00ã.......INFOAmiga Icon file
>
> E3 82 85 96ã‚…–PWLWindows 98 password file
>
> E4 52 5C 7B 8C D8 A7 4D
>
> AE B1 53 78 D0 29 96 D3äR\\{ŒØ§M
>
> ®±SxÐ)–ÓONEMicrosoft OneNote note
>
> E8 **_or_**èE9 **_or_**éEBëCOM, SYSWindows executable file
>
> EB 3C 90 2Aë<.\*IMGGEM Raster file
>
> EB 52 90 2D 46 56 45 2D
>
> 46 53 2DëR.-FVE-
>
> FS-n/aHeader of boot sector in BitLocker protected volume (Vista)
>
> EB 58 90 2D 46 56 45 2D
>
> 46 53 2DëX.-FVE-
>
> FS-n/aHeader of boot sector in BitLocker protected volume (Windows 7)
>
> [512 (0x200) byte offset]
>
> EC A5 C1 00[512 (0x200) byte offset]
>
> ì¥Á.DOCWord document subheader (MS Office)
>
> ED AB EE DBí«îÛRPMRedHat Package Manager file
>
> EF BB BFï»¿n/aByte-order mark (BOM) for 8-bit Unicode Transformation Format
>
> (UTF-8) files.
>
> (See the [Unicode Home Page](http://www.unicode.org/).)
>
> EF BB BF 3Cï»¿<WSFWindows Script Component (UTF-8)
>
> EF BB BF 3C 3Fï»¿<?WSCWindows Script Component (UTF-8)
>
> EF BB BF 3C 3F 78 6D 6C
>
> 20 76 65 72 73 69 6F 6Eï»¿<?xml
>
> Â versionYTTYouTube Timed Text (subtitle) file
>
> [At a cluster boundary]
>
> F0 FF FF[At a cluster boundary]
>
> ðÿÿn/aFAT12 File Allocation Table
>
> [At a cluster boundary]
>
> F8 FF FF FF[At a cluster boundary]
>
> øÿÿÿn/aFAT16 File Allocation Table
>
> [At a cluster boundary]
>
> F8 FF FF 0F FF FF FF 0F[At a cluster boundary]
>
> øÿÿ.ÿÿÿ.n/aFAT32 File Allocation Table
>
> [At a cluster boundary]
>
> F8 FF FF 0F FF FF FF FF[At a cluster boundary]
>
> øÿÿ.ÿÿÿÿn/aFAT32 File Allocation Table
>
> F9 BE B4 D9ù¾´ÙDATBitcoin-Qt blockchain block file
>
> FD 37 7A 58 5A 00ý7zXZ.
>
> XZXZ archive file
>
> [512 (0x200) byte offset]
>
> FD FF FF FF 02[512 (0x200) byte offset]
>
> ýÿÿÿ.PUBMS Publisher file subheader
>
> [512 (0x200) byte offset]
>
> FD FF FF FF 04[512 (0x200) byte offset]
>
> ýÿÿÿ.MSGMicrosoft Outlook/Exchange MessageQBMQuickBooks Portable Company FileSUOVisual Studio Solution User Options subheader (MS Office)
>
> [512 (0x200) byte offset]
>
> FD FF FF FF nn nn 00 00[512 (0x200) byte offset]
>
> ýÿÿÿ....PPTPowerPoint presentation subheader (MS Office)
>
> [512 (0x200) byte offset]
>
> FD FF FF FF nn 00[512 (0x200) byte offset]
>
> ýÿÿÿ..**_or_**[512 (0x200) byte offset]
>
> FD FF FF FF nn 02[512 (0x200) byte offset]
>
> ýÿÿÿ..XLSExcel spreadsheet subheader (MS Office)
>
> [512 (0x200) byte offset]
>
> FD FF FF FF 20 00 00 00[512 (0x200) byte offset]
>
> ýÿÿÿ ...OPTDeveloper Studio File Workspace Options subheader (MS Office)XLSExcel spreadsheet subheader (MS Office)
>
> [512 (0x200) byte offset]
>
> FD FF FF FF xx xx xx xx
>
> xx xx xx xx 04 00 00 00[512 (0x200) byte offset]
>
> ýÿÿÿ....
>
> ........DBThumbs.db subheader (MS Office)
>
> FE ED FA CEþíúÎn/aApple [OS X ABI Mach-O](https://github.com/aidansteele/osx-abi-macho-file-format-reference/blob/master/Mach-O_File_Format.pdf) binary file (32-bit)
>
> FE ED FA CFþíúÏn/aApple [OS X ABI Mach-O](https://github.com/aidansteele/osx-abi-macho-file-format-reference/blob/master/Mach-O_File_Format.pdf) binary file (64-bit)
>
> FE ED FE EDþíþíJKS[JavaKeyStore file](https://zgrepcode.com/java/openjdk/10.0.2/java.base/sun/security/provider/javakeystore.java)
>
> FE EFþïGHO, GHSSymantex Ghost image file
>
> FE FFþÿn/aByte-order mark (BOM) for 16-bit Unicode Transformation Format/
>
> 2-octet Universal Character Set (UTF-16/UCS-2), big-endian files.
>
> (See the [Unicode Home Page](http://www.unicode.org/).)
>
> FFÿSYSWindows executable (SYS) file
>
> FF 00 02 00 04 04 05 54
>
> 02 00ÿ......T
>
> ..WKSWorks for Windows spreadsheet file
>
> FF 0A 00ÿ..QRPQuickReport Report file
>
> FF 46 4F 4E 54ÿFONTCPIWindows international code page
>
> FF 4B 45 59 42 20 20 20ÿKEYB SYSKeyboard driver file
>
> FF 57 50 43ÿWPCWP, WPD, WPG, WPP, WP5, WP6WordPerfect text and graphics file
>
> FF D8ÿØJPE, JPEG, JPGGeneric JPEG Image file
>
> **Trailer:** FF D9 (ÿÙ)
>
> > **NOTES on JPEG file headers:** The proper JPEG header is the two-byte sequence, 0xFF-D8, aka _Start of Image (SOI)_ marker.
> >
> > JPEG files end with the two-byte sequence, 0xFF-D9, aka _End of Image (EOI)_ marker.
> >
> > Between the SOI and EOI, JPEG files are composed of _segments_. Segments start with a two-byte _Segment Tag_ followed by a
> >
> > two-byte _Segment Length_ field and then a zero-terminated string identifier (i.e., a character string followed by a 0x00), as
> >
> > shown below with the JFIF, Exif, and SPIFF segments.
> >
> > Segment Tags of the form 0x-FF-Ex (where x = 0..F) are referred to as
> > APP0-APP15, and contain application-specific information. The
> >
> > most commonly seen APP segments at the beginning of a JPEG file are APP0 and APP1 although others are also seen. Some additional
> >
> > tags are shown below:
> >
> > - 0xFF-D8-FF-E0 —[Standard JPEG/JFIF file](http://www.faqs.org/faqs/jpeg-faq/part1/section-15.html), as shown below.
> > - 0xFF-D8-FF-E1 — Standard JPEG file with Exif metadata, as shown below.
> > - 0xFF-D8-FF-E2 — Canon Camera Image File Format (CIFF) JPEG file (formerly used by some EOS and Powershot cameras).
> > - 0xFF-D8-FF-E8 —[Still Picture Interchange File Format (SPIFF)](http://www.digitalpreservation.gov/formats/fdd/fdd000019.shtml), as shown below.
>
> FF D8 FF E0 xx xx 4A 46
>
> 49 46 00ÿØÿà..JF
>
> IF.JFIF, JPE, JPEG, JPG[JPEG/JFIF graphics file](https://jpeg.org/jpeg/workplan.html)
>
> **Trailer:** FF D9 (ÿÙ)
>
> FF D8 FF E1 xx xx 45 78
>
> 69 66 00ÿØÿá..Ex
>
> if.JPGDigital camera JPG using [Exchangeable Image File Format (EXIF)](http://www.cipa.jp/std/documents/e/DC-008-2012_E.pdf)
>
> **Trailer:** FF D9 (ÿÙ)
>
> See ["Using Extended File Information (EXIF) File Headers in Digital\
> \
> Evidence Analysis"](http://www.utica.edu/academic/institutes/ecii/publications/articles/A0B1F944-FF4E-4788-E75541A7418DAE24.pdf) (P. Alvarez, _IJDE_, _2_(3), Winter 2004) and
>
> [ExifTool Tag Names](http://www.sno.phy.queensu.ca/~phil/exiftool/TagNames/index.html)
>
> FF D8 FF E8 xx xx 53 50
>
> 49 46 46 00ÿØÿè..SP
>
> IFF.JPG[Still Picture Interchange File Format (SPIFF)](http://www.fileformat.info/format/spiff/index.dir)
>
> **Trailer:** FF D9 (ÿÙ)
>
> FF Exÿ.FF Fxÿ.MPEG, MPG, MP3MPEG audio file frame [synch pattern](http://www.mp3-tech.org/programmer/frame_header.html)
>
> FF F1ÿñAACMPEG-4 Advanced Audio Coding (AAC) Low Complexity (LC) audio file
>
> FF F9ÿùAACMPEG-2 Advanced Audio Coding (AAC) Low Complexity (LC) audio file
>
> FF FEÿþREGWindows Registry file
>
> n/aByte-order mark (BOM) for 16-bit Unicode Transformation Format/
>
> 2-octet Universal Character Set (UTF-16/UCS-2), little-endian files.
>
> (See the [Unicode Home Page](http://www.unicode.org/).)
>
> FF FE 00 00ÿþ..n/aByte-order mark for 32-bit Unicode Transformation Format/
>
> 4-octet Universal Character Set (UTF-32/UCS-4), little-endian files.
>
> (See the [Unicode Home Page](http://www.unicode.org/).)
>
> FF FE 23 00 6C 00 69 00
>
> 6E 00 65 00 20 00 31 00ÿþ#.l.i.
>
> n.e. .1.MOFWindows MSinfo file
>
> FF FF FF FFÿÿÿÿSYSDOS system driver
>
> * * *
>
> > ACKNOWLEDGEMENTS
> >
> > The following individuals have given me updates or suggestions for this
> > list over the years: Devon Ackerman, Nazim Aliyev, Marco Barbieri,
> > Vladimir Benko, Arvin Bhatnagar, Jim Blackson, Keith Blackwell, Alex
> > Boschma, Sam Brothers, David Burton, Alex Caithness, Erik Campeau, Björn
> > Carlin, Tim Carver, Michael D Cavalier, Per Christensson, Oscar Choi,
> > JMJ.Conseil, Jesse Cooper, Jesse Corwin, Mike Daniels, David DeBrota,
> > Cornelis de Groot, Jeffrey Duggan, Tony Duncan, Jon Eldridge, Ehsan
> > Elhampour, Jean-Pierre Fiset, Peter Almer Frederiksen, Tim Gardner,
> > Chris Griffith, Linda Grody, Andis Grosšteins, Paulo Guzmán, Rich Hanes,
> > George Harpur, Brian High, Eric Huber, John Hughes, Allan Jensen,
> > Broadus Jones, Matthew Kelly, Axel Kesseler, Nick Khor, Shane King, Art
> > Kocsis, Thiemo Kreuz, Bill Kuhns, Evgenii Kustov, Andreas Kyrmegalos,
> > Glenn Larsson, Jeremy Lloyd, Anand Mani, Kevin Mansell, Davyd McColl,
> > Par Osterberg Medina, Michal, Sergey Miklin, David Millard, Bruce
> > Modick, Lee Nelson, Mart Oskamp, Dan P., Jorge Paulhiac, Carlo Politi,
> > Seth Polley, Hedley Quintana, Anthony Rabon, Stanley Rainey, Cory
> > Redfern, Bruce Robertson, Ben Roeder, Thomas Rösner, Gerd, Röthig,
> > Gaurav Sehgal, Andy Seitz, Anli Shundi, Erik Siers, Philip Smith, Mike
> > Sutton, Matthias Sweertvaegher, Tobiasz Åšwiatlowski, Frank Thornton,
> > Erik van de Burgwal, Øyvind Walding, Jason Wallace, Daniel Walton,
> > Franklin Webber, Bernd Wechner, Douglas White, Mike Wilkinson, Gavin
> > Williams, Sean Wolfinger, David Wright, Yuna, and Shaul Zevin. I thank
> > them and apologize if I have missed anyone.
> >
> > I would like to give particular thanks to Danny Mares of [Mares and Company](http://www.maresware.com/), author of the [MaresWare Suite](http://www.maresware.com/maresware/software.htm) (primarily for the "subheaders" for many of the file types here), and the people at [X-Ways Forensics](http://www.x-ways.net/) for their permission to incorporate their lists of file signatures.
> >
> > Finally, Dr. Nicole Beebe from The University of Texas at San Antonio
> > posted samples of more than 32 file types at the Digital Corpora, which I
> > used for verification and additional signatures. These files were used
> > to develop the [Sceadan File Type Classifier](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=06567922). The file samples can be downloaded from the [Digital Corpora](https://digitalcorpora.org/corpora/files) website.
> >
> > COPYRIGHT NOTICE
> >
> > All information on this page © 2002-2023,
> > Gary C. Kessler. Permission to use the material here is extended to any
> > of this page's visitors, as long as appropriate attribution is provided
> > and the information is not altered in any way without express written
> > permission of the author.


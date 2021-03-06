AnnotationConverter
===================
Version 1.0.0 Beta
S*bit*Fire Software, 2014-12-14


Purpose
-------
The AnnotationConverter imports annotations (highlights, notes, bookmarks.  
from one E-reader and converts them to the format used by another.


Restrictions, Requirements
--------------------------
� Requires .Net 4 (if absolutely necessary, I could try to create a .Net 3.5 version)
� Has only be tested on Windows 7 (but should work on other versions of Windows, too)
� Currently, annotations can only be converted from Sony PRS-T1-3 to Adobe Digital Editions 2-3
� Only epub is supported
� Drawings (notes done by handwriting.  will not be converted


Installation instructions
-------------------------
An installer is not included.
Simply unpack the entire content of AnnotationConverter.zip to your directory of choice.
Opening AnnotationConverter.exe should start the application.
If .NET 4 is not installed on your machine, install instructions will automatically be provided by Windows (Windows 7 and successors).


Manual
======


Sony PRS-T# -> Mantano Reader
-----------------------------
1.  Import the book which will receive the annotations in Mantano Reader. Then, connect to your android device to your PC and copy the mantano library to your PC. The library can be found in a folder called /storage/emulated/0/Mantano and should contain. This might vary depending on your device. The library must contain a file called mreader-premium.db or mreader-lite.db.

2.  Click 'Browse' to look for the database file containing your books (books.db). You can either directly use the file on your reader (..\Sony_Reader\database\book.db.  or a backup of this file.

3.  The combobox will now display all epubs containing highlight or bookmarks. Choose the one you want to convert.

4.  Browse to the folder you have copied in step 1 and choose the database file (mreader-premium.db / mreader-lite.db). If both files are present, choose mreader-premium.db.

5.  The target book should be identified automatically. If not, browse for it and/or make sure you have imported the book to Mantano Reader.

6.  Choose the formatting options. They will be used for all new/changed annotations.

7.  Hit 'Convert'. Entries, that already exist, will be skipped, changed entries will be updated and new entries will be inserted. Depending on your number of annotations, this can take a looong time (sorry for that).

8.  Make sure Mantano Reader is not currently running on your android device, otherwise the library will be broken (you can restore it using the backup, if that should happen).
Copy the mreader-premium.db / mreader-lite.db file back to your android devide and start Mantano Reader.


Sony PRS-T# -> Adobe Digital Editions
-------------------------------------
1.  Import the book containing your annotations into Adobe Digital Editions (2 or 3).

    If the epub is imported from an external source (the reading device, Calibre, any folder containing your books), ADE will simply reference the book (not copy it) and create an .annot file in ..\My Digital Editions\Annotations\.external

    If the book is downloaded/unlocked from within ADE, the .epub file will be created in 
    '..\My Digital Editions\'
    and an .epub.annot file will be created in
    '..\My Digital Editions\Annotations\'
    Open 'AnnotationConverter.exe' and check 'Ok, I've done that'

2.  Click 'Browse' to look for the database file containing your books (books.db). You can either directly use the file on your reader '(..\Sony_Reader\database\book.db)' or a backup of this file.

3.  The combobox will now display all epubs containing highlight or bookmarks. Choose the one you want to convert

4.  The tool will attempt to automatically find the target file within your 'My Digital Editions' folders. However, if the book on the reader has a different filename than within ADE, the .annot file will not be found. In such a case, use 'Browse' to look for the corresponding file.

    Note: You first have to import the book in ADE (step 1) and only then convert the annotations. Otherwise your converted annotations will be overwritten with an empty .annot file once you import the book in ADE.

5.  Hit 'Convert,' wait for the process the finish and open ADE.

The book should now contain your annotations. Depending on the number of annotations, it can take several minutes to open the file in ADE (the annotations in ADE are based on XML -> bad performance).


Change history
--------------
2014-12-14, v. 1.0.0:
added Mantano Reader as target type

2014-09-19, v. 0.9.0 Beta:
initial version, supporting one source type (Sony PRS-T#.  and one target type (ADE)



License
-------
Copyright (c) 2014 Pesche Helfer

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
# moodle-po
Converted .po files for Moodle php files.

HOW TO CONVERT MOODLE PHP FILES INTO PO-GETTEXT FORMAT

- Download the english language pack and language pack of your language ( must be the same moodle vesion e.g https://download.moodle.org/langpack/3.5/ )

-Create a directory and unpack the compressed files.
 
-Now you have two directories with the php files from each language

- 1st step > create the .pot files from the english translation with the command
$ php2po -P en pot  

- 2nd step > create the .po files that have already translated strings in your language with the command 
$ php2po -t en el po-el

(el and po-el are the directories for the Greek language- Replace with your language code)

- Since you are  missing all the files that do not had any translated stings, you have to add these files manually to your language-po directory

- 3nd step - Copy the english .pot files in a test directory and convert them to .po files with the command
$ pot2po *.pot  *.po

- 4th step - Copy alL the missing  (untranslated) .po files from the test directory into your language-po directory 

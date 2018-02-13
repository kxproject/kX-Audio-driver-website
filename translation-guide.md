## kX Translation Guide

There are two main fields of work: to translate the kX Documentation and to translate the kX Audio Driver interface. You can choose any field you wish. If you wish to translate the documentation, please go to our Support Forum and find a topic dealing with documentation translations.

If you want to localize the kX Audio Driver, do the following:

- get the latest driver release (or check our Support Forum for the latest development release currently available)
- add (or update) a translation for your native language as shown below

After you download the very recent release, run the installation program - it will extract kX Project files
(typically, in C:\Program Files\kX Project\35xx folder). Note: it is not necessary to install the driver, just
unpack the installation files! Now you should find the file 'kxskin.kxs': it is actually a WinRar archive. 
Rename the file into 'kxskin.rar' and use WinRar to unpack the file. You will need only -one- file from this archive,
'lang.ini'. After you get the file, open it in any text editor (such as NotePad) and add/update the translation the following way:


# an example:

- function=Event:
- function.222='your translation here'

Note: instead of '222' you should use your locale number.
For example, for Russian it is '419', for German it is '407' and so on.
The full list of language codes is available here or here.

Don't forget to specify your name and e-mail address in the very beginning of the 'lang.ini' file in order to be mentioned on our 'credits' page.

You can test your translation by 'updating' the 'kxskin.kxs' archive with your new 'lang.ini' file. Sometimes, however, you will not be able to see the results until your language is supported via 'Language' menu by the mixer.

When your translation is done, commit your custom lang.ini file to be included in the next release of the kX Audio Driver.

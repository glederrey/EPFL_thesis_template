# Template for the EPFL PhD thesis

Welcome to the **unofficial** template for the EPFL PhD thesis. Before starting to write your thesis, have a look at this page: [https://www.epfl.ch/education/phd/regulations/internal-regulations/edoc-faq-end-of-thesis/](https://www.epfl.ch/education/phd/regulations/internal-regulations/edoc-faq-end-of-thesis/). It will give you all mandatory information concerning your thesis. It is also not required for you to use this template. It's only here to help you and remove the struggle to create your own template. 

Other versions of the template:
- Mathias Payer: [https://github.com/HexHive/thesis_template](https://github.com/HexHive/thesis_template).

If you are using this template and improved it, if you have suggestions to improve it or if you have questions, feel free to contact me: [gael.lederrey@epfl.ch](mailto:gael.lederrey@epfl.ch). You can also contact [PolyDoc](mailto:polydoc@epfl.ch), the PhD students association from EPFL, or visit their [website](http://polydoc.epfl.ch) if you have more general questions.

If you are looking for other templates in Word or from different universities, feel free to visit this page: [https://www.epfl.ch/education/phd/regulations/internal-regulations/edoc-faq-end-of-thesis/](https://www.epfl.ch/education/phd/regulations/internal-regulations/edoc-faq-end-of-thesis/). At the end of the page, under the collapse button named *Any thesis template available*, you will find a generic Word template.

> **WARNING**: These templates are not maintained. However, if you modify it, feel free to send it to PolyDoc and we will replace them.

And if you created another template and want to share it with other PhD students from EPFL, feel free to contact PolyDoc and we'll see what we can do. 

## FAQ 

**The compilation fails: it says "LaTeX Error: Unknown option `explicit` for package `titlesec`**
> The package titlesec has been modified in 2007 to include an option which allows more customization of the chapter titles. This template relies heavily on this option. In order to resolve this, you need to update to a more recent version (either your full Latex-Distribution or at least the titlesec package).

**I have a problem with special characters, the compilation fails as soon as there is a special character in my file**
> For best cross-platform compatibility, the template is configured for "UTF-8" input encoding instead of platform specific encodings (such as "Western-Latin for Mac"). In your Latex-Editor, be sure that the files are saved with this encoding.
(In TeX-Shop for Mac: Preferences -&gt; Source-Code -&gt; Encoding -&gt; "UTF-8". You'll need to re-open and save the files in order to make the change happen).

**I'm using "mhchem" for typesetting chemical formula and there is a bug in the compilation**
> This package is under active development: it has been updated on 2011/06/03 to version 3.11 correcting for an incompatibilty with some font-related packages. Please update your Latex-distribution to this latest version of mhchem by downloading the newest version from CTAN and replacing your existing mhchem.sty file by the newer version.

**I want to use Tex+dvi for compiling my files, because I have a lot of .eps graphics and I don't want to convert all of them and use pdftex for compiling my files**
> Never mind for the .eps files: the pdftex compiler is able to convert them automatically to .pdf files. In some configurations you will not even need to do anything besides specifying the full graphic-file-names (ex: "mybeautifuleps.eps"). If this fails, you can still include the [epstopdf](https://ctan.org/pkg/epstopdf?lang=en) package manually.
The template chapter header styles are unfortunately not (yet) compatible with tex+dvi compilation, so there is really no way around the pdftex compiler at the very moment if you want to use this template.

**The compilation fails with the error message "! pdfTeX error (font expansion): auto expansion is only possible with scalable fonts**
> This error stems from an incompatibility of your system with the font used for the titlepage. We might change this for the whole template design soon, but in the mean time, just open "head/titlepage.tex" -&gt; go to line 4 and put the line in comment by adding a "%" in front of the line such that it reads "%\sffamily". After this the compilation should work.
>
> Another solution to this problem (tested on Windows 10) is the following:
>  1. Start "MiKTeX Settings (Admin)"
>  2. Press "Refresh FNDB"
>  3. Press "Update Formats"
>  4. Press "OK" (to close the app)
>  5. Clean auxiliary files (.aux and .out)
>  6. Recompile and everything should work.

## Contributors

* ??? (Original creator)
* Diogo Rodrigues (Fixed latex -> dvips -> ps2pdf version + other minor problems)
* Mahdi Khoramshahhi (Added a fix for the bug on the font expansion) 
* Léo Belzile (Changed the logo, tidy up the code, fixed some bugs) [**current version**]

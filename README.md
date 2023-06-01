[Table of contents](toc.md)

<img src="https://github.com/LetsWrappIt/DocMkr/blob/main/images/DocMkr_logo_1280x640.png" width="300" height="150">

DocMkr, short for DocMaker, is an unopinionated, scratch-your-own-itch, yet powerfull tool, that generates proper PDF documents.

What makes DocMkr so usefull?
- DocMkr generates beautiful PDF documents.
- DocMkr uses plain text/xml/html/markdown files as input.
- It separates styling and content: this allows for sharing and reuse of style templates.
- It supports 'classic' document structures like: Sections, Pages, Headers, Footers, Headings, TableOfContents, Images ... 
- DocMkr supports a conditional build process (write 1 tutorial, publish for 10 brands?)
- It supports multi file projects. This facilitates large document scenarios.
- It is easy to store documentation under version control on github (and others).


## How does DocMkr work?
The main function of DocMkr is the 'build' process, which takes 2 core files and transforms those into a PDF document.

- The first file is a DocMkr Template file (DmTemplate or dmt), which contains the styling settings.
- The second file is a DocMkr Content file (DmContent or dmc).

DocMkr itself comes in the form of a console app (win/linux/mac).

Use your favorite text/html/xml editor to edit content and styling template.

## "Start Here" tutorial

### Step 1: Get your editor
Pick your favorite text/XML/HTML editor (example: VsCode) for writing content and styling. 

### Step 2: Write a DmContent file
Write a HTML document with some content, this is the DmContent file (dmc).
Example:
```
<html>
<body>
    <section>
        <h1>A short manual</h1>
        <p>This is a very short manual ...</p>
    </section>
</body>
</html>
```
Save as: manual.dmc.html


### Step 3: Write a DmTemplate file
Write a XML document with styling configuration, this is the shortest, and still viable, DmTemplate file (dmt).
```
<docmkr-template>
</docmkr-template>
```
Save as: simple.dmt.xml

 Since this simple.dmt.xml file is almost empty, DocMkr will use default values. This will result in a nicely readable PDF. 
 The easiest way to author your own DmTemplate file, is to take an existing one and modify settings in that template.

### Step 4: Donwload DocMkr cli

You can do that [here](download.md)!


### Step 5: Write a build script

Write a one line script which includes the proper arguments to start the PDF generation process. Something like:

Example:
```
./docmkr.exe build /dmt:simple.dmt.xml /dmc:manual.dmc.html
```

Save as: generate-manual.cmd

### Step 6: Build the PDF
Call the build script. It will call DocMkr to build your first PDF document.
From here you can build further.



Some links:
- [Table of contents](toc.md)
- [Download](download.md)
- [ChangeLog](changelog.md)

What is nxslt2?

nxslt2 is a free feature-rich command line utility that allows to perform XSL Transformations (XSLT) using .NET Framework 2.0 XSLT implementation - System.Xml.Xsl.XslCompiledTransform class. nxslt2 is backwards compatible with functionality and command line options provided by Microsoft's MSXSL.EXE Command Line Transformation Utility with a tiny difference: unlike msxsl.exe, nxslt2 does not support specifying start mode. In addition, nxslt2 supports plenty of advanced features:

    XInclude 1.0/XPointer 1.0
    Embedded stylesheets
    Multiple output documents via exsl:document extension element
    Custom URI resolving
    Custom extension functions
    EXSLT and EXSLT.NET extension functions
    New! XHTML output
    New! XSLT 2.0 character maps
    Credentials to access XML source and XSLT stylesheet
    Pretty printing 

Requirements

nxslt2 is the .NET 2.0 Framework application, written in C# 2.0 language and requires .NET Framework version 2.0 to be installed.
Usage

To see help on nxslt2 usage, run nxslt2 with -? option:

nxslt2 -?

You should see the following message:

.NET 2.0 XSLT command line utility, version 2.3.0
(c) 2004-2006 Oleg Tkachenko, http://www.xmllab.net
Running under .NET 2.0.50727.1378

Usage: nxslt source stylesheet [options] [param=value...] [xmlns:prefix=uri...]

Options:
   @file        Reads a file for more options
  -?            Show this message
  -o filename   Write output to named file
  -xw           Strip non-significant whitespace from source and stylesheet
  -xe           Do not resolve external definitions during parse phase
  -xi           Do not process XInclude in source XML during parse phase
  -xslxi        Process XIcnlude in XSLT stylesheets
  -v            Validate documents during parse phase
  -t            Show load and transformation timings
  -xs           No source XML
  -pp           Pretty-print source document
  -pi           Get stylesheet URL from xml-stylesheet PI in source document
  -r            Use named URI resolver class
  -af           Assembly file name to look up URI resolver class
  -an           Assembly full or partial name to look up URI resolver class
  -mo           Allow multiple output documents
  -ext          Comma-separated list of extension object class names
  -cm           Process XSLT 2.0-like character maps
  -xhtml        Enforce XHTML output mode
  -xmlc creds   Credentials in username:password@domain format to be
                used in Web request authentications when loading source XML
  -xslc creds   Credentials in username:password@domain format to be
                used in Web request authentications when loading XSLT
  -             Dash used as source argument loads XML from stdin
  -             Dash used as stylesheet argument loads XSLT from stdin

Basic usage example: to transform source.xml document using style.xsl stylesheet into result.html file, run the following command:

nxslt2 source.xml style.xsl -o result.html

For more usage info and samples see following sections.

Note: Individual options may be entered anywhere in the command, but source and stylesheet (they can be filenames or URLs) must follow in this order. Some arguments are mutually exclusive, for instance stylesheet and -pi.

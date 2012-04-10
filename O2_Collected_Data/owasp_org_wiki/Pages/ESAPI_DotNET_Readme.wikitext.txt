'''OWASP ESAPI - .NET Edition ReadMe'''

Release 0.2: August 2009

<br>'''Welcome to the .NET Edition of OWASP ESAPI v0.2'''

This document provides information about the .NET Edition of OWASP ESAPI. The topics below cover system requirements, additional product information, and application notes. 

The code for the ESAPI is currently in [http://code.google.com/p/owasp-esapi-dotnet/ Google Code]. 

Download the latest .NET ESAPI library binary from Google Code [http://owasp-esapi-dotnet.googlecode.com/files/Esapi.zip here]. 

Download the latest .NET ESAPI documentation from Google Code [http://owasp-esapi-dotnet.googlecode.com/files/Esapi_Documentation.zip here]. It is a zipped .chm (help) file.

You can also browse the .NET ESAPI documentation [http://alexsmolen.com/dotnetesapidoc/index.html here]

To download and work with the source you must use an SVN tool.

[http://ankhsvn.open.collab.net/ AnkhSVN] is a free SVN tool that integrates with Visual Studio.  Point your SVN tool at http://owasp-esapi-dotnet.googlecode.com/svn/trunk.  Anonymous checkout is supported.

You can also [http://code.google.com/p/owasp-esapi-dotnet/source/browse browse the source].

<br>'''System Requirements'''

The solution is created with VS 2008 and .NET 3.5. However, the actual code should be compatible with .NET 2.0, so it should be simple to get the code to compile in most environments.   [[ESAPI.NET_Build_Troubleshooting|Troubleshooting]]

<br>'''Other Requirements'''

The .NET Edition of OWASP ESAPI includes a reference implementation which may be tailored or replaced, according to your organization's needs.

You must also download download and install the latest version of the [http://www.codeplex.com/AntiXSS AntiXss] library.


<br>'''Server Recommendations'''

None

<br>'''Obtaining the .NET Edition of OWASP ESAPI'''

There are a couple of ways to get started with the .NET ESAPI. 

If you simply want to start using the functionality, you can download the assembly from [ Google Code]. You will also need to add the appropriate configuration (see here).

You can download the solution from Google Code with SVN.

You will need to download and install the AntiXss library separately, in order to respect the code licensing. 

The SwingSet application requires you to login - just register a username and go. You also need to supply a SMTP host in the web.config file in SwingSet in order to register a user, so that you can get an activation email. I might change this in the released version, since it's sort of a pain. You can just use the external SMTP server for an email account you own and use that - i.e.

    <mailSettings>
      <smtp from="dot-net-esapi@owasp.com">
        <network
             host="you fill this part in, for example d.mx.mail.yahoo.com for a yahoo.com mail account"
             port="25"
             />
      </smtp>
    </mailSettings>


<br>
----
'''OWASP ESAPI - .NET Edition Release Notes'''

Release 0.2

August 2009

<br>'''Welcome to the .NET Edition of OWASP ESAPI v0.2'''

This document provides information about .NET Edition of OWASP ESAPI v0.2. Browse through the topics below to find out about new features, known issues and limitations for this release.

Information specific to the changes in this release are captured in this document set. For all other information and for feature details, see the ESAPI <version> programming manual.

<br>'''New features'''

This release improve significanlty on the first release. The following components have been redesigned and reimplemented:

* AccessController
* AccessReferenceMap
* Encoder
* Encryptor
* Esapi
* HttpUtilities
* IntrusionDetector
* Logger
* Randomizer
* SecurityConfiguration
* Validator

The SwingSet application has also been introduced, to demonstrate how to use the ESAPI as well as showcase other ASP.NET security best practices.

<br>'''Fixed in this release'''

* All components have been redesigned - there have been major changes since v0.1.

<br>'''Known issues'''

* Canonicalization support is incomplete - only some Codecs support decoding.
* There are only a few ValidationRules.
* AccessController implementation does not provide policy storage.
<br>'''Upgrading from earlier releases'''

* This version is an entirely different code base. Please completely upgrade all existing implementations.

<br>
[[Category: OWASP Enterprise Security API]]
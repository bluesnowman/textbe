# Development Environment #

This page will give concrete version numbers. However users can and should attempt to use more recent versions, if the ones mentioned have become outdated.

To set up your Environment

  * [Windows XP Professional 32 Bit Service pack 3](http://en.wikipedia.org/wiki/Windows_XP). You must obtain a licence for this software.
  * [Java SE 6 Update 30 JDK](http://en.wikipedia.org/wiki/Java_Development_Kit). It is available from the [Oracle Java SE Downloads](http://www.oracle.com/technetwork/java/javase/downloads/index.html) page.
  * Eclipse Classic 3.7.1 (labeled '[Indigo](http://en.wikipedia.org/wiki/Eclipse_(software)#Releases)') available from the [Eclipse Downloads](http://www.eclipse.org/downloads/?osType=win32) page. At the time of this writing this revision [R-3.7.1-201109091335 available through this link](http://www.eclipse.org/downloads/download.php?file=/eclipse/downloads/drops/R-3.7.1-201109091335/eclipse-SDK-3.7.1-win32.zip) **Note:** While TextBE requires numerous Modeling plugins to build, the **Eclipse Modeling Tools** version on the Indigo downloads page is still based on version 3.6 'Helios' of Eclipse. As a result, we need to assemble the required features by hand.

# Installing software into eclipse #

Procedure for [installing new software](http://help.eclipse.org/indigo/topic/org.eclipse.platform.doc.user/tasks/tasks-124.htm?resultof=%22%69%6e%73%74%61%6c%6c%22%20%22%69%6e%73%74%61%6c%22%20%22%6e%65%77%22%20%22%73%6f%66%74%77%61%72%65%22%20%22%73%6f%66%74%77%61%72%22%20) in Indigo.

# Project Access / Version Control #

Install [Subclipse](http://subclipse.tigris.org/) from the
[Subclipse 1.8.x release update site](http://subclipse.tigris.org/update_1.8.x)

**Note:** In order to connect to source code as a contributor, you need to use
'xyz@google.com' (replace 'xyz' by your uid) as your SVN user name, but you need a **different** password. Look at the following procedure that shows you
[where to get your subversion access password](http://code.google.com/p/support/wiki/SubversionFAQ#Where_do_I_get_a_password_for_committing_to_Subversion?).

## Code ##

[TextBe Repository Trunk (SVN)](http://textbe.googlecode.com/svn/trunk)

## Wiki (Optional) ##

You can edit the [TextBE wiki online](http://code.google.com/p/textbe/w/list). If you want to edit it offline, you can check it using the [TextBe Wiki Trunk (SVN)](https://textbe.googlecode.com/svn).

Use this procedure [to add images to the wiki](http://code.google.com/p/heekscad/wiki/HowtoAddImagesToWiki).

The wiki content is written in a subset of the [MoinMoin](http://en.wikipedia.org/wiki/MoinMoin) syntax documented on the [Google Code Wiki Syntax page ](http://code.google.com/p/support/wiki/WikiSyntax). To have some support with editing the content, install Mylyn Wikitext and the
[Moinmoin Wikitext integration](http://update-site.moinmoinwikitext.googlecode.com/hg/) for Eclipse from the [Moinmoin Wikitext integration download site](http://update-site.moinmoinwikitext.googlecode.com/hg/)

## Issues (Optional) ##

You can manage issues in the [TextBE online issues list](http://code.google.com/p/textbe/issues/list). If you want to edit them in Eclipse, install Mylyn, followed by the [Mylyn Google Code Connector](http://code.google.com/p/googlecode-mylyn-connector/) installable from the  [Google code mylyn connector update site](http://knittig.de/googlecode-mylyn-connector/update/).

**Note:** This connector uses your google account uid and password.
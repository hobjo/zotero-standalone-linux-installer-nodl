Zotero standalone installer for Linux (no download version)
===========================================================

Made with love in UE.

About
-----

This is a modified version of the automated installer from <https://github.com/smathot/zotero_installer>.
The provided "zotero_installer.sh" script will install Zotero standalone on a Linux system, provided you give it an archive downloaded from the official website.
I modified the more complete original version to better cope with proxy issues, and give more flexibility about the version I choose to install.

Using the installer
-------------------

1- Download a Zotero Standalone archive from <http://www.zotero.org/download/>, and save it somewhere (/tmp/ is used for what follows).
Example for Zotero 4.0.17 (may be outdated) and a x86_84 OS:

	wget http://download.zotero.org/standalone/4.0.17/Zotero-4.0.17_linux-x86_64.tar.bz2 -O /tmp/Zotero-4.0.17_linux-x86_64.tar.bz2

2- Download zotero_installer.sh and run it. This extracts Zotero archive into /opt/zotero, and create a Zotero menu entry.

	wget https://raw.github.com/hobjo/zotero-standalone-linux-installer-nodl/master/zotero_installer.sh -O /tmp/zotero_installer.sh
	chmod +x /tmp/zotero_installer.sh
	/tmp/zotero_installer.sh /tmp/Zotero-4.0.17_linux-x86_64.tar.bz2


Compatibility with Zotero versions
----------------------------------

This script was tested and working for all 4.0.x releases of Zotero Standalone, for x up to 17, for x86_84 architectures.


How I typically use it
----------------------

I saved once for all the installer under a ~/bin/ folder, gave it executable permissions, and added ~/bin to my $PATH.
Then, after downloading the latest version of Zotero into ~/Downloads/ I run:

	sudo $(which zotero_installer.sh) $(find ~/Downloads/ -iname "zotero*linux*.tar*" | sort -r | head -n 1)

	
More features / Original script
-------------------------------

The original work by Sebastiaan Mathot at <https://github.com/smathot/zotero_installer> provides automated download and even a PPA, so make sure the check it.


License
-------

This installer falls under the General Public License v2. For more information, see the file `COPYING` or visit <http://www.gnu.org/licenses/gpl.html>.

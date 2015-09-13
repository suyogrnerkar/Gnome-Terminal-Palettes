## Gnome Terminal Palettes

### Collection of numerous vivid gnome terminal palettes.

- Gnome terminal color palette details are stored under directory 
  ~/.gconf/apps/gnome-terminal/profiles/

	- In Default directory you will be able to see a file named %gconf.xml. 
  	This file stores all palette related data. So you can backup all the 
  	files under directory ~/.gconf/apps/gnome-terminal/profiles/ or replace
  	the contents of the same file with contents of file ending in ' palette.xml '
    in respective themes in this repo so as to load only the color palette for gnome terminal.

	- To view the configurations: Open gconf-editor using dash and navigate 
	  to apps->gnome-terminal->Profiles->Default

- For dumping and loading complete profile on the system with the colors and settings you want, run:

  - `gconftool-2 --dump '/apps/gnome-terminal' > gnome-terminal-profile.xml`
    
    to dump the profile to gnome-terminal-profile.xml 

  - Then on the other machines, run

    `gconftool-2 --load gnome-terminal-profile.xml`
    
    to set it.

  Note that this method overwrites all settings. Try running

  gconftool-2 -R '/apps/gnome-terminal'
  to see all the settings that will be affected.
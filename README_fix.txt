
This patch fixes most issues related to engine branch incompatibility and 
is designed to run using the latest "Beta" of Source SDK Base 2013 Singleplayer.

Hope it helps.

Sincerely,
Marc-Antoine (malortie) Lortie.

===============================
** Instructions **
===============================

1a.

	Ensure that you have Source SDK Base 2013 Singleplayer installed and configured to use 
	the latest beta, "incoming".

	If not set:

	- Right-click on Source SDK Base 2013 Singleplayer.
	- Go to the "Betas" tab.
	- Change "Select the beta you would opt into" option to "incoming"
	
	(Optionally restart Steam).
	
1b.

	Verify the integrity of game cache for Source SDK Base 2013 Singleplayer.
	
	- Right-click on Source SDK Base 2013 Singleplayer.
	- Go to the "Local Files" tab.
	- Click "Verify Integrity of Tool cache..."
	- Wait until game cache inspection is completed.
	
	(Optionally launch Source SDK Base 2013 Singleplayer to update game data files).

2.

	Ensure that you have downloaded and installed "DayHard", available
	on the mod's page.
	
	if not, you can download it at the following address:
	
	http://www.runthinkshootlive.com/posts/day-hard-complete/
	
	** Do not download any additional patches that could have been made. **
	
	-------------------------------------------------------------
	 Method 1 (Recommended)
	-------------------------------------------------------------
	
	** This method will NOT make the mod appear in your Steam game library. **

	- Extract the content of this (patch) archive to your "Source SDK Base 2013 Singleplayer" folder.
	  
		.i.e
		<Drive>:\Steam\steamapps\common\Source SDK Base 2013 Singleplayer\DayHard
	

		In the "DayHard" folder, you should have several other folder 
		such as  bin; cfg; maps...
	
	- Restart Steam
	- Right click on Source SDK Base 2013 Singleplayer.
	- Select "Set Launch Options" in the "General" tab.
	- Enter the following: 	-game "DayHard"
	- Click OK. (Optionally restart Steam).
	
	-------------------------------------------------------------
	 Method 2
	-------------------------------------------------------------
	
	** This method will make the mod appear in your Steam game library. **
	
	- Extract the content of this (patch) archive to your SourceMods folder.
	  
		.i.e
		<Drive>:\Steam\steamapps\Sourcemods\DayHard

		NOTE: If you use multiple drives to store Steam game data, you should use
			  the <Drive> in which the Windows folder resides.

			 .i.e
			 <Drive>:\Windows
			 <Drive>:\Program Files (x86)\Steam\steamapps\sourcemods\DayHard
			 
		In the "DayHard" folder, you should have several other folder 
		such as  bin; cfg; maps...
	
	- Restart Steam. 
	- "DayHard" should appear in your Steam game library.
	
	---------------------------------
	 Technical problems in Method 2
	---------------------------------

	If you encounter any crash when launching the mod, try the following:
	- Right click on "DayHard".
	- Select "Set Launch Options" in the "General" tab.
	- Enter the following without quotes: "-allowdebug"
	- Click OK. (Optionally restart Steam).
	
	
===============================
** Fixed **
===============================

- "Could not load library client." when launching the mod.
-  Scene files not playing.
-  In-game menu.
-  Gameinfo.txt now has correct parameters.
-  Crash due to prop ragdoll entity, on third map (dayhardpart3)

===============================
** Changes **
===============================

- Map dayhardpart4

Restructured the tram scene to allow Jack to remain present during
entire ride.

This was done due to AI inconsistency. Jack would fall through the
train, and thus not being able to follow players after arriving at
the bottom of the hill.
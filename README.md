**This is an experimental/work-in-progress UI.** Before installing this, take a backup of your UI folder and be prepared for some things to not work.

This UI is designed to be played on The Heroes Journey and will probably break on any other server.

The philosophy behind this UI is that it is simple, minimalist, and strips away a lot of the information overload that comes built into EQ. When you see screenshots of people's UI setups and they have 1/3rd of their screen covered in windows, this UI is a counter to that.

## Player Window
![image](https://github.com/user-attachments/assets/644b3ef4-0f82-4c5a-b482-6744256182b8)

The player window displays health as a larger red bar, mana as a smaller blue bar, and endurance as a smaller yellow bar. Beneath that is a casting bar (pink) that appears only when casting spells.

- Plan to eventually incorporate the oxygen bar in here somehow instead of having it as its own window.

## Target Window

Target bar matches the player health bar in size and is designed to mirror it on the screen. The upper bar is the player's current target and then beneath that it displays the target's target.

- Target buffs currently don't display.

## Hotbars and Spell Gems

These are smaller than the default hot bars and are designed to use the custom icon/label system. Unused hot buttons are semi-transparent to get out of the way. The spell gems are sized equally to the hot buttons so the spell gem bar essentially just looks like another hotbutton bar.

- If you are unable to move your spellgem bar horizontally, open EQUI_CastSpellWindow, ctrl+f for <Style_Border>false</Style_Border> and set it to true, and set <Style_Transparent>true</Style_Transparent> to false. You can then drag the window horizontally, and then reset those values to turn transparency back on and borders off.

## 3-Pet Window
![image](https://github.com/user-attachments/assets/84a22d15-6ee4-477e-9ef2-6c1e72ec095a)

The pet window can handle displaying 3 pets simultaneously. Designed to be transparent, but by default transparency is left off because it causes the button frames to disappear. Recommend turning transparency on or setting the alpha of the window to zero.

- Doesn't currently handle a 4th pet from Dragon Tooth.
- Pet buffs don't display properly.
- The purple colour is subject to change. I suck at choosing good colours.

**If you want the 3-pet window but don't want it with the btmpkdUI style then download the file in the Pet Window (Three Pets) folder and use that.**

## Map Window
![image](https://github.com/user-attachments/assets/1fc3fe61-eecc-4d62-89b9-29ab3239c960)

The map window is a *minimap*. It's designed to be open all the time and positioned in one of the four corners. It has nearly all of the default map functionality removed. The two buttons in the top right are height filter and reset map position. You can still look around the map by zooming in and out with mousewheel and dragging the map around. It's a very different experience from the default map.

- The map window has a **dark background**. It's designed to be used with https://github.com/xackery/eq-darkmodemaps.
- You will need to customise your player map arrow to change it from black to another colour of your choice. Do this by finding UI_CharacterName_thj.ini (where "CharacterName" is your character's name) in your THJ main install folder. Ctrl+f for MapViewWnd and change the MyColor RGB values to an RGB colour that stands out better.

## Chat Window

Chat window is simple, semi-transparent *without* titlebar. It's designed that way for me because I play with only two chat windows, one in the bottom left and one in the bottom right, and I never move them. If you are the kind of person who moves chat windows around or uses tell windows: open EQUI_ChatWindow and ctrl+f for <Style_Titlebar>false</Style_Titlebar> and set it to true.

- Don't forget to hit Alt+O and change your chat colours to non-terrible ones!

## Large Dialogue Window
![image](https://github.com/user-attachments/assets/c6257c3e-6a18-45ac-af4c-2b247a616bcc)

The large dialogue window is **intentionally broken**. It has been made small for the purpose of not having a giant window popup every time you use the Tearel teleports. This means some other things that use the large dialogue window (tutorials, etc.) will not display correctly, but that's okay because you only see them once when you turn them off, whereas you see the Tearel window all the time.

## Selector Window

The selector window has been replaced with a top bar that contains a gauge for AA experience, the number of unspent AAs, and a gauge for level experience. If the custom EQtype for power source experience ever gets added, I'll add this here as well. The button to toggle this on and off is Alt+W.

- There is a good chance this won't be sized correctly for your screen. You can try resizing it manually. Not sure what the immediate best fix is other than making multiple versions for different resolutions.

## Other Windows
![image](https://github.com/user-attachments/assets/c59eb692-83e7-4934-9f2e-74378a563f16)

Most windows that are not open all the time are simple and solid, so you can actually read the information on them. Not every window has been adjusted though, so there will be a lot of windows that might not display properly.

## Target Ring
![image](https://github.com/user-attachments/assets/72f319b7-25a1-4326-9b17-7dead9ee4907)

A simple, minimalist target ring.

# Troubleshooting

If a certain window is active but you can't see it anywhere, it might be displaying offscreen. Go to UI_CharacterName_thj.ini (where "CharacterName" is your character's name) in your THJ main install folder, search for the name of the window (for example "BuffWindow") and look for any X or Y values that might be outside the range of your resolution. Set them back to a position inside your resolution and restart EQ.

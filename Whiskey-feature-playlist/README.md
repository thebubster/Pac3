# Whiskey Music Player [WIP]

![icon](https://i.imgur.com/FU5C3q3.png)

**Before you use it:** This project is still a work in progress!  
A lot of the features might not be implemented yet or might have bugs which make them unusable!

---

**Whiskey** is a **Music Player** made for use with the addon [**Starfall Ex**](https://github.com/thegrb93/StarfallEx).  
It will feature an advanced UI to simplify it's use and make it's features easily accessible.

## Contents

- [Current Status](#current-status)
- [Usage](#usage)
  - [Adding Music](#adding-music)
  - [Playing Music](#playing-music)
  - [Chat Commands](#chat-commands)
- [Downloading](#downloading)
- [FAQ](#frequently-asked-questions)

---

## Current Status

The music player is still a work in progress and is being actively worked on.  
It is in a useable state but some things may change in the future.

### Planned features

- Streaming
- Sharing

---

## Usage

### Adding Music

To add music you'll need to open the **Add Music** tab.  
<img src="https://i.imgur.com/kQM5MYg.png" width=32 height=32>

In that tab, there are three fields you can fill to add music.

Since these fields require text, they are part of the rare inputs that you can't click on.  
To input text, you'll need to use the specified commands in chat. (Refer to [Chat commands](#chat-commands))

These fields and commands are:

| Field  | Command            | Description             |
|--------|--------------------|-------------------------|
| Title  | `!title <title>`   | The title of the music  |
| Author | `!author <author>` | The author of the music |
| URL    | `!url <url>`       | The url for the music   |

Upon entering the URL, the music player will attempt to fetch the music.  
You'll only be able to save if the link is valid and you will be notified of it's status.  

#### Note

The urls used by this music player need to be **direct links** to an **mp3** file.  
It's the same limitation as **Wiremod E2's Streamcore** links.  
This means that **YouTube** links will not work.

You can use websites such as **Dropbox** or **Google Drive** to save mp3s and create direct links.

### Playing Music

To play music you have added, head over to the **Playlist** tab.  
<img src="https://i.imgur.com/CSvesH0.png" width=32 height=32>

There you can select music that you've added and add it to the Currently Playing list.  
This list acts as a queue and music will not play automatically if one is already playing.

### Chat Commands

Chat commands can be used to interact with the music player.  
They can be sent in global or team chat.  
All commands use the same prefix `!`

While most of the music player is useable by clicking on the screen, these chat commands are still implemented and will probably always be there.

| Command     | Description                                  |
|-------------|----------------------------------------------|
| !play url   | Play a music from the given URL              |
| !play       | Toggles pause on the currently playing music |
| !pause      | Pauses the music but can also unpause        |
| !unpause    | Unpauses the music                           |
| !volume vol | Sets the volume of the music (1 being 100%)  |

---

## Downloading

To download the music player, make sure you are on the `main` branch.  
![main-branch](https://i.imgur.com/KsjsOsv.png)

Then select **Download ZIP** in the **Code** dropdown:  
![download-button](https://i.imgur.com/eIQ69X7.png)

Once downloaded, open the `zip` file.  
There should be another folder inside called `Whiskey-main`. This is the file you want.  
Then go to your Starfall data folder (`GarrysMod/garrysmod/data/starfall`) and drop the `Whiskey-main` folder in there.  
You can rename the folder (Like removing the `-main` part) but it is not necessary.

Once this is done, you can open your starfall editor in-game and you should be able to find the folder you added.  
If you don't, try pressing the refresh button at the bottom left:  
![refresh-button](https://i.imgur.com/Bw3bDOm.png)

## Frequently Asked Questions

<br>

> My music's URL is not valid but the link is!

If you are using a link to a **YouTube** video, know that those links aren't supported. (Refer to [Adding Music](#adding-music))

<br>

> My CPU Quota keeps exceeding!

- If you are the owner of the chip:  
The allowed CPU Quota should already be higher than for the chips of other players.  
You can increase it using the command `sf_timebuffer_cl_owner <quota>` in console.  
The `quota` argument is between 0 and 1, 0 being 0% of your cpu time and 1 being 100% of your cpu time.  
***NEVER*** set your allowed quota to 1 (I don't even recommend going above 0.1).  
This can potentially lead to your game being in a frozen state until you restart it.  
The default quota is `0.015`

- If you are using the chip of someone else:  
The default cpu quota for other player's chips is lower than for yours which is why you might encounter this error.  
You can increase it by using the `sf_timebuffer_cl <quota>` command in console.  
As explained above, the quota is between 0 and 1, although it should never be set to 1.  
The default quota is `0.006`

If increasing your allowed quota didn't fix the problem, unfortunately there isn't much that can be done.  
Due to the code running client side, the only other solution would be to get a computer with better specs.  
But I don't think that's a good option just to listen to music with a Starfall Music Player.

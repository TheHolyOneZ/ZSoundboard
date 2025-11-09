# ZSoundboard
**ZSoundboard** is a Discord bot that allows users to upload and play custom audio files (MP3/MP4) in voice channels. Each user gets their own personal soundboard with statistics tracking, a queue system for multiple users, and comprehensive admin controls.

> 💡 **Built for the Zygnal Ecosystem — to download and use this extension, you must be part of the Zygnal Ecosystem.**  
> This extension (cog) is part of the **Zygnal Ecosystem** and is only available through its supported platforms.  
> You can use it with:  
> - The **[Discord Bot Framework](https://github.com/TheHolyOneZ/discord-bot-framework)** — ideal for developers who want full control and flexibility *(includes an integrated extension marketplace)*, or  
> - The **[ZygnalBot](https://zygnalbot.de)** — a prebuilt, plug-and-play Discord bot *(also includes an integrated extension marketplace)*.  
>
> Browse and install extensions at [zygnalbot.com/extension](https://zygnalbot.com/extension).  
> For help or community discussions, join us on Discord: [discord.gg/sgZnXca5ts](https://discord.gg/sgZnXca5ts)

# ZSoundboard 


## 📖 Overview

**ZSoundboard** is a Discord bot that allows users to upload and play custom audio files (MP3/MP4) in voice channels. Each user gets their own personal soundboard with statistics tracking, a queue system for multiple users, and comprehensive admin controls.

### What is this extension for?
- Play custom sound effects in voice channels
- Create your own library of sounds
- Share sounds with your server members
- Manage audio playback with an automatic queue system
- Track usage statistics and play counts

---

## ✨ Features

### For Regular Users:
- **Personal Soundboard**: Upload and manage your own sounds (MP3/MP4 files)
- **Easy Management**: Upload, edit, delete, and play sounds through an interactive UI
- **Search**: Find your sounds quickly with the built-in search feature
- **Statistics**: Track how many times each sound has been played
- **Smart Queue**: Automatically queues sounds when multiple people want to play at once
- **Real-time Notifications**: Get notified when it's your turn in the queue

### For Server Admins:
- **Role-Based Permissions**: Control who can use the bot with role restrictions
- **Channel Restrictions**: Limit bot usage to specific text and voice channels
- **Custom Limits**: Set sound limits and cooldowns per server
- **Enable/Disable**: Toggle the bot on/off for your server
- **Role-Based Sound Limits**: Give different roles different sound storage limits

### For Bot Owners:
- **Global Control**: Enable/disable the bot across all servers
- **File Size Limits**: Set maximum file size limits with automatic enforcement
- **Guild Whitelist**: Control which servers can use the bot when globally disabled
- **Statistics**: View bot-wide usage statistics
- **Automatic Cleanup**: Automated file size checking with user notifications

---

## 🚀 Getting Started

### Step 1: First Time Setup
1. Make sure you're in a voice channel
2. Type `!zsound` or `/zsound` in any text channel
3. You'll see your personal soundboard panel

### Step 2: Upload Your First Sound
1. Open your soundboard with `!zsound`
2. Click the **"📤 Upload Sound"** button
3. Upload an MP3 or MP4 file in the chat (you have 60 seconds)
4. Click the **"Enter Details"** button when it appears
5. Fill in the sound name and description
6. Click **Submit**

### Step 3: Play a Sound
1. Go to the **"🎵 My Sounds"** tab
2. Select a sound from the dropdown menu
3. Click the **"▶️ Play"** button
4. The bot will join your voice channel and play the sound!

---

## 👤 User Commands

### `/zsound` or `!zsound`
Opens your personal soundboard control panel.

**What you can do:**
- **🏠 Overview Tab**: See your stats, what's currently playing, and queue status
- **🎵 My Sounds Tab**: Browse, search, and manage all your sounds
- **📊 Statistics Tab**: View detailed stats about your sound usage
- **⚙️ Settings Tab**: See your sound limit and current usage

**Buttons:**
- **📤 Upload Sound**: Add a new sound to your collection
- **▶️ Play**: Play the selected sound (must select from dropdown first)
- **✏️ Edit**: Change the name/description of a sound
- **🗑️ Delete**: Remove a sound from your collection
- **⏹️ Stop Bot**: Immediately stop playback and disconnect the bot
- **🔍 Search**: Search for sounds by name
- **🔄 Refresh**: Reload the panel to see updates
- **❌ Close**: Close the panel

**Requirements:**
- Must be in a voice channel to play sounds
- Need appropriate permissions (if admins set role restrictions)
- Must be in an allowed text channel (if admins set channel restrictions)

---

## 👑 Admin Panel

### `/zsound_admin` or `!zsound_admin`
Opens the server administration panel for the soundboard.

**Who can use this:**
- Server Administrators (always have access)
- Users with roles added to "Admin Roles" list

### Admin Panel Tabs:

#### 🏠 Main Tab
**Quick Actions:**
- **✅ Enable Bot**: Turn on the soundboard for your server
- **❌ Disable Bot**: Turn off the soundboard for your server
- **🔄 Refresh**: Reload the panel

**What you see:**
- Current bot status (Enabled/Disabled)
- Global cooldown setting
- Sound limit per user
- List of admin roles
- List of user roles
- Allowed text channels
- Allowed voice channels

#### 👥 Roles Tab
**Configure role-based access:**
- **Add Admin Role**: Give a role admin panel access
  - Click the button
  - Enter the role ID or @mention the role
  - That role can now access `/zsound_admin`

- **Remove Admin Role**: Remove admin access from a role

- **Add User Role**: Set which roles can use the bot
  - When you add user roles, ONLY those roles can use `/zsound`
  - Leave empty to allow everyone

- **Remove User Role**: Remove a role from the allowed list

**Use Case Example:**
You want only members with the "DJ" role to use the soundboard:
1. Go to Roles tab
2. Click "Add User Role"
3. Enter your DJ role ID
4. Now only DJ role members can use `/zsound`

#### 📺 Channels Tab
**Control where the bot can be used:**
- **Add Text Channel**: Only allow `/zsound` in specific text channels
  - Great for keeping bot commands organized
  - Leave empty to allow all text channels

- **Remove Text Channel**: Remove a channel from the allowed list

- **Add Voice Channel**: Only allow sound playback in specific voice channels
  - Useful for dedicated music/soundboard channels
  - Leave empty to allow all voice channels

- **Remove Voice Channel**: Remove a channel from the allowed list

**Use Case Example:**
You only want sounds played in your "Soundboard" voice channel:
1. Go to Channels tab
2. Click "Add Voice Channel"
3. Enter the voice channel ID
4. Sounds can now only be played there

#### ⚙️ Settings Tab
**Fine-tune bot behavior:**
- **Set Cooldown**: Time in seconds between sound plays per user
  - Default: 5 seconds
  - Prevents spam
  - Applies per user, not globally

- **Set Sound Limit**: Maximum number of sounds each user can upload
  - Default: 10 sounds
  - Keeps storage manageable

- **Set Embed Timeout**: How long (in minutes) the panel stays interactive
  - Default: 10 minutes
  - After timeout, panels become non-interactive

**Use Case Example:**
Your server is very active and you want to prevent spam:
1. Go to Settings tab
2. Click "Set Cooldown"
3. Enter "10" for 10 second cooldown
4. Users must wait 10 seconds between plays

---

## 🔧 Owner Panel

### `!zsound_owner`
Opens the bot-wide control panel (bot owner only).

**Who can use this:**
- Only the bot owner (defined in bot configuration)

### Owner Panel Tabs:

#### 🏠 Main Tab
**Global bot control:**
- **Global Status**: Shows if bot is enabled or disabled everywhere
- **Max File Size**: Current maximum file size for uploads
- **Enabled Guilds**: Number of servers on the whitelist
- **Total Guilds**: Total servers using the bot

**Quick Actions:**
- **✅ Enable All**: Allow all servers to use the bot
- **❌ Disable All**: Block all servers except whitelisted ones

#### ⚙️ Settings Tab
**Configure global settings:**
- **Set Max File Size**: Change the maximum allowed file size (in MB)
  - Affects all new uploads
  - Triggers automatic check of existing files
  - Users are notified if their sounds are deleted

**Use Case Example:**
You need to reduce storage and set max size to 3MB:
1. Go to Settings tab
2. Click "Set Max File Size"
3. Enter "3"
4. All sounds over 3MB will be automatically deleted
5. Users get DM notifications with sound details

#### 📊 Stats Tab
**View bot-wide statistics:**
- Total number of guilds using the bot
- Total number of users with sounds
- Total sounds uploaded across all servers
- Total plays across all sounds
- Average sounds per user
- Average plays per sound

**Use Case:**
Check how popular the bot is and monitor usage patterns

#### 🔧 Tools Tab
**Advanced management:**
- **Global Status Display**: See if bot is globally enabled/disabled
  - Shows whitelist explanation when disabled
  - Lists all whitelisted guilds

- **Enable Guild**: Add a server to the whitelist
  - Only matters when globally disabled
  - That server can use the bot even when others can't

- **Disable Guild**: Remove a server from whitelist

- **Check File Sizes**: Manually trigger file size check
  - Scans all sounds in all servers
  - Deletes oversized files
  - Sends notifications to users

**Use Case Example:**
You want to temporarily disable the bot everywhere except your test server:
1. Go to Main tab, click "Disable All"
2. Go to Tools tab, click "Enable Guild"
3. Enter your test server's ID
4. Only your test server can now use the bot

---

## 📋 Queue System

### How It Works

When multiple people want to play sounds simultaneously, the bot uses a **per-guild queue system**:

1. **First User**: Sound plays immediately
   - Message: "▶️ Playing **[sound]** now..."

2. **Additional Users**: Sound added to queue
   - Message shows: Position number, how many sounds ahead, notification promise
   - Example: "📋 Position: #3, You have 2 sounds ahead, You'll be notified when it's your turn!"

3. **When Your Turn Arrives**: You get notified
   - Message: "🎵 **Your turn!** Now playing: **[sound]**"

4. **Auto-Progression**: Queue automatically moves to next sound when current finishes

5. **Stop Function**: The stop button clears the queue and disconnects the bot

### Queue Features:
- **Per-Guild**: Each server has its own independent queue
- **Smart Detection**: Knows if something is playing before adding to queue
- **Position Tracking**: Always know where you are in line
- **Auto-Cleanup**: Bot disconnects when queue is empty
- **Force Stop**: Stop button clears everything immediately

---

## 🔐 Permissions & Roles

### Understanding the Permission System

**There are 3 levels of access:**

1. **Regular Users**
   - Can use `/zsound` to manage their own sounds
   - Restricted by admin settings (if configured)

2. **Server Admins**
   - Can use `/zsound_admin` to configure the bot
   - Server Administrators always have access
   - Additional roles can be granted admin access

3. **Bot Owner**
   - Can use `!zsound_owner` for global control
   - Only the bot owner has this access

### How Restrictions Work:

#### User Role Restriction:
- **If NO user roles are set**: Everyone can use the bot
- **If user roles ARE set**: ONLY those roles can use `/zsound`
- Admins are NOT affected by user role restrictions

#### Channel Restrictions:
- **Text Channels**: If set, `/zsound` only works in those channels
- **Voice Channels**: If set, sounds only play in those channels
- Empty = no restrictions

#### Finding Role/Channel IDs:
1. Enable Developer Mode in Discord (User Settings > Advanced > Developer Mode)
2. Right-click the role/channel
3. Click "Copy ID"
4. Paste the ID into the bot panel

---

## 🔍 Troubleshooting

### "❌ Soundboard is disabled in this server"
**Cause**: Either globally disabled or server admin disabled it
**Solution**: 
- Ask server admin to use `/zsound_admin` and enable the bot
- If globally disabled, ask bot owner to enable your server in `!zsound_owner`

### "❌ You don't have permission to use this command"
**Cause**: User roles are set and you're not in one of them
**Solution**: Ask server admin to add your role to the user roles list

### "❌ This command cannot be used in this channel"
**Cause**: Text channel restrictions are active
**Solution**: Use the command in an allowed text channel, or ask admin to add your channel

### "❌ You cannot use the soundboard in this voice channel"
**Cause**: Voice channel restrictions are active
**Solution**: Join an allowed voice channel, or ask admin to add your channel

### "⏱️ Cooldown active! Wait X seconds"
**Cause**: You played a sound too recently
**Solution**: Wait for the cooldown to finish

### "❌ You have reached your sound limit (X)"
**Cause**: You've uploaded the maximum allowed sounds
**Solution**: Delete some sounds, or ask admin to increase the limit

### "🗑️ Sound Deleted - File Size Limit"
**Cause**: Bot owner changed max file size and your sound exceeded it
**Solution**: Re-upload a smaller version of the sound

### Sound won't play / Bot is stuck
**Solution**: 
1. Click the **"⏹️ Stop Bot"** button
2. This disconnects the bot and clears the queue
3. Try playing again

### Bot won't join voice channel
**Check**:
- Are you in a voice channel?
- Does the bot have permission to join/speak in that channel?
- Is the voice channel restricted? (check admin panel)

---

## 📊 File Specifications

### Supported Formats:
- **MP3** (recommended)
- **MP4** (automatically converted to MP3)

### File Size:
- Default: 5MB maximum
- Configurable by bot owner
- Checked automatically every hour
- Users notified if sounds are deleted

### Best Practices:
- Use MP3 format for best compatibility
- Keep files under 2MB for quick playback
- Use clear, descriptive names for sounds
- Add descriptions to remember what each sound is

---

## 💡 Tips & Tricks

1. **Organize Your Sounds**: Use clear names and descriptions so you can find them easily

2. **Use Search**: If you have many sounds, use the search feature to find them quickly

3. **Check Stats**: See which sounds are most popular in the Statistics tab

4. **Be Courteous**: Remember there's a queue system - wait your turn!

5. **Test Uploads**: Make sure your sound plays correctly before sharing with others

6. **Regular Cleanup**: Delete sounds you no longer use to stay under your limit

7. **Use Stop Wisely**: Only use the stop button when necessary - it clears the entire queue

---

## 📞 Support

For issues, bugs, or feature requests:
- Join the ZygnalBot Discord Server
- Check this guide for common solutions
- Make sure the bot has proper Discord permissions

**Made by TheHolyOneZ / ZSoundBoard**

---

## 📜 Quick Reference Card

### Commands:
- `/zsound` - Open soundboard panel
- `/zsound_admin` - Open admin panel (admins only)
- `!zsound_owner` - Open owner panel (bot owner only)

### Common Tasks:
- **Upload sound**: `/zsound` > Upload Sound button
- **Play sound**: `/zsound` > My Sounds > Select > Play
- **Stop bot**: `/zsound` > Stop Bot button
- **Set restrictions**: `/zsound_admin` > Roles/Channels tabs
- **Change limits**: `/zsound_admin` > Settings tab
- **Global control**: `!zsound_owner`

### Permission Levels:
1. Users - Can upload and play sounds
2. Admins - Can configure server settings
3. Owner - Can configure global settings

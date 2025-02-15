﻿---
id: settings
title: Rythm's Settings and How They Work
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

:::info note
You must have either the `Administrator` or `Manage Server` permissions to change any of Rythm's settings in your server.
:::

These are the options you can access through Rythm’s settings menu.

1. To access this menu use the command `!settings`.<br/>

   ![Settings](/img/docs/settings/settings.png)
2. Rythm should then display a menu showing the settings that can be changed.
3. For more information on a setting just type: `!settings <Setting-Name>`.
   - **Example:** `!settings blacklist`<br/>

   ![SettingsBlacklistTest](/img/docs/settings/settings-blacklist-test.png)

## Prefix
---
The prefix is what you use in order to tell Rythm what to do.
If you ever forget the prefix for your server, you can always mention Rythm to find your prefix.<br/>

![Mention to get prefix](/img/docs/settings/prefix.png)

### Changing the Prefix
:::info note
- You must have either the `Administrator` or `Manage Server` permissions to change Rythm's prefix in your server.
- Be sure to not include the brackets (`<>`/`[]`/`{}`) when setting the prefix, as they'll become part of the prefix.
:::

To change the prefix to anything you like, follow the steps below:
  - Mention Rythm to get its current prefix.
  - Use the command `!settings prefix <NewPrefix>`
(Note: Replace `!` with your current prefix and replace `<NewPrefix>` with your desired prefix)

<Tabs
  defaultValue="e1"
  values={[
    {label: 'Example 1', value: 'e1'},
    {label: 'Example 2', value: 'e2'},
  ]}>
  <TabItem value="e1"> If the current prefix is <code>!</code> and you want to change it to <code>$</code>, do: <br/>
  <code>!settings prefix $</code><br/><br/>
    <img src="/docs/img/docs/settings/prefix-example-1.png" alt="example-1"/>
  </TabItem>
  <TabItem value="e2"> If the current prefix is <code>></code> and you want to change it to <code>r!</code>, do: <br/>
  <code>>settings prefix r!</code><br/><br/>
    <img src="/docs/img/docs/settings/prefix-example-2.png" alt="example-2"/>
  </TabItem>
</Tabs>

If you are unable to use the current prefix (non-ASCII characters, multiple bots having the same prefix,...), you can also use mention as a prefix to change your prefix to something else: `@Rythm#3722 settings prefix <NewPrefix>`
  - **Example:** `@Rythm#3722 settings prefix -`

  ![Change Prefix Example 3](/img/docs/settings/prefix-example-3.png)

## Blacklist
---
:::caution
   - This only applies to text channels.
   - This only prevents music commands from being used. Other commands such as `!ping`, `!help` still work normally.

To completely disallow Rythm from being used within the voice channel, or to get rid of those blacklist messages, you have to use the Discord's permission system, as explained [here](/permissions#block-rythm-completely-from-textvoice-channels).
:::

The blacklist setting allows you to control which text channels Rythm is allowed to be used in.

To disallow Rythm from being used within certain text channels, use the following command:<br/>
`!settings blacklist #channels`

You can provide multiple channels for quicker blacklisting.

**Example**: If you wanted to blacklist channels named `#chat`, `#gaming` and `#international`, use `!settings blacklist #chat #gaming #international`<br/>

![Blacklist text channel example](/img/docs/settings/blacklist-text-channel-example.png)

To unblacklist the channels, run the command again.

## AutoPlay
---
:::info Note
This is a Premium-only feature. You will need to [subscribe](https://rythm.fm/premium) in order to activate this.
:::

AutoPlay plays a song from a pre-defined playlist when there is nothing currently playing.

To setup AutoPlay, provide a playlist using the following command:<br/>
`!settings autoplay playlist-link`

**Example**: If you wanted to set autoplay to be your playlist, use `!settings autoplay https://www.youtube.com/playlist?list=PLX0RQHkBDj88WRGrql2OKgVp-aXdPInhe `<br/>

![Autoplay example](/img/docs/settings/autoplay-example.png)

:::info
- To make it not repetitive every time Rythm joins the voice channel, the songs will be played in shuffle.
- Queuing a song will skip the current AutoPlay song and play the one you requested.
:::
## Announce Songs
---
When enabled, Rythm will send a message to announce when a song has started playing.

:::caution
The messages go to the channel in which the last command was used before it announces.
:::

To enable or disable song announcements, use the following command:<br/>
`!settings announcesongs yes/no`

**Example**: If you want announcements when a song plays, use `!settings announcesongs yes`<br/>

![Announce songs example](/img/docs/settings/announce-songs-example.png)

## Max Queue Length
---
This limits how many songs can be in the queue at once.

To change this limit, use the following command:<br/>
`!settings maxqueuelength <10-10000>`

You can also set it back to default:<br/>
`!settings maxqueuelength disable`

**Example**: If you want to limit the queue to 10 songs total, use `!settings maxqueuelength 10`<br/>

![Max queue length example](/img/docs/settings/max-queue-length-example.png)

## Max User Songs
---
:::info note
Users with `DJ` role or `Manage Channels` permission bypass this restriction.
:::

This limits how many songs a user can have in queue at once.

To change this limit, use the following command:<br/>
`!settings maxusersongs <1-10000>`

You can also set it back to default:<br/>
`!settings maxusersongs disable`

**Example**: If you want to limit the amount of songs a user can queue to 1, use `!settings maxusersongs 1`<br/>

![Max user songs example](/img/docs/settings/max-user-songs-example.png)

## Duplicate Song Prevention
---
This prevents duplicated songs from being played.

To enable or disable this setting, use the following command:<br/>
`!settings preventduplicates yes/no`

**Example**: If you want to prevent duplicates of songs from being played, use `!settings preventduplicates yes`<br/>

![Prevent duplicates example](/img/docs/settings/prevent-duplicates-example.png)

## Default Volume
---
:::info Note
This is a Premium-only feature. You will need to [subscribe](https://rythm.fm/premium) in order to activate this.
:::

**This is not the same as `!volume`.** This is for changing the default volume for new listening sessions. If you need to change the volume for the current listening session, use `!volume <1-200>`, for example: `!volume 50`

To change the default volume for when you summon Rythm to a voice channel, use the following command:<br/>
`!settings defaultvolume <1-200>`

**Example**: If you wanted the volume to be 25 when someone summons Rythm, use `!settings defaultvolume 25`<br/>

![Default volume example](/img/docs/settings/default-volume-example.png)

## DJ Only Playlists
---
This setting allows you to control if only DJs can queue playlists, or if everyone can.

To enable or disable DJ only playlists, use the following command:<br/>
`!settings djplaylists yes/no`

**Example**: If you want only DJs to queue playlists, use `!settings djplaylists yes`<br/>

![DJ only playlists example](/img/docs/settings/dj-only-playlists-example.png)

## DJ Only Mode
---
This setting allows you to control if only DJs can control Rythm, or if everyone can.

To enable or disable DJ only mode, use the following command:<br/>
`!settings djonly yes/no`

**Example**: If you want only DJs to use Rythm, use `!settings djonly yes`<br/>

![DJ only mode example](/img/docs/settings/dj-only-mode-example.png)

## DJ Role
---
This setting allows you to control which role is DJ.

:::caution
Any roles named '<b>DJ</b>' and anyone with the `Manage Channels` permission will always be able to use Rythm as a DJ regardless of this setting.
:::

To change the DJ role, use the following command:<br/>
`!settings djrole role`/`!settings djrole @role`

**Example**: If you want to give a role named `Special` DJ without assigning a new role, use `!settings djrole Special`<br/>

![DJ role example](/img/docs/settings/dj-role-example.png)

### Resetting your DJ Role
---
If you want to reset this setting, use `!settings djrole DJ`. This will reset it back to default regardless of if a role named '**DJ**' exists.<br/>

![DJ role reset example](/img/docs/settings/dj-role-reset-example.png)


## Always Playing
---
:::info Note
This is a Premium-only feature. You will need to [subscribe](https://rythm.fm/premium) in order to activate this.
:::

This setting allows the bot to stay in the voice channel 24/7, ready to play whenever you join.

To enable or disable Always Playing mode, use the following command:<br/>
`!settings alwaysplaying yes/no`

![Always playing example](/img/docs/settings/always-playing-example.png)

## Reset
---
If you want to reset **all** settings back to their defaults, you can use `@Rythm#3722 settings reset` or `!settings reset`, then reply with `yes` when Rythm prompts you.<br/>

![Reset example](/img/docs/settings/reset-example.png)

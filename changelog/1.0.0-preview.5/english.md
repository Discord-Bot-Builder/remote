# Bot Update

#### 1.0.0-preview.5 • 2024-09-28

---

![Image](https://clan.akamai.steamstatic.com/images/35455752/df2b25249eb7ecd5bedc40911b85bfc2998b40a5.jpg)

### **Hey Builders!**

This is the first update related to the second phase of preview releases, where the new features are more about the bot this time. With that said, let's talk about the new DBB Bot v2.0:
<br>
<br>
<br>

![Image](https://clan.akamai.steamstatic.com/images/35455752/6fb174eddd53ca5c76fee05d29e4c541d88fccb4.jpg)

## **DBB Bot 2.0**

The new _bot.js_ file was made from scratch to offer a better performance and fidelity, and is now smarter than ever at detecting issues and having new mechanics. Below there are some of those new features:
<br>
<br>
<br>

![Image](https://clan.akamai.steamstatic.com/images/35455752/09598f68beba9f45e21383e706350207c8cbe5b1.jpg)

## **New Mechanics**

**Less action, or not...**
<br>

DBB Bot v2.0 is smart to the point of being able to get values from blocks that had no direct connection previously (via the _Action_ ports).<br>
It's recommended that you continue connecting the blocks that may take longer to process and return the value (also known as asynchronous blocks), such as those that fetch data from the internet, read files, etc...<br>
If you don't feel confident with this new logic, you can still continue connecting all the _Action_ ports as usual.
<br>
<br>
<br>

![Image](https://clan.akamai.steamstatic.com/images/35455752/4d165a08716f3641988da4cb836576f809839dfb.jpg)

## **Required Input Warning**

**It happens to the best of us**
<br>

In the console, it will warn you whenever it runs a block with a required input not connected, showing you all the information to help you find the target input.
<br>
<br>

---

![Image](https://clan.akamai.steamstatic.com/images/35455752/5bc661cc78a59d0129baece438eaabbdc9beefda.jpg)

## **New Command/Interaction Blocks**

**And more other blocks...**
<br>

Finally added slash commands to DBB! <u>The old prefix command system is obsolete and it's recommended (even by Discord) to switch to slash commands or other types of commands/interactions.</u>
<br>
<br>
<br>

![Image](https://clan.akamai.steamstatic.com/images/35455752/fd8b5f8a53aababe6ec1f18a7119ab78abf52697.gif)

## **Multiselect Option**

**Being able to select more than one option**
<br>

This new option type provides the ability to get a list of selected options, ordered by the user, and the block developer can even set:

-   _allowUserOptions = false_ - Whether to allow the user to write and select custom options
-   _duplicates = false_ - Whether to allow the user to select the same option more than once
    <br>
    <br>

---

![Image](https://clan.akamai.steamstatic.com/images/35455752/85953c028c9db8b8595adfde0875ea4d4ee92f1a.jpg)

## **Better Search**

**Less scrolling and more accurate results at the top**
<br>

Item Browser has a better algorithm to search for better overall results.
<br>
<br>
<br>

![Image](https://clan.akamai.steamstatic.com/images/35455752/b44be30eaf4d1f7b8b7abadf0a74a39bd2394dab.gif)

## **Create Block by Dragging Wire**

**Less wires to connect**
<br>

Instead of always right-clicking to open the Item Browser, you can also drag a wire to an empty spot to open it and then wiring the newly placed block automatically.
<br>
<br>

---

## **Changelog**

-   Added DBB Bot v2.0
-   Slightly better overall performance
    -   Added new mechanics (see above)
    -   Added Required Input Warning
    -   Beautified console messages
    -   Added command/interaction-related blocks
    -   Fixed and improved audio-related blocks
    -   Added _executedFrom_ property to block's _cache_
    -   Added new tools for block developers:
        -   _setDependency(dependencyId: string, blockName: string, data: unknown)_
        -   _eraseConsole()_
        -   _runNextBlock(outputId: string, cache: BlockCache, multiPortIndex?: number)_
        -   _GetInputValueAsync(inputId: string, cache: BlockCache, explicitValue?: boolean, defaultValue?: unknown)_
        -   _isInputConnected(inputId: string, cache: BlockCache, multiPortIndex?: number)_
        -   _isOutputConnected(outputId: string, cache: BlockCache, multiPortIndex?: number)_
        -   _findWorkspaces(searchType: "id" | "title" | "description", searchValue: string)_
-   Added _MULTISELECT_ and _TEXT_LINE_ option types for blocks
-   Added the ability to add a description to each option in a _SELECT_ block option type
-   Forced _bot.js_ file being updated on the first bot run
-   Removed "Set Bot Main Prefix" and "Set Bot Owners" menu options as they are obsolete
-   Improved "Set Bot Intents" menu option
-   Updated "Generate Bot Invite" menu option to support a User-Installable App
-   Added the ability to create items by dragging and dropping the wire into an empty spot
-   Improved the search results of Item Browser
-   Made Note avoiding being selected when making a selection area within it
-   Added "Animated Item Preview" and "Oversimplify Items" settings to _Workspace_ settings page
-   Added "Add starting block when creating workspace" setting to _Advanced_ settings page
-   Made font size of Note's title increase when zooming out
-   Fixed the font size of _SELECT_ block option being bigger than before
-   Fixed wires disconnecting when switching between single port and multiport
-   Added Steam Language API support
-   Added Japanese, Korean and Thai translations by npcdotcom (NPC), Svelion, muleu (Null) and npoka (Simba 🦁)
    <br>

### **Added/Updated Blocks**

<details>
    <summary>Show Details</summary>
    <ul><li>await_message_component
     <li>boolean
     <li>bot_initialization_event
     <li>button_component
     <li>clear_server_queue
     <li>command_interaction_event
     <li>control_bot_audio
     <li>control_variable
     <li>create_action_row
     <li>create_command_advanced
     <li>create_context_menu
     <li>create_modal
     <li>create_select_menu_component
     <li>create_slash_command
     <li>defer_interaction_reply
     <li>delete_interaction_reply
     <li>delete_variable
     <li>discord_audio_player_dependency
     <li>discord_commands_manager_dependency
     <li>edit_interaction_reply
     <li>emitter
     <li>get_audio_info
     <li>get_bot_audio_info
     <li>get_bot_info
     <li>get_interaction_info
     <li>get_slash_command_options
     <li>get_variable
     <li>interaction_create_event
     <li>join_voice_channel
     <li>leave_voice_channel
     <li>loop_server_queue
     <li>modal_text_input
     <li>play_audio
     <li>remove_audio_from_server_queue
     <li>reply_interaction
     <li>restrict_interaction
     <li>select_menu_option
     <li>send_message
     <li>send_webhook_message
     <li>set_audio_volume
     <li>shuffle_server_queue
     <li>skip_audio
     <li>slash_command_option
     <li>text_line</ul>
</details>
    <br>
    <br>
    <br>

_MrGold - DBB Developer_<br>
[DBB Discord Server](https://discord.gg/PAzxTDw)<br>
[Unofficial DBB Website](https://dbb.software/)

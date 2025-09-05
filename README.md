Of course. Here is the fully complete and updated README for Kinexus, including a detailed breakdown and a full example of the `story.json` file format.

***

<p align="center">
    <a href="https://discord.gg/HMYpnPzbTm"><img src="https://img.shields.io/badge/Chat%20with%20us%20on%20Discord--blue?style=social&logo=discord" alt="Chat" title="Chat"></a>
    <a href="https://twitter.com/tintwotin"><img src="https://img.shields.io/twitter/follow/tintwotin" alt="Follow us on X" title="Follow on X"></a>
<p>

<h1 align="center">KINEXUS</h1>

**Kinexus** is a powerful zero-code tool for creating, styling, and exporting choice-based narrative games, interactive fiction, and interactive graphic novels. It runs entirely in your web browser, providing a complete workflow from writing your story to packaging a distributable ZIP file for platforms like [itch.io](https://itch.io/).

<img width="1907" height="958" alt="image" src="https://github.com/user-attachments/assets/c9fb771f-5a07-4be4-aa73-8294e3c21879" />

## Try It

<div align="left">
  <a href="https://tin2tin.github.io/Kinexus/">Open Kinexus</a><br><br>
</div>

<div align="left">
  <a href="https://tintwotin.itch.io/cyoa-test?secret=G3dumLNBVgg2migNyde3jOYm8">Try the example game</a><br><br>
</div>

Library of Kinexus Games: [Itch](https://itch.io/c/6268695/interactive-cinematic-fiction-created-in-kinexus)

An example project to download, unzip and open with Kinexus: [The_Last_Broadcast](https://github.com/tin2tin/CYOA_Studio/raw/refs/heads/main/example_the_last_broadcast.zip)

## Features

*   **Visual Story Creation:**
    *   A rich text editor for writing your narrative.
    *   **Markdown Text Formatting:** Use simple markdown like `**bold**`, `*italics*`, `~~strikethrough~~`, `` `inline code` ``, and `[links](https://example.com)` to style your story text.
    *   Easily add, edit, and link choices between scenes.
    *   **Integrated Generative AI Tools (Powered by Pollinations.ai):**
        *   **Image Generation:** Create and add unique artwork for your scenes directly within the editor.
        *   **Text Processing:** Use AI to rewrite or expand upon your story text.

*   **Advanced Story Logic:**
    *   **Conditional Choices:** Show or hide choices based on the player's actions, creating dynamic and reactive storylines.
    *   **Variable Management:** Create and track boolean (true/false) variables to manage game state, inventory, character stats, or unlock secret paths.

*   **Interactive Story Map:**
    *   Dual navigation modes: a collapsible **Tree View** for visualizing story branches and a sortable **Scene List View** for quick management.
    *   Status icons instantly show the start scene, dead ends, orphan scenes, conditional choices, and scenes with media.
    *   Safely rename scenes with automatic link updating across all choices.
    *   Search and filter your scenes to quickly find what you need.

*   **Live Player & Preview:**
    *   Instantly playtest your game from the start or the current scene using the built-in player.
    *   Launch a full, clean preview of your project in a new browser tab at any time.
    *   **Modern Player UI:** The exported game features a clean, overlay-based UI with quick access to menu, sound toggle, save/load, and exit functions.

*   **Integrated Asset Management:**
    *   Select image and audio files from your computer using a file picker or by **dragging and dropping** them directly onto the input fields.
    *   The studio automatically copies them into your project folder on save, ensuring all asset paths are correct and ready for export.

*   **Powerful Style Editor:**
    *   Customize the visual theme of your game, including layout, colors, fonts, padding, background images, and even global background music. Your custom style is saved with the project.

*   **Batch AI Processing:**
    *   Automate image creation for all scenes that are missing one.
    *   Optionally use AI to automatically generate image prompts based on your scene's text.
    *   Globally add artistic suffixes (e.g., ", cinematic lighting, 4k") to all generated images.
    *   Includes tools to safely delete all image paths or all prompts from your project at once.

*   **One-Click Export:**
    *   Export your complete, playable project as a self-contained `.zip` file. This bundle includes the game, your custom theme, and all required assets, ready to be hosted online.
    *   The exported game is optimized for both desktop and mobile browsers.
    *   Export specific data, such as all AI image prompts, to a structured `.json` file for analysis or external use.

*   **Single-File, Zero Installation:**
    *   The entire studio is a single `.html` file. It runs directly in your browser with no installation, servers, or dependencies required.

*   **Local-First Project Management:**
    *   Works directly with folders on your computer via the File System Access API. Your project, including the story file and all assets, is saved locally, not in the cloud. The app tracks unsaved changes to prevent data loss.

## Screenshots

Style Template Editor

<img width="1905" height="957" alt="image" src="https://github.com/user-attachments/assets/b2fc925b-7f20-4211-86ee-560b6ab4a56a" />

Play Current

<img width="1919" height="956" alt="image" src="https://github.com/user-attachments/assets/0a544a00-f62a-4ffc-a3c9-0bb05e63eef2" />

Preview in Browser/Export as Standalone

<img width="1919" height="1040" alt="image" src="https://github.com/user-attachments/assets/4d73a9d1-35c6-4c93-9174-b546fe8f5126" />

Standalone Menu

<img width="1919" height="990" alt="image" src="https://github.com/user-attachments/assets/9efbb7b8-d471-4be1-8879-7bd51d8a3b7a" />

Story Map Navigator

<img width="602" height="740" alt="image" src="https://github.com/user-attachments/assets/95d27c3a-f76e-4f91-8477-587cdf92b8dd" />

Generate AI Image

<img width="1902" height="956" alt="image" src="https://github.com/user-attachments/assets/a9675323-7d5e-4180-919f-6de44f6719b1" />

AI Rewrite

<img width="1112" height="386" alt="image" src="https://github.com/user-attachments/assets/90ca296c-7d6e-4438-8eb8-c94dec5c84f5" />

Project Menu

<img width="639" height="566" alt="image" src="https://github.com/user-attachments/assets/6f484886-d95a-4a09-8451-fbbc8bbf9372" />

Project Text Editor

<img width="644" height="485" alt="image" src="https://github.com/user-attachments/assets/fd572ff7-0faf-44ab-905a-c15230054ec5" />


## How to Get Started

Creating your first game is a straightforward process. The app handles all the file and folder setup for you.

### 1. Create or Open a Project
First, open Kinexus in your browser. From the **Menu**, you have two options:
*   **New Project:** Creates a complete project folder for you, including sub-folders for `images` and `sounds`, and the main `story.json` file.
*   **Open Existing Project:** Lets you select a project folder you previously created.

### 2. Create Your Story
*   **Create Scenes:** Use the **round blue '+' button** above the scene list to create new scenes. Give them short, unique IDs (e.g., `start`, `cockpit`, `alien_encounter`).
*   **Navigate:** Click any scene in the Story Map to load it into the editor. Right-click a scene for more options, like **"Set as Start Scene"**.
*   **Edit Content:** Write your narrative in the "Story Text" area. You can use simple markdown for formatting, like `**bold**`, `*italics*`, and `[links](https://example.com)`. The formatting is visible in the live preview, the player, and the final exported game.
*   **Add Choices:** Click the **round blue '+' button** below the choices list. Write the text the player will see and select the target scene from the dropdown menu.

### 3. Create Dynamic Stories with Variables and Conditions
*   **Manage Variables:** Click the `{...}` button next to "Add Choice". In the modal, add new true/false variables to track game state (e.g., `has_key`).
*   **Set a Variable:** Create a choice and in its destination dropdown, select a variable (e.g., `var_has_key`). You can then set it to `true` or `false`. Leave the button text blank for a silent, automatic action.
*   **Add a Condition:** Click the condition icon (`→`) on any choice. In the new view, you can set the choice to only appear if a variable is true/false or if a specific scene has been visited.

### 4. Add Media (Image & Audio)
You have multiple ways to add media:
1.  **File Picker:** Click the **yellow folder icon** next to the "Image" or "Audio" field.
2.  **Drag & Drop:** Drag an image or audio file from your file explorer directly onto the text input field.
3.  **Generative AI (Images):** Write a prompt in the "AI Image Prompt" box and click the **purple Render button**. Once you're happy with the result, click the **green Add button** to add it to your scene.

The app automatically sets the correct path. The file will be copied into your project's `images/` or `sounds/` folder when you click **"Save Project"**.

### 5. Customize the Look & Feel
Click the **Style Editor icon** (next to the Menu button). Use the controls to change your game's layout, fonts, colors, and even add background music. Your style settings are saved with your project.

### 6. Save & Export
*   **Save Project:** Click the main **"Save Project"** button in the Menu. This saves all your work to the `story.json` file inside your project folder. **Save frequently!**
*   **Export Standalone Game:** When your game is complete, click **"Menu**" -> "**Export Standalone Game**". This packages your story, all required assets, and your custom theme into a single `.zip` file that you can share or upload anywhere. This is the final, playable product.

***

## The `story.json` File Format

The entire state of a Kinexus project is stored in a single JSON file named `story.json`. This file contains all story text, choices, variables, and styling information.

The top-level structure is a single JSON object with two keys: `meta` and `scenes`.
```json
{
  "meta": { ... },
  "scenes": { ... }
}
```

---

### The `meta` Object
This object contains global information and settings for the project.

| Key | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `title` | String | Yes | The title of your story. This appears in the player's UI. |
| `startSceneId` | String | Yes | The ID of the scene where the story begins. Must match a valid key in the `scenes` object. |
| `creatorName` | String | No | The name of the author, displayed in the "About" section. Defaults to an empty string. |
| `aboutText` | String | No | A description of the project, displayed in the "About" section. Defaults to an empty string. |
| `variables` | Array | Yes | An array of strings, where each string is the unique name of a boolean variable used in the game. |
| `layout` | String | Yes | Defines the player's visual layout. Must be one of `layout-image-as-bg`, `layout-top-down`, or `layout-side-by-side`. |
| `styles` | Object | Yes | An object containing key-value pairs for CSS variables that control the player's appearance (fonts, colors, etc.). |

#### Example `meta` Object:
```json
"meta": {
  "title": "The Last Broadcast",
  "startSceneId": "start",
  "creatorName": "Jane Doe",
  "aboutText": "A short interactive fiction story about a mysterious signal.",
  "variables": [
    "power_restored",
    "has_keycard"
  ],
  "layout": "layout-top-down",
  "styles": {
    "--bg-color": "#1a1a1a",
    "--text-color": "#e0e0e0",
    "--btn-color": "rgba(80, 80, 95, 1)",
    "--font-family": "sans-serif",
    "--music-path": "sounds/ambient_theme.mp3"
  }
}
```

---

### The `scenes` Object
This object acts as a dictionary containing all the individual scenes of the story. The key for each entry is the unique Scene ID, and the value is the corresponding scene object.

#### Structure of a Scene Object
Each scene object has the following structure:

| Key | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `id` | String | Yes | The unique ID of the scene. Must match its key in the parent `scenes` object. |
| `text` | String | Yes | The main story text for this scene. Can contain markdown and can be an empty string. |
| `image` | String | No | The relative path to an image file for the scene (e.g., `images/control_room.jpg`). |
| `imagePrompt`| String | No | The text prompt used to generate an AI image for this scene. |
| `ambienceSound`| String | No | The relative path to a sound file for the scene (e.g., `sounds/static.mp3`). |
| `ambienceLoop`| Boolean | No | If `true` (the default), the `ambienceSound` will loop. If `false`, it will play once. |
| `choices` | Array | Yes | An array of choice objects. An empty array `[]` signifies a dead-end scene. |
| `lastModified`| Number | No | A timestamp (milliseconds since epoch) indicating when the scene was last saved. |

#### Structure of a Choice Object
A choice object defines the logic for a single player interaction, governed by an optional `condition` and a required `action`.

| Key | Type | Description |
| :--- | :--- | :--- |
| `condition`| Object/null | If not `null`, the choice is only shown if the condition is met. |
| `action` | Object | Defines what happens when the choice is triggered. |

**The `condition` Object:**
| Key | Type | Description |
| :--- | :--- | :--- |
| `variable`| String | The state to check. It can be a custom variable (e.g., `"var_power_restored"`) or a scene visit check (e.g., `"visited_scene_basement"`). |
| `value` | Boolean | The required state for the condition to be met (`true` or `false`). |

**The `action` Object:**
| Key | Type | Description |
| :--- | :--- | :--- |
| `text` | String | The text displayed on the choice button. If this is an empty string, the action is silent and triggers automatically when the scene loads. |
| `target` | String/null | The `id` of the scene that this choice leads to. `null` if the action only modifies a variable. |
| `set_variable`| String/null | The name of a variable to modify (e.g., `"has_keycard"`). `null` if the action only changes scene. |
| `set_value`| Boolean | The value to set the `set_variable` to (`true` or `false`). |

---

### Full `story.json` Example
This example demonstrates a small, complete story structure with multiple features.

```json
{
  "meta": {
    "title": "The Last Broadcast",
    "startSceneId": "start",
    "creatorName": "Jane Doe",
    "aboutText": "A short interactive fiction story about a mysterious signal.",
    "variables": [
      "power_restored",
      "has_keycard"
    ],
    "layout": "layout-top-down",
    "styles": {
      "--bg-color": "#1a1a1a",
      "--text-color": "#e0e0e0",
      "--btn-color": "rgba(80, 80, 95, 1)",
      "--font-family": "sans-serif",
      "--music-path": "sounds/ambient_theme.mp3"
    }
  },
  "scenes": {
    "start": {
      "id": "start",
      "text": "You awaken in a dimly lit radio control room. A single monitor glows with the words: **EMERGENCY POWER ONLY**. The main console is dark.\n\nA strange, rhythmic static hums from the speakers.",
      "image": "images/control_room_dark.jpg",
      "imagePrompt": "A dark radio control room, computer monitors are off except one, cinematic lighting, tense mood",
      "ambienceSound": "sounds/static_hum.mp3",
      "ambienceLoop": true,
      "choices": [
        {
          "condition": null,
          "action": {
            "text": "Investigate the main console.",
            "target": "console",
            "set_variable": null,
            "set_value": false
          }
        },
        {
          "condition": null,
          "action": {
            "text": "Look for a way out.",
            "target": "door",
            "set_variable": null,
            "set_value": false
          }
        }
      ],
      "lastModified": 1725528000000
    },
    "console": {
      "id": "console",
      "text": "The console is cold and lifeless. A placard reads \"Auxiliary Power Breaker located in the basement.\" You notice a `keycard` lying next to the keyboard.",
      "choices": [
        {
          "condition": null,
          "action": {
            "text": "Take the keycard and go to the door.",
            "target": "door",
            "set_variable": "has_keycard",
            "set_value": true
          }
        }
      ],
      "lastModified": 1725528100000
    },
    "door": {
      "id": "door",
      "text": "You stand before a heavy metal door with an electronic lock.",
      "choices": [
        {
          "condition": {
            "variable": "var_has_keycard",
            "value": true
          },
          "action": {
            "text": "Use the keycard.",
            "target": "hallway",
            "set_variable": null,
            "set_value": false
          }
        },
        {
          "condition": {
            "variable": "var_has_keycard",
            "value": false
          },
          "action": {
            "text": "Try to force the door.",
            "target": "door_locked",
            "set_variable": null,
            "set_value": false
          }
        }
      ],
      "lastModified": 1725528200000
    },
    "door_locked": {
      "id": "door_locked",
      "text": "It's locked tight. You'll need to find another way.",
      "choices": [
        {
          "condition": null,
          "action": {
            "text": "Go back to the console.",
            "target": "console",
            "set_variable": null,
            "set_value": false
          }
        }
      ],
      "lastModified": 1725528300000
    },
    "hallway": {
      "id": "hallway",
      "text": "You've entered a long, dark hallway. You hear something shuffling in the distance.",
      "choices": [],
      "lastModified": 1725528400000
    }
  }
}
```

---

## Exporting as a Desktop Application (.exe, .app)

For a simple and powerful way to convert your Kinexus web export into a professional desktop application, we recommend using the **Build Standalone Application From HTML** tool.

This tool automates the entire process and provides several key advantages:
*   **Cross-Platform:** Build for Windows (.exe), macOS (.app), and Linux from a single tool.
*   **Easy to Use:** A simple graphical interface walks you through the process.
*   **Custom Icons:** Properly embeds your custom game icon into the final application.
*   **No Security Warnings:** Avoids the common issues with file blocking and security warnings.

### How to Use the Build Tool

1.  **Export Your Game from Kinexus:** Go to **Menu** -> **Export Standalone Game** to download the project `.zip` file. Unzip this file to a folder on your computer.

2.  **Download the Build Tool:** Go to the [Build Standalone Application From HTML repository](https://github.com/tin2tin/Build_Standalone_Application_From_HTML) and download the latest version for your operating system from the **Releases** page.

3.  **Prepare Your Icon:** Create a custom icon for your game (`.ico` for Windows, `.png`/`.icns` for macOS).

4.  **Run the Build Tool:** Launch the application and provide it with:
    *   The `index.html` file you exported from Kinexus.
    *   Your custom icon file.
    *   The name for your application.

5.  **Build and Distribute:** Click **'Build'**. The tool will package your game into a professional, standalone desktop application, ready to be zipped and distributed on platforms like [itch.io](https://itch.io/).

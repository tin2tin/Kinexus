# Kinexus (Interactive Narrative Editor)

**Kinexus** is a powerful zero-code tool for creating, styling, and exporting choice-based narrative games, interactive fiction, and interactive graphic novels. It runs entirely in your web browser, providing a complete workflow from writing your story to packaging a distributable ZIP file for platforms like [itch.io](https://itch.io/).

<img width="1905" height="959" alt="image" src="https://github.com/user-attachments/assets/8a7c3d51-4abd-4d48-8a15-cb728ec17401" />

## Try It

<div align="left">
  <a href="https://tin2tin.github.io/CYOA_Studio/">Open Kinexus</a><br><br>
</div>

<div align="left">
  <a href="https://tintwotin.itch.io/cyoa-test?secret=G3dumLNBVgg2migNyde3jOYm8">Try the example game</a><br><br>
</div>

An example project. Unzip and open with Kinexus: [Example_The_Last_Broadcast](https://github.com/tin2tin/CYOA_Studio/raw/refs/heads/main/example_the_last_broadcast.zip)

## Features

*   **Visual Story Creation:**
    *   A rich text editor for writing your narrative.
    *   Easily add, edit, and link choices between scenes.
    *   **Integrated Generative AI Tools:**
        *   **Image Generation:** Create and add unique artwork for your scenes directly within the editor.
        *   **Text Processing:** Use AI to rewrite or expand upon your story text.

*   **Interactive Story Map:**
    *   A collapsible tree view provides a clear visualization of your story's branches.
    *   Status icons instantly show the start scene, dead ends, orphan scenes, and which scenes have images or audio.
    *   Safely rename scenes with automatic link updating across all choices.
    *   Search and filter your scenes to quickly find what you need.

*   **Live Player & Preview:**
    *   Instantly playtest your game from the start or the current scene using the built-in player.
    *   Launch a full, clean preview of your project in a new browser tab at any time.
    *   **Modern Player UI:** The exported game features a clean, overlay-based UI with quick access to menu, sound toggle, and exit functions, ensuring an immersive experience.

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
    *   Export your complete, playable project as a self-contained `.zip` file. This bundle includes the game, your custom theme, and all required assets, ready to be shared or hosted.
    *   The exported game is optimized for both desktop and mobile browsers.
    *   Export specific data, such as all AI image prompts, to a structured `.json` file for analysis or external use.

*   **Single-File, Zero Installation:**
    *   The entire studio is a single `.html` file. It runs directly in your browser with no installation, servers, or dependencies required.

*   **Local-First Project Management:**
    *   Works directly with folders on your computer via the File System Access API. Your project, including the story file and all assets, is saved locally, not in the cloud. The app tracks unsaved changes to prevent data loss.

## Screenshots

Style Template Editor

<img width="1909" height="958" alt="image" src="https://github.com/user-attachments/assets/4b6d1bee-a579-4ad4-91f5-fafbd41d960b" />

Play Current

<img width="1919" height="956" alt="image" src="https://github.com/user-attachments/assets/3fea42fc-b729-43d8-aa4f-f832d7a90d5b" />

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

<img width="641" height="400" alt="image" src="https://github.com/user-attachments/assets/5ec1328d-0501-4a6e-b8bb-751877a6a529" />

Project Text Editor

<img width="644" height="485" alt="image" src="https://github.com/user-attachments/assets/fd572ff7-0faf-44ab-905a-c15230054ec5" />


## How to Get Started

Creating your first game is a straightforward process. The app handles all the file and folder setup for you.

### 1. Create or Open a Project

First, open the `index.html` file in your browser. From the **Menu**, you have two options:

*   **A. New Project:**
    1.  Click **"New Project"**.
    2.  Enter a name for your game (e.g., "Space Adventure").
    3.  Choose a location on your computer to save it.
    4.  The app will automatically create a complete project folder for you, including sub-folders for `images` and `sounds`, and the main `story.json` file.

*   **B. Open Existing Project:**
    1.  Click **"Open Project"**.
    2.  Navigate to and select a project folder you previously created with the app.

### 2. Create Your Story

*   **Create Scenes:** Use the **round blue '+' button** in the "Story Map" header to create new scenes. Give them short, unique IDs (e.g., `start`, `cockpit`, `alien_encounter`).
*   **Navigate:** Click any scene in the Story Map to load it into the editor. Right-click a scene for more options, like **"Set as Start Scene"**. Use the `[+]` and `[-]` toggles to collapse and expand branches.
*   **Edit Content:** Write your narrative in the "Story Text" area.
*   **Add Choices:** Click the **round blue '+' button** below the choices list. Write the text the player will see and select the target scene from the dropdown menu.

### 3. Add Media (Image & Audio)

You have multiple ways to add images and audio:

1.  **From Your Computer (File Picker):**
    *   Click the **yellow folder icon** next to the "Image" or "Audio" field.
    *   Select any image or audio file from your computer.

2.  **From Your Computer (Drag & Drop):**
    *   Drag an image or audio file from your file explorer directly onto the corresponding text input field (e.g., drag `my_image.png` onto the "Image Path" field). The input will highlight to show it's a valid target.

3.  **Using Generative AI (for Images):**
    *   Write a descriptive prompt in the "AI Image Prompt" text box.
    *   Click the **purple Render button** (with the stars icon) to create an image.
    *   Once you're happy with the result, click the **green Add button** (with the plus icon) to add it to your scene.

For all methods, the app automatically sets the correct path. The file will be copied into your project's `images/` or `sounds/` folder the next time you click **"Save Project"**.

### 4. Customize the Look & Feel

1.  Click **"Menu"** and select **"Style Template Editor"**.
2.  Use the controls to change your game's layout, fonts, colors, and even add background music.
3.  You can see your changes by using the **Preview** or **Play** buttons. Your style settings are saved with your project.

### 5. Save & Export

It's crucial to understand the difference between saving and exporting:

*   **Save Project:** Click the main **"Save Project"** button in the Menu. This saves all your work (story, choices, asset paths, styles) directly to the `story.json` file inside your project folder. **Save your project frequently!**

*   **Export Standalone Game:** When your game is complete, click **"Menu"** -> **"Export Standalone Game"**. This packages your story, all required assets, and your custom theme into a single `.zip` file that you can share or upload anywhere. This is the final, playable product.

***

## The Story File Format

To programmatically generate stories for this application, you must produce a valid JSON file adhering to the precise schema detailed below. This format is ideal for any kind of interactive fiction, from simple stories to complex narratives with state management.

### Root Object Structure

The root element **MUST** be a single JSON object with two required, top-level keys: `meta` and `scenes`.

```json
{
  "meta": { ... },
  "scenes": { ... }
}
```

### The `meta` Object

The `meta` object contains global metadata and configuration for the entire story.

| Key | Type | Required | Description | Example |
| :--- | :--- | :--- | :--- | :--- |
| `title` | String | Yes | The title of your story. | `"The Last Broadcast"` |
| `creatorName` | String | No | The name of the author. | `"A. N. Author"` |
| `aboutText` | String | No | A brief description of the project. | `"A short interactive story of suspense."` |
| `startSceneId` | String | Yes | The ID of the scene where the story begins. | `"radio_room"` |
| `variables` | Object | No | **OPTIONAL.** An object defining the initial state of all story variables (e.g., inventory, character stats). | `{ "has_key": false, "power_on": true }` |
| `layout` | String | Yes | The visual layout. **MUST** be either `"layout-top-down"` or `"layout-side-by-side"`. | `"layout-side-by-side"` |
| `styles` | Object | Yes | An object containing key-value pairs for CSS styling. | `{ "--bg-color": "#1a1a1a", ... }` |

#### The `styles` Object

This object contains CSS custom properties to theme the player. All keys and values **MUST** be strings.

| Key | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| `--bg-color` | String | Background color of the game screen. | `"#1a1a1a"` |
| `--text-color` | String | Main narrative text color. | `"#e0e0e0"` |
| `--btn-color` | String | Background color of choice buttons. | `"#4a78ad"` |
| `--btn-text-color` | String | Text color of choice buttons. | `"#ffffff"` |
| `--btn-hover-color`| String | Background color of choice buttons on hover. | `"#6c757d"` |
| `--btn-border` | String | **OPTIONAL.** Border style for choice buttons. | `"1px solid #ffffff"` |
| `--font-family` | String | Font style. **MUST** be `sans-serif`, `serif`, or `monospace`. | `"monospace"` |
| `--font-size` | String | The base font size, including the `px` unit. | `"18px"` |
| `--padding` | String | Padding inside the game container, including the `px` unit. | `"40px"` |
| `--border-radius` | String | **OPTIONAL.** Corner roundness for buttons and containers. | `"8px"` |
| `--music-path` | String | **OPTIONAL.** Relative path to a global background music file. | `"sounds/bg_music.mp3"` |
| `--screen-bg-image`| String | **OPTIONAL.** Relative path to a background image for the screen. | `"images/static_bg.png"` |
| `--container-bg-image` | String | **OPTIONAL.** Relative path to a background image for the content box. | `"images/paper_texture.jpg"` |

### The `scenes` Object

The `scenes` object is a dictionary where each key is a unique `sceneId` (String) and each value is a corresponding Scene Object.

### Scene Object Structure

Each Scene Object represents a single page or moment in the story.

| Key | Type | Required | Description | Example |
| :--- | :--- | :--- | :--- | :--- |
| `id` | String | Yes | The unique identifier for the scene. | `"radio_room"` |
| `text` | String | Yes | The main narrative text for the scene. | `"The static hisses."` |
| `image` | String | No | **OPTIONAL.** The relative path to the image file. | `"images/radio.jpg"` |
| `imagePrompt` | String | No | **OPTIONAL.** The descriptive prompt used to generate the image. | `"A vintage 1940s radio..."` |
| `ambienceSound` | String | No | **OPTIONAL.** The relative path to a looping background audio file. | `"sounds/radio_static.ogg"` |
| `soundEffect` | String | No | **OPTIONAL.** The relative path to a one-shot sound effect that plays on scene entry. | `"sounds/power_up.wav"` |
| `setVariables` | Object | No | **OPTIONAL.** An object defining variable changes that occur upon entering this scene. | `{ "power_on": true }` |
| `choices` | Array | Yes | An array of Choice Objects. An empty array (`[]`) signifies an ending. | `[ { ... } ]` |

### Choice Object Structure

Each Choice Object defines a single player action and its consequences.

| Key | Type | Required | Description | Example |
| :--- | :--- | :--- | :--- | :--- |
| `text` | String | Yes | The text that appears on the button. | `"Turn the dial."` |
| `target` | String | Yes | The `id` of the scene this choice leads to. | `"faint_signal"` |
| `conditions` | Array | No | **OPTIONAL.** An array of conditions that **MUST** be met for this choice to be visible. | `[{"variable": "power_on", "operator": "equals", "value": true}]` |
| `setVariables` | Object | No | **OPTIONAL.** An object defining variable changes that occur when this choice is selected. | `{ "heard_signal": true }` |

#### Condition Object Structure

The `conditions` array contains one or more Condition Objects. All conditions must be met for the choice to appear.

| Key | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `variable` | String | Yes | The name of the variable to check (must be defined in `meta.variables`). |
| `operator` | String | Yes | The comparison to perform. **MUST** be `"equals"` or `"notEquals"`. |
| `value` | Boolean, String, or Number | Yes | The value to compare against. |

### Complete JSON Example (with new features)

This example demonstrates the use of variables (`knows_code`) to unlock a new story path.

```json
{
  "meta": {
    "title": "The Last Broadcast",
    "creatorName": "A. N. Author",
    "aboutText": "A short interactive story of suspense set in a remote listening post.",
    "startSceneId": "radio_room",
    "variables": {
      "knows_code": false
    },
    "layout": "layout-side-by-side",
    "styles": {
      "--bg-color": "#1a1a1a",
      "--text-color": "#e0e0e0",
      "--btn-color": "#4a78ad",
      "--btn-text-color": "#ffffff",
      "--btn-hover-color": "#6c757d",
      "--btn-border": "1px solid #333",
      "--font-family": "monospace",
      "--font-size": "18px",
      "--padding": "40px",
      "--border-radius": "4px",
      "--music-path": "",
      "--screen-bg-image": "images/static_bg.png",
      "--container-bg-image": ""
    }
  },
  "scenes": {
    "radio_room": {
      "id": "radio_room",
      "text": "The only light in the shack comes from the warm, orange glow of the radio's vacuum tubes.\nOutside, the blizzard howls.\nThe constant hiss of static is your only companion.",
      "image": "images/radio.jpg",
      "imagePrompt": "A vintage 1940s radio console in a dark, rustic wooden shack, glowing tubes casting long shadows, snow visible through a window, dramatic lighting, photorealistic.",
      "ambienceSound": "sounds/radio_static.ogg",
      "choices": [
        {
          "text": "Try to tune the main frequency dial.",
          "target": "faint_signal",
          "setVariables": {}
        },
        {
          "text": "Make a cup of coffee and wait.",
          "target": "ending_nothing"
        }
      ]
    },
    "faint_signal": {
      "id": "faint_signal",
      "text": "You slowly turn the heavy bakelite dial. The static crackles and shifts.\nSuddenly, through the noise, you hear something... a voice? It's faint, distorted by distance and the storm.",
      "image": "",
      "imagePrompt": "",
      "soundEffect": "sounds/faint_voice.mp3",
      "choices": [
        {
          "text": "Fine-tune the signal.",
          "target": "clear_message"
        },
        {
          "text": "Dismiss it as interference and go back.",
          "target": "radio_room"
        }
      ]
    },
    "clear_message": {
      "id": "clear_message",
      "text": "With delicate adjustments, the voice becomes clearer. It's speaking a sequence of numbers, repeating them over and over.\n'...seven... four... one... zero...'\nIt's a code. Then, the signal dies.",
      "image": "images/headphones.jpg",
      "imagePrompt": "Close-up on a pair of vintage 1940s military headphones lying on a wooden desk next to a code book, shallow depth of field, moody lighting.",
      "setVariables": {
        "knows_code": true
      },
      "choices": [
        {
          "text": "Write down the numbers and ponder their meaning.",
          "target": "secret_ending"
        },
        {
          "text": "The numbers mean nothing. The storm is getting worse.",
          "target": "ending_nothing"
        }
      ]
    },
    "ending_nothing": {
      "id": "ending_nothing",
      "text": "You decide against chasing phantoms in the static. The storm rages on, and the night passes in quiet solitude.\nNothing happens. Perhaps that's for the best.",
      "image": "images/snow_window.jpg",
      "imagePrompt": "Looking out a frosted window from a dark cabin into a fierce blizzard at night.",
      "ambienceSound": "sounds/blizzard.mp3",
      "choices": []
    },
    "secret_ending": {
      "id": "secret_ending",
      "text": "The numbers... it's the access code for the emergency bunker hidden beneath the floorboards. You never thought you'd use it.\nAs the storm worsens, you realize the broadcast wasn't a phantom, but a warning.",
      "image": "images/bunker_door.jpg",
      "imagePrompt": "A heavy steel hatch set into a dark wooden floor, a wheel lock in the center.",
      "choices": []
    }
  }
}
```

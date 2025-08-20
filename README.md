# CYOA Studio (Choose Your Own Adventure Editor)

CYOA Studio is a powerful, single-file, zero-installation tool for creating, styling, and exporting choice-based narrative games. It runs entirely in your web browser, providing a complete workflow from writing your story to packaging a distributable ZIP file for platforms like [itch.io](https://itch.io/).

<img width="1919" height="959" alt="image" src="https://github.com/user-attachments/assets/29d32050-1668-4c53-8f1a-7f9ba144128c" />

## Try It

<div align="left">
  <a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/tin2tin/CYOA_Studio_Pro/master/index.html">CLICK HERE!</a><br><br>
</div>

## Features

*   **Visual Story Creation:**
    *   A rich text editor for writing your narrative.
    *   Easily add, edit, and link choices between scenes.
    *   Includes an integrated **Generative AI Image** tool to create and add unique artwork for your scenes directly within the editor.

*   **Interactive Story Map:**
    *   A collapsible tree view provides a clear visualization of your story's branches.
    *   Status icons instantly show the start scene, dead ends, orphan scenes, and which scenes have images or audio.
    *   Safely rename scenes with automatic link updating across all choices.
    *   Search and filter your scenes to quickly find what you need.

*   **Live Player & Preview:**
    *   Instantly playtest your game from the start or the current scene using the built-in player.
    *   Launch a full, clean preview of your project in a new browser tab at any time.

*   **Integrated Asset Management:** Select image and audio files from your computer. The studio automatically copies them into your project folder on save, ensuring all asset paths are correct and ready for export.

*   **Powerful Style Editor:** Customize the visual theme of your game, including layout, colors, fonts, padding, background images, and even global background music. Your custom style is saved with the project.

*   **One-Click Export:**
    *   Export your complete, playable project as a self-contained `.zip` file. This bundle includes the game, your custom theme, and all required assets, ready to be shared or hosted.
    *   Export specific data, such as all AI image prompts, to a structured `.json` file for analysis or external use.

*   **Single-File, Zero Installation:** The entire studio is a single `.html` file. It runs directly in your browser with no installation, servers, or dependencies required.

*   **Local-First Project Management:** Works directly with folders on your computer via the File System Access API. Your project, including the story file and all assets, is saved locally, not in the cloud. The app tracks unsaved changes to prevent data loss.

Of course! Here is the updated "How to Get Started" guide, rewritten to accurately reflect the app's modern, streamlined workflow.

***

## Screenshots

<img width="1919" height="957" alt="image" src="https://github.com/user-attachments/assets/5e5bf8e6-bc71-4394-9cdb-ab7e2129b19c" />
<img width="1919" height="960" alt="image" src="https://github.com/user-attachments/assets/981509d8-acf2-4e0b-9c41-eb0676853fb9" />
<img width="1919" height="958" alt="image" src="https://github.com/user-attachments/assets/3b60724b-92e2-49ab-b864-64edc3830c5e" />

***

## How to Get Started

Creating your first game is a straightforward process. The app handles all the file and folder setup for you.

### 1. Create or Open a Project

First, open the `cyoa-studio.html` file in your browser. From the **Menu**, you have two options:

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

You have two ways to add images, and one way to add audio:

1.  **From Your Computer:**
    *   Click the **yellow folder icon** next to the "Image" or "Audio" field.
    *   Select any image or audio file from your computer.
    *   Or you can drag & drop the files to the string widgets. 
    *   The app automatically sets the correct path. The file will be copied into your project's `images/` or `sounds/` folder the next time you click **"Save Project"**.

2.  **Using Generative AI (for Images):**
    *   Write a descriptive prompt in the "Generative AI Image" text box.
    *   Click the **purple Render button** (with the stars icon) to create an image.
    *   Once you're happy with the result, click the **green Add button** (with the plus icon) to add it to your scene.

### 4. Customize the Look & Feel

1.  Click **"Menu"** and select **"Style Template Editor"**.
2.  Use the controls to change your game's layout, fonts, colors, and even add background music.
3.  You can see your changes by using the **Preview** or **Play** buttons. Your style settings are saved with your project.

### 5. Save & Export

It's crucial to understand the difference between saving and exporting:

*   **Save Project:** Click the main **"Save Project"** button in the Menu. This saves all your work (story, choices, asset paths, styles) directly to the `story.json` file inside your project folder. **Save your project frequently!**

*   **Export Standalone Game:** When your game is complete, click **"Menu"** -> **"Export Standalone Game"**. This packages your story, all required assets, and your custom theme into a single `.zip` file that you can share or upload anywhere. This is the final, playable product.

  
---


## The Story File Format

To generate stories for this editor, you must produce a valid JSON file adhering to the following structure.

### Root Object Structure

The root element **MUST** be a single JSON object with two top-level keys: `meta` and `scenes`.

```json
{
  "meta": { ... },
  "scenes": { ... }
}
```

### The `meta` Object

The `meta` object contains global information about the story and its presentation.

| Key            | Type   | Description                                                                                                   | Example                                 |
| -------------- | ------ | ------------------------------------------------------------------------------------------------------------- | --------------------------------------- |
| `title`        | String | The title of your story. Used for the browser tab and exported project name.                                  | `"The Grey Uniform"`                      |
| `startSceneId` | String | The ID of the scene where the story begins. This ID **MUST** exist as a key in the `scenes` object.             | `"conscription_notice"`                 |
| `layout`       | String | The visual layout of the game screen. **MUST** be either `"layout-top-down"` or `"layout-side-by-side"`.        | `"layout-side-by-side"`                 |
| `styles`       | Object | An object containing key-value pairs for CSS styling. See the `styles` object details below.                  | `{ "--bg-color": "#3d2b1f", ... }`       |

#### The `styles` Object

This object contains key-value pairs that directly map to CSS custom properties.

| Key                 | Type   | Description                                     | Example         |
| ------------------- | ------ | ----------------------------------------------- | --------------- |
| `--bg-color`        | String | Background color of the game. (Hex code)        | `"#3d2b1f"`      |
| `--text-color`      | String | Main text color. (Hex code)                     | `"#f5f5dc"`      |
| `--btn-color`       | String | Background color of choice buttons. (Hex code)  | `"#8a6d3b"`      |
| `--btn-text-color`  | String | Text color of choice buttons. (Hex code)        | `"#ffffff"`      |
| `--btn-hover-color` | String | Background color of buttons on hover. (Hex code)| `"#ab884a"`      |
| `--font-family`     | String | Font style. **MUST** be `sans-serif`, `serif`, or `monospace`. | `"serif"`       |
| `--padding`         | String | Padding inside the game container, in pixels. **MUST** be a string of a number. | `"35"`          |

### The `scenes` Object

The `scenes` object is a dictionary where each key is a unique `sceneId` (String) and each value is a Scene Object.

```json
"scenes": {
  "sceneId_1": { ... Scene Object 1 ... },
  "sceneId_2": { ... Scene Object 2 ... }
}
```

### Scene Object Structure

Each Scene Object describes a single moment or page in the story.

| Key             | Type   | Description                                                                                                   | Example                                                                                             |
| --------------- | ------ | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `id`            | String | The unique identifier for this scene. **MUST** be identical to its key in the `scenes` object.                  | `"conscription_notice"`                                                                             |
| `text`          | String | The main narrative text for the scene. Can include newline characters (`\n`) for formatting.                      | `"The letter arrives, cold and official.\nYou have been conscripted."`                               |
| `image`         | String | *Optional.* The relative path to the image file for this scene. Omit or leave empty (`""`) for no image.          | `"images/letter.jpg"`                                                                               |
| `imagePrompt`   | String | *Optional.* The descriptive prompt used to generate the image with an AI.                                       | `"A WW1 German conscription letter on a rustic wooden table, photorealistic, somber lighting."`       |
| `ambienceSound` | String | *Optional.* The relative path to the looping background sound file. Omit or leave empty for silence.            | `"sounds/paper_rustle.mp3"`                                                                         |
| `choices`       | Array  | An array of Choice Objects. If empty, the story ends at this scene.                                           | `[ { "text": "...", "target": "..." } ]`                                                            |

### Choice Object Structure

Each Choice Object, located inside a scene's `choices` array, defines a player option.

| Key      | Type   | Description                                                                             | Example                   |
| -------- | ------ | --------------------------------------------------------------------------------------- | ------------------------- |
| `text`   | String | The text that appears on the button for the player to click.                            | `"Accept your fate."`       |
| `target` | String | The `id` of the scene this choice leads to. This ID **MUST** exist as a key in the `scenes` object. | `"train_station"` |

### Complete JSON Example

```json
{
  "meta": {
    "title": "The Grey Uniform",
    "startSceneId": "conscription_notice",
    "layout": "layout-side-by-side",
    "styles": {
      "--bg-color": "#3d2b1f",
      "--text-color": "#f5f5dc",
      "--btn-color": "#8a6d3b",
      "--btn-text-color": "#ffffff",
      "--btn-hover-color": "#ab884a",
      "--font-family": "serif",
      "--padding": "35"
    }
  },
  "scenes": {
    "conscription_notice": {
      "id": "conscription_notice",
      "text": "The letter arrives on a Tuesday, cold and official. The Imperial German eagle stares from the masthead, its gaze impersonal. You have been conscripted.\n\nYour mother weeps quietly in the kitchen. Your father claps you on the shoulder, his face a mask of grim pride. There is no choice.",
      "image": "images/letter.jpg",
      "imagePrompt": "A WW1 German conscription letter on a rustic wooden table, photorealistic, somber lighting, ink pen and a half-empty glass nearby.",
      "ambienceSound": "sounds/paper_rustle.mp3",
      "choices": [
        {
          "text": "Accept your fate and pack your bag.",
          "target": "train_station"
        }
      ]
    },
    "train_station": {
      "id": "train_station",
      "text": "The platform is a chaotic sea of grey uniforms, steam, and tearful goodbyes. The air is thick with the smell of coal smoke and anxiety. A sergeant barks orders, his voice raw.\n\nThe train, a monstrous iron beast, waits impatiently.",
      "image": "images/steam_train.jpg",
      "imagePrompt": "Thousands of German soldiers in Pickelhaube helmets boarding a steam train, WW1, platform is crowded with families, cinematic, sepia tone, emotional.",
      "ambienceSound": "sounds/train_station.mp3",
      "choices": [
        {
          "text": "Find a quiet corner in a railcar.",
          "target": "western_front"
        },
        {
          "text": "Try to start a conversation with another recruit.",
          "target": "western_front"
        }
      ]
    }
  }
}
```

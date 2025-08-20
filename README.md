# CYOA Studio

CYOA Studio is a powerful, single-file, zero-installation tool for creating, styling, and exporting choice-based narrative games. It runs entirely in your web browser, providing a complete workflow from writing your story to packaging a distributable ZIP file for platforms like [itch.io](https://itch.io/).

<img width="1919" height="957" alt="image" src="https://github.com/user-attachments/assets/279f6a85-7f70-49c7-80ff-d4564b802b56" />
<img width="1919" height="959" alt="image" src="https://github.com/user-attachments/assets/25855fd8-cb0e-475e-a2d3-8694923da5c3" />

## Try It

<div align="left">
  <a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/tin2tin/CYOA_Studio_Pro/master/index.html">OPEN HERE!</a><br><br>
</div>

## Features

*   **Single-File Application:** The entire editor is one `.html` file. No installation, no servers, no dependencies.
*   **Visual Editor & Live Preview:** Write your story, add choices, and instantly preview your game in the built-in player.
*   **Autosaving & Session Restore:** Never lose your work. Your session is automatically saved in the browser, and you'll be prompted to restore it if you accidentally close the tab.
*   **Interactive Story Map:**
    *   A collapsible tree view to visualize your story's branches.
    *   Safely rename scenes with automatic link updating.
    *   Right-click any scene to set it as the starting point.
*   **Integrated Asset Management:** Set a project root folder and pick your images and sounds from a list, preventing typos and broken paths.
*   **Visual Style Editor:** A powerful modal for customizing the colors, fonts, and layout of your game's interface. Changes are saved with your project and reflected in the export.
*   **Data & Project Export:**
    *   Export specific data, like all AI image prompts, to a structured `.json` file.
    *   Export the complete, playable project as a `.zip` file, containing the game, your custom theme, and all required assets.

## How to Use the Editor

Follow these steps to create your first game.

### 1. Setup Your Project Folder

Before you start, create a main folder for your game on your computer. Inside this folder, create two sub-folders: `images` and `sounds`.

```
my-amazing-game/
├── images/
│   ├── scene1.jpg
│   └── scene2.png
└── sounds/
    ├── ambient_wind.mp3
    └── title_music.ogg
```

### 2. Set the Project Root

1.  Open the `cyoa-studio.html` file in your browser.
2.  Click the **"Set Project Root"** button.
3.  In the file dialog, select the main folder you created (e.g., `my-amazing-game`).
4.  The editor will scan the folder and its sub-folders for compatible asset files.

### 3. Create Your Story

*   **Create Scenes:** Use the **`+`** button in the "Story Map" to create new scenes. Give them short, unique IDs (e.g., `start`, `trench_battle`).
*   **Navigate:** Click a scene in the Story Map to load it into the editor. Right-click for more options like **"Set as Start Scene"**. Use the `[+]` and `[-]` toggles to collapse and expand branches.
*   **Edit Content:** Fill in the fields in the Scene Editor. Add descriptive text, AI image prompts, and link to assets.
*   **Add Choices:** Click the **"+ Add Choice"** button. Write the text the player will see and select the target scene from the dropdown menu.

### 4. Add Assets

Once the project root is set, you can easily add images and sounds:

1.  Click the **"Select..."** button next to the "Image Filename" or "Ambience Sound" field.
2.  A modal will appear listing all the compatible files found in your project folder.
3.  Click on a file to automatically insert its correct path (e.g., `images/scene1.jpg`).

### 5. Customize the Look

1.  Click the **"Style Editor"** button.
2.  Use the color pickers, dropdowns, and number fields to change the appearance of your game.
3.  You can preview your changes by clicking one of the **"Play"** buttons. Your style settings are saved with your project file.

### 6. Save and Export

*   **Save Project File:** Click the main **"Save"** button. This downloads a `.json` file containing your entire story structure and style settings. **This is your source file.** Save it frequently.
*   **Export Playable Game:** When you are finished, click **"Export Playable Project"**. This will package your story, assets, and theme into a single `.zip` file that you can share or upload.

---

## The Story File Format (For LLM Instruction)

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

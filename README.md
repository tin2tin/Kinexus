# Kinexus (Interactive Narrative Editor)

**Kinexus** is a powerful zero-code tool for creating, styling, and exporting choice-based narrative games, interactive fiction, and interactive graphic novels. It runs entirely in your web browser, providing a complete workflow from writing your story to packaging a distributable ZIP file for platforms like [itch.io](https://itch.io/).

<img width="1905" height="959" alt="image" src="https://github.com/user-attachments/assets/8a7c3d51-4abd-4d48-8a15-cb728ec17401" />

## Try It

<div align="left">
  <a href="https://tin2tin.github.io/Kinexus/">Open Kinexus</a><br><br>
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

The entire state of a Kinexus project is stored in a single JSON file named `story.json`. This file contains all story text, choices, scene connections, and styling information. The structure is composed of two primary top-level objects: `meta` and `scenes`.

#### **Top-Level Structure**

```json
{
  "meta": { ... },
  "scenes": { ... }
}
```

---

#### **The `meta` Object**

This object contains global information and settings for the project.

| Key | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `title` | String | Yes | The title of your story. This appears in the player's "About" section and as the title of the exported HTML file. |
| `startSceneId` | String | Yes | The ID of the scene where the story begins. This ID must correspond to a valid key in the `scenes` object. |
| `creatorName` | String | No | The name of the author, displayed in the "About" section. Defaults to an empty string. |
| `aboutText` | String | No | A description of the project, displayed in the "About" section. Defaults to an empty string. |
| `layout` | String | Yes | Defines the player's visual layout. Must be one of `layout-image-as-bg`, `layout-top-down`, or `layout-side-by-side`. |
| `styles` | Object | Yes | An object containing key-value pairs for CSS variables that control the player's appearance (fonts, colors, etc.). |

**Example `meta` Object:**
```json
"meta": {
  "title": "The Cavern of Whispers",
  "startSceneId": "entry",
  "creatorName": "Jane Doe",
  "aboutText": "A short interactive fiction story.",
  "layout": "layout-image-as-bg",
  "styles": {
    "--bg-color": "#1a1a1a",
    "--text-color": "#e0e0e0",
    "--btn-color": "rgba(80, 80, 95, 1)",
    "--font-family": "serif",
    "--music-path": "sounds/dungeon_theme.mp3"
  }
}
```

---

#### **The `scenes` Object**

This object acts as a dictionary containing all the individual scenes of the story. The key for each entry is the unique Scene ID.

| Key | Type | Description |
| :--- | :--- | :--- |
| `[sceneId]` | String | The unique identifier for a scene (e.g., "entry", "hallway", "room_12"). This key must match the `id` property within the scene object itself. |
| `[sceneObject]` | Object | An object containing all the data for that specific scene. |

**Structure of a Scene Object:**

Each scene object within the `scenes` dictionary has the following structure:

| Key | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `id` | String | Yes | The unique ID of the scene. Must match the key in the parent `scenes` object. |
| `text` | String | Yes | The main story text displayed to the player for this scene. Can be an empty string. |
| `image` | String | No | The relative path to an image file for the scene (e.g., `images/cavern.jpg`). |
| `imagePrompt` | String | No | The text prompt used to generate an AI image for this scene. |
| `ambienceSound` | String | No | The relative path to a sound file for the scene (e.g., `sounds/dripping.mp3`). |
| `ambienceLoop` | Boolean | No | If `true` (the default), the `ambienceSound` will loop. If `false`, it will play once. |
| `choices` | Array | Yes | An array of choice objects. An empty array `[]` signifies a "dead end" scene. |
| `lastModified` | Number | No | A timestamp (milliseconds since epoch) indicating when the scene was last saved. Used for sorting. |

**Structure of a Choice Object (within the `choices` array):**

| Key | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `text` | String | Yes | The text displayed on the choice button for the player. |
| `target` | String | Yes | The ID of the scene that this choice leads to. This ID must correspond to a valid key in the `scenes` object. |

**Example `scenes` Object:**
```json
"scenes": {
  "entry": {
    "id": "entry",
    "text": "You stand at the mouth of a dark cavern. A cold wind blows out from within, carrying faint whispers.",
    "image": "images/cave_entrance.jpg",
    "ambienceSound": "sounds/wind.mp3",
    "ambienceLoop": true,
    "choices": [
      {
        "text": "Enter the cavern.",
        "target": "dark_passage"
      },
      {
        "text": "Turn back.",
        "target": "forest"
      }
    ],
    "lastModified": 1724911380000
  },
  "dark_passage": {
    "id": "dark_passage",
    "text": "The passage is narrow and dark. You can barely see your hand in front of your face.",
    "choices": [],
    "lastModified": 1724911440000
  }
}
```

### 2. Instructions for a Successful Import

To ensure your `story.json` file is imported correctly, it must adhere to the following demands and structure:

1.  **Valid JSON Format**: The file must be a syntactically correct JSON file. You can validate your file using an online JSON validator. Any syntax error (like a missing comma or quote) will cause the import to fail immediately.

2.  **Top-Level Objects**: The root of the JSON object must contain the `meta` and `scenes` keys. The application is designed to be robust and may create them if they are missing, but for a predictable import, they should be present.

3.  **Required `meta` Fields**:
    *   The `meta` object **must** contain a `startSceneId` property.
    *   The value of `startSceneId` **must** be a string that matches one of the scene IDs (keys) in the `scenes` object. If it doesn't, the application will attempt to correct it by selecting the first available scene, but this may not be your intended starting point.

4.  **Scene and Choice Integrity**:
    *   Every scene object in the `scenes` dictionary **must** have a unique key (its ID).
    *   Inside each scene object, the `id` property should be present and match its key.
    *   The `text` and `choices` properties must be present in every scene object. `text` must be a string, and `choices` must be an array.
    *   For every choice object in a `choices` array, the `text` (string) and `target` (string) properties are required.
    *   The `target` of every choice should point to a valid scene ID that exists in the `scenes` object. A non-existent target will be flagged as a "Broken Link" in the tree view and will result in an error in the player.

5.  **Order of Items**:
    *   Inside the main JSON object, the order of `meta` and `scenes` does not matter.
    *   Inside the `scenes` object, the order of the individual scene objects does not matter, as they are accessed by their unique ID keys.
    *   Inside each scene object, the order of properties (`id`, `text`, `choices`, etc.) does not matter.
    *   **Crucially, the order of choice objects within a `choices` array is preserved.** They will be displayed to the player in the same order they appear in the array.


***

## Export to EXE

### Explanation for the Windows Unzipping and Icon Issues

These issues cannot be solved with code, but here is the essential information you need.

#### 1. How to Fix the "Windows blocks unzipping" Warning

When you distribute your game, your users may see a warning when they try to unzip the file. Instruct them to do the following:

1.  Find the downloaded `.zip` file on their computer.
2.  **Right-click** on the file and choose **Properties**.
3.  At the bottom of the **General** tab, there will be a security message: *"This file came from another computer and might be blocked to help protect this computer."*
4.  Check the **Unblock** checkbox next to this message.
5.  Click **Apply**, and then **OK**.

After doing this, they will be able to unzip the file and run the game without any issues.

#### 2. How to Manually Add the Icon to the EXE

Because the browser cannot modify the EXE file, you must do this one final step manually after exporting.

1.  **Prepare your Icon:** Create a proper Windows icon file. It must have the **`.ico`** extension. You can use free online tools to convert a PNG or JPG into a `.ico` file.
2.  **Download a Resource Editor:** A free, popular tool for this is **Resource Hacker**. You can download it from its official site.
3.  **Export and Unzip:** Export your game from your application and unzip the resulting folder.
4.  **Change the Icon:**
    *   Open Resource Hacker.
    *   Go to `File > Open` and select the `.exe` file for your game.
    *   In the left-hand pane, right-click on the **Icon** folder and choose **Replace Icon...**.
    *   In the new window, click **Open file with new icon...** and select your `.ico` file.
    *   Select the icon from the list (usually there's only one) and click **Replace**.
    *   Go to `File > Save` to save the changes to your `.exe` file.

Your `.exe` will now have a proper custom icon when viewed in Windows Explorer.

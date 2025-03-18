# Copy Scene Path Menu

A Unity Editor utility that allows you to easily copy the hierarchical path of GameObjects in your scene.

## Features

- Copy the full scene path of any selected GameObject
- Support for copying multiple GameObjects at once
- Regex filtering to remove or keep specific parts of paths
- Preview window to review and edit paths before copying
- Configuration window to customize behavior

## Installation

1. Place the `CopyScenePathMenu.cs` file in your project's `Editor` folder
2. Load the Script somehow may auto load or may have to restart

## Usage

### Basic Usage

1. Select any GameObject in your scene hierarchy
2. Right-click and select "Copy Scene Path" from the context menu
3. The path is copied to your clipboard in the format: `Parent/Child/GrandChild`

### Multiple Selection

1. Select multiple GameObjects in your scene hierarchy
2. Right-click and select "Copy Scene Path"
3. A preview window will appear showing all paths
4. Click "Copy All to Clipboard" to copy all paths separated by newlines

### Path Preview

When copying paths, a preview window allows you to:
- View the paths before copying
- Enable "Edit Mode" to manually modify paths
- Reset individual paths to their original form
- Copy all paths or only the original paths

### Regex Filtering

You can filter paths using regular expressions:

1. Go to "Tools > Scene Path Copy > Configure"
2. Enable "Regex Filtering"
3. Enter a regex pattern
4. Choose whether to remove or keep matched parts

#### Example Regex Pattern

- `Effect(\s*\(\d+\))?` - Matches "Effect" and "Effect (1)", "Effect (42)", etc.

## Configuration Options

Access the configuration window via "Tools > Scene Path Copy > Configure":

- **Enable Regex Filtering**: Toggle regex filtering on/off
- **Regex Pattern**: The pattern to match against path segments
- **Remove Matched Parts**: When enabled, removes matched segments; when disabled, keeps only matched segments
- **Show Preview Before Copy**: When enabled, shows the preview window before copying

## Tips

- Use regex filtering to clean up paths with numbered duplicates (e.g., "Effect (1)")
- The preview window allows for manual editing if you need to make specific changes
- All settings are saved between Unity sessions

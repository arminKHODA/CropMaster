# CropMaster

CropMaster is a Windows Forms application built with C# for managing and analyzing image data. It provides functionalities for cropping images, detecting faces, and generating thumbnails.

## Features

- Browse and select directories containing images.
- Display thumbnails of images with optional crop regions.
- Crop images manually or automatically using face detection.
- Save crop coordinates and update thumbnails accordingly.
- Rotate, flip, and crop images with easy-to-use buttons.
- Toggle UI visibility for a streamlined interface.

## Requirements

- .NET Framework 4.7.2 or higher
- Guna.UI2.WinForms for UI controls
- Emgu.CV for computer vision functionalities

## Installation

1. Clone the repository or download the source code.
2. Open the solution in Visual Studio.
3. Restore NuGet packages to install required dependencies.
4. Build the solution to compile the application.

## Usage

### Running the Application

1. Launch the application by running the executable or starting it from Visual Studio.
2. Use the "Browse" button to select a root directory containing images.
3. Click "Show Crop" to display thumbnails of the images in the selected directory.
4. Click on a thumbnail to open the image in a new form for cropping and other manipulations.

### Main Functionalities

1. **Browsing Directories**:
    - The "Browse" button allows you to select a root directory. The selected path is displayed in the text box next to the button.

2. **Displaying Thumbnails**:
    - Click the "Show Crop" button to load and display thumbnails of the images in the selected directory. Subfolders will be displayed as buttons for further navigation.

3. **Image Manipulations**:
    - Click on a thumbnail to open the image in a new form where you can:
        - Rotate the image left or right.
        - Flip the image horizontally or vertically.
        - Crop the image manually by dragging to select a crop area.
        - Save the crop area coordinates to a text file.

4. **Face Detection**:
    - Click the "Auto Detection" button to automatically detect faces in the images and save the coordinates. Thumbnails will be updated to reflect detected faces.

5. **UI Toggle**:
    - The "UI" button toggles the visibility of the main UI elements for a streamlined interface.

6. **Show Undetected**:
    - The "Show Undetected" button toggles between displaying all thumbnails and only those that have not been detected with faces.

### Example Code Snippets

#### Main Entry Point (Program.cs)

```csharp
using System;
using System.Windows.Forms;

namespace CropMaster
{
    internal static class Program
    {
        [STAThread]
        static void Main()
        {
            Application.EnableVisualStyles();
            Application.SetCompatibleTextRenderingDefault(false);
            Application.Run(new Form1());
        }
    }
}

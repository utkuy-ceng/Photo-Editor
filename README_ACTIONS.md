# Automated Windows Executable Building

This project uses GitHub Actions to automatically build a Windows executable (.exe) file.

## How It Works

Whenever code is pushed to the main branch, GitHub Actions will:

1. Launch a Windows virtual machine in GitHub's cloud
2. Install Python 3.11 and all dependencies
3. Build the executable using PyInstaller
4. Upload the result as downloadable artifacts

## How to Get the Windows Executable

After pushing changes to GitHub:

1. Go to your repository on GitHub
2. Click on the "Actions" tab at the top
3. Click on the most recent workflow run (it will be named after your commit message)
4. Scroll down to the "Artifacts" section
5. Download the "PhotoEditor-Windows-Zip" file

This zip file contains:

- PhotoEditor.exe (the standalone executable)
- Input and output folders
- A README and quick guide

## Running the Workflow Manually

You can also trigger a build manually:

1. Go to your repository on GitHub
2. Click on the "Actions" tab
3. Select "Build Windows Executable" from the left sidebar
4. Click the "Run workflow" button
5. Select the branch you want to build from
6. Click "Run workflow"

## Checking Build Status

The green checkmark (✓) means the build succeeded. A red X means something went wrong.

Click on any workflow run to see detailed logs and debug any issues.

## Notes

- The executable is built for Windows only
- Each build takes about 5-10 minutes to complete
- The standalone .exe file includes all dependencies
- Users don't need to install Python to run it

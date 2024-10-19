# TurnOffMonitor
A simple keyboard/desktop shortcut Powershell script to turn off the monitor(s).

## How to Use
Download the [zip archive](https://github.com/colvdv/TurnOffMonitor/releases/download/v1.0/TurnOffMonitor.zip) from the [latest release](https://github.com/colvdv/TurnOffMonitor/releases) or follow the DIY instructions below.

## DIY Instructions
### Step 1: Create the Desktop Shortcut Script
1. In Windows, right click the desktop and choose New > Shortcut.
2. In the window that appears, put the following code in the box for the location of the item, then click next:
```
C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe -Command "(Add-Type '[DllImport(\"user32.dll\")]public static extern int SendMessage(int hWnd,int hMsg,int wParam,int lParam);' -Name a -Pas)::SendMessage(-1,0x0112,0xF170,2)"
```
3. Now name the shortcut (e.g. *TurnOffMonitor*), then click Finish. At this stage, you will have created a desktop shortcut that turns off the monitor(s).

### Step 2: Add the Keyboard Shortcut
1. Right click on the desktop shortcut you created and open Properties.
2. Click inside the "Shortcut key" textbox (where it says "None" if you haven't already created a keyboard shortcut; if you have already then it will show it).
3. Press your desired key combination (e.g. *Ctrl + Alt + N*), then click Apply. You will now be able to press the key combination you set to turn of the monitor(s).

## Notes
- The shortcut must remain on the desktop in order to work.
- Keyboard shortcut has limitations. Follow *Ctrl + Alt + KEY* format for best results.

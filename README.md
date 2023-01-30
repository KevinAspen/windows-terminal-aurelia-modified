# Aurelia Retro - a Windows Terminal theme

![alt text][logo]

[logo]: https://raw.githubusercontent.com/KevinAspen/windows-terminal-aurelia-modified/master/demo.png "Aurelia theme for Windows Terminal"

## Installation

1. Install Oh my Posh 3;

2. Open your Windows Terminal settings.json

   ```
   %LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json
   ```

3. Copy the profiles and the scheme from [profiles.json](theme/profiles.json) to the settings.json \
   Make sure to change the variable backgroundImage has the correct path of [au-os-M.png](au-os-M.png)

4. Edit your PowerShell profile and add the following line, modifying it to match the location of your [start_message_pwsh.txt](theme/start_message_pwsh.txt) and [purple-man.omp.json](theme/purple-man.omp.json)

   ```
   oh-my-posh init pwsh --config 'C:/Users/PATH/TO/purple-man.omp.json' | Invoke-Expression
   type 'C:/Users/PATH/TO/start_message_pwsh.txt'
   ```
   
5. Modify [clink_start.cmd](theme/clink_start.cmd) to have the correct path to [start_message_clink.txt](theme/start_message_clink.txt)

6. Modify [oh-my-posh.lua](theme/oh-my-posh.lua) to have the correct path to [purple-man.omp.json](theme/purple-man.omp.json)
   
7. Add clink_start.cmd and oh-my-posh.lua to your Clink directory
   ```
   C:\Program Files (x86)\clink
   ```
   
### Bonus Steps - Ascii Banner Clear Command

1. Modify [cleart.bat](theme/clear/cleart.bat) to have the correct path to [clear.txt](theme/clear/clear.txt)

2. Add cleart.bat to PATH
   ```
   C:\> setx path "%PATH%;C:\PATH\TO\clear\"
   ```
3. `cleart` now clears the terminal and prints an ascii banner



## Fonts

The theme is using Cascadia Code.

Information on how to download Cascadia Code can be found here: <https://github.com/microsoft/cascadia-code>

If you like to use another font, just change the fontFace property in profiles.json.
   
To make all the glyphs work as intended, you need to switch to a font that supports Power Line glyphs. 
Caskaydia Cove, a Cascadia Code version patched with the required glyphs, is recommened. You can find it on NerdFonts.com or via direct link here: <https://github.com/ryanoasis/nerd-fonts/releases/download/v2.3.3/CascadiaCode.zip>

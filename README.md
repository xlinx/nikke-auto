# nikke-auto
* All nature action, no need root
* Android device
* Game
  * 🔴 Auto-Hot-Key (not-recommand) 
    * https://www.autohotkey.com/
  * 🟢 Auto-tower (ready4Use)
    - requirement: adb
      * [<img src="./autoTower/next.png" width="50"/>](https://decade.tw/)
  * 🟠 nikke-auto-MCP-ai (updating)
    - requirement: nodejs, adb, lm-studio or ollama which can load MCP protocol 3rd ai chat tool are fine.
    * [<img src="https://lmstudio.ai/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Flmstudio-app-logo.11b4d746.webp&w=32&q=75" height="20"/>](https://lmstudio.ai/) LLM LM-Studio

### install Auto-tower

```shell
# Auto-tower
#when developer mode ok then install android adb tool(for send device tap command)
brew install adb-enhanced
#image tool: imagemagick (for check blue button)
brew install imagemagick
cd autoTower
sh nikke_ADB.sh


```
### install nikke-auto-MCP-ai

```shell

# nikke-MCP-ai
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
nvm install 12
cd nikke-MCP-ai
npm install
node run nikkeMcpServer

#open ur 3rd chat tool: lm-studio (https://lmstudio.ai/)


```

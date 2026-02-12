# Ace-Attorney-Discord-Improved
A Discord bot that turns conversations into Ace Attorney scenes, with extra features and improvements. *A fork of [ace-attorney-discord-bot by LuisMayo](https://github.com/LuisMayo/ace-attorney-discord-bot)*.
## Getting Started
Ace-Attorney-Discord-Improved and the original Ace-Attorney-Discord-Bot use [Objection Engine](https://github.com/LuisMayo/objection_engine) to render scenes. You can find the requirements for Objection Engine [here](https://github.com/LuisMayo/objection_engine/blob/main/README.md#prerequisites).

> [!IMPORTANT]
> Python 3.10 is required. Objection Engine will not run on Python 3.13 or others. I recommend using [uv](https://docs.astral.sh/uv/) to install and manage your virtual environment. For installation instructions for uv, see [here](https://docs.astral.sh/uv/getting-started/installation/).

To install uv on Linux or macOS, execute the following command.
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```
*See the uv docs for Windows instructions.*
Clone and enter the repository.
```bash
git clone --recurse-submodules https://github.com/Jab11n/ace-attorney-discord-improved && cd ace-attorney-discord-improved
```
Create the virtual environment and enter it.
```bash
uv venv --python 3.10
source .venv/bin/activate
```
Install dependencies from the `requirements.txt`.
> [!NOTE]
> The `requirements.txt` and `Pipfile` call for the CPU-only version of torch by default. If you have a discrete graphics card and want to use the GPU for rendering, edit them to require the latest default version of torch.
```bash
uv pip install -r requirements.txt
```
Create a copy of `config.yaml.example`, name it `config.yaml`, enter your Discord bot token, and change settings as needed.
Then, run the bot.
```bash
python3 main.py
```
It may take a while to generate the first video, because the reasoning model has to be downloaded.

## Project
This is a work in progress. I'm working on adapting the original code to use a newer version of Discord.py and Discord features. The original repository hasn't been updated in over 2 years and the official Discord bot has been offline for a while. 

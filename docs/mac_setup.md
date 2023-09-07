# Mac Setup

## Terminal Tools and Dependencies

* Starship
* Warp
* pipx
* virtualenv
* oh-my-zsh

With the following plugins enabled and installed
    
```bash
    plugins=(
      git
      docker
      zsh-autosuggestions
      zsh-syntax-highlighting
      web-search
    )
```

## Warp

Next generation lightning fast Terminal written in Rust

## GUI Applications

* VSCode
* ExpressVPN
* GitKraken [Dark with Menlo font]
* Firefox
* Notion
* Slack
* Figma
* Loom
* Docker
* Telegram
* Sublime Text

## VSCode

Github Dark Theme

![VSCode Github Theme Screenshot](/images/vscode.png)

### Extensions

* Docker
* Fig
* Git History
* GitLens
* Live Share
* Material Icons
* Path intellisense
* Path Autocomplete
* Prettier
* Python
* Remote
* Project Manager
* Sourcery
* Git Graph
* CodeSnap
* SVG
* JavaScript and TypeScript Nightly
* Marp
* Highlight Matching Tag
* Rust

### Settings for Python `settings.json`

```json
{
  "python.defaultInterpreterPath": "./venv/bin/python",
  "python.formatting.provider": "black",
  "python.formatting.blackArgs": [
      "--line-length 120"
  ],
  "editor.formatOnSave": true,
  "python.envFile": "${workspaceFolder}/.env.test",
  "python.testing.pytestEnabled": true,
  "python.testing.unittestEnabled": false,
  "python.analysis.inlayHints.functionReturnTypes": true,
  "python.analysis.inlayHints.parameterNames": true,
}
```

## Workflows

* Slack connected to GitHub

## Newsletters

* TLDR
* TLDR AI
* Console Dev
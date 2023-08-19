# Mac Setup

## Terminal Tools and Dependencies

* Fig
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
* Xnapper
* GitKraken [Dark with Menlo font]
* Firefox
* Brave
* Notion
* Slack
* Sunsama
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
* Thunder Client
* Project Manager
* Gitlab Workflow
* Sourcery
* Git Graph
* CodeSnap
* SVG
* JavaScript and TypeScript Nightly
* Marp
* Highlight Matching Tag

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

### Debugger for Next.js `launch.json`

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Next.js: debug server-side",
      "type": "node-terminal",
      "request": "launch",
      "command": "npm run dev"
    },
    {
      "name": "Next.js: debug client-side",
      "type": "chrome",
      "request": "launch",
      "url": "http://localhost:3000"
    },
    {
      "name": "Next.js: debug full stack",
      "type": "node-terminal",
      "request": "launch",
      "command": "npm run dev",
      "serverReadyAction": {
        "pattern": "started server on .+, url: (https?://.+)",
        "uriFormat": "%s",
        "action": "debugWithChrome"
      }
    }
  ]
}
```

## Workflows

* Slack connected to Notion for all the comments and actions happening
* Gitlab connected to Slack with webhook

## Newsletters

* TLDR
* TLDR Crypto
* Web Tools Weekly
* PyCoders Weekly
* Real Python
* Bytes
* Console.dev
* Talk Python
* VSCode.Email
* Bitcoin Magazine
* The Hacker News
* Django Newsletter

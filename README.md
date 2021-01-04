# diary_c

## vscode terminal 乱码

    // "terminal.integrated.shellArgs.windows": ["/K chcp 65001 >nul"],
    "terminal.integrated.shellArgs.windows": ["-NoExit", "/c", "chcp 65001"],
    "terminal.integrated.fontFamily": "Lucida Console",

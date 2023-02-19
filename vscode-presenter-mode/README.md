# How to Setup Presenter Mode in Visual Studio Code

## Plugins to install:

Name: Commands <br />
Id: usernamehw.commands <br />
Description: Run one/multiple commands with arguments from Tree View / Status Bar / Quick Pick. <br />
Version: 1.8.0 <br />
Publisher: Alexander <br />
VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=usernamehw.commands <br />

Name: Toggle <br />
Id: rebornix.toggle <br />
Description: Toggle settings in Visual Studio Code <br />
Version: 0.0.2 <br />
Publisher: Peng Lv <br />
VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=rebornix.toggle <br />

## Settings Code

relevant settings.json snippet
```json

"commands.commands": {
    "presenterMode": {
        "sequence": [
            "presetZoom",
            "workbench.action.toggleScreencastMode"
        ],
        "statusBar": {
            "alignment": "left",
            "text": "PresenterMode"
        }
    },
    "presetZoom": {
        "command": "toggle",
        "args": {
            "id": "presetZoom",
            "value": [
                {
                    "window.zoomLevel": 0,
                    "workbench.activityBar.visible": 1
                },
                {
                    "window.zoomLevel": 2,
                    "workbench.activityBar.visible" : 0
                }
            ]
        }
    }
}
```

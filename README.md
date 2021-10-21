# EasyJob

<a href="https://img.shields.io/github/license/akshinmustafayev/EasyJob">
  <img src="https://img.shields.io/github/license/akshinmustafayev/EasyJob" alt="License" />
</a>
<a href="https://img.shields.io/tokei/lines/github/akshinmustafayev/EasyJob">
  <img src="https://img.shields.io/tokei/lines/github/akshinmustafayev/EasyJob" alt="Total lines" />
</a>
<a href="https://img.shields.io/github/downloads/akshinmustafayev/EasyJob/total">
  <img src="https://img.shields.io/github/downloads/akshinmustafayev/EasyJob/total" alt="Downloads" />
</a>
<a href="https://img.shields.io/github/stars/akshinmustafayev/EasyJob?style=social">
  <img alt="GitHub repo file count" src="https://img.shields.io/github/stars/akshinmustafayev/EasyJob?style=social">
</a>
<a href="https://img.shields.io/github/contributors/akshinmustafayev/EasyJob">
  <img alt="GitHub repo file count" src="https://img.shields.io/github/contributors/akshinmustafayev/EasyJob">
</a>


## Description

EasyJob keep and execute your PowerShell and BAT scripts from one interface


## Overview
![image](https://user-images.githubusercontent.com/29357955/138327334-02aedf80-3119-4220-8f2e-1d27ca680e26.png)

![image](https://user-images.githubusercontent.com/29357955/138327363-072fe889-745d-4f57-b8df-7ce567258191.png)

![image](https://user-images.githubusercontent.com/29357955/138327384-740485f3-1a0a-4717-81a0-75f209207c32.png)

![image](https://user-images.githubusercontent.com/29357955/136707408-518324f0-1de3-4b66-9d77-ed186d25c1fe.png)


## Features
* _Remove_ or _Edit_ button from the GUI by right mouse click on it and then select item in the context menu. Settings are automatically will be saved to your config.json file.

![image](https://user-images.githubusercontent.com/29357955/136830752-7c1ab401-3f90-4421-b0d5-21468ac80d08.png)


* _Remove_ or _Add_ tab from the GUI by right mouse click on it and then select Remove Tab in the context menu. Settings are automatically will be saved to your config.json file.

![image](https://user-images.githubusercontent.com/29357955/136830773-9adaf839-fb6f-4019-b537-3d332df94481.png)


* _Add_ button from the GUI by right mouse click on button bar and then select Add button.

![image](https://user-images.githubusercontent.com/29357955/137178361-2cd10c94-a4ac-4673-9d9d-02109ea29f21.png)


* Reorder Tabs from the _Settings->Workflow->Reorder_ tabs window
* Add Tabs from the _Settings->Workflow->Add tab_ window
* Rename Tabs from the _Settings->Workflow->Remove current tab_ window
* Remove Tabs from the _Settings->Workflow->Rename current tab_ window
* Remove Add buttons from the _Settings->Workflow->Add button to current_ tab window
* Reorder buttons from the _Settings->Workflow->Reorder buttons in current_ tab window
* Change application settings from the _Settings->Configuration_ window
* Colored console support


## Configuration

Configuration could be done from config.json file located with the app executable.

Here is an example:

```
{
  "default_powershell_path": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
  "default_cmd_path": "C:\\Windows\\System32\\cmd.exe",
  "powershell_arguments": "",
  "console_background": "Black",
  "console_foreground": "White",
  "clear_events_when_reload": true,
  "restrictions": {
    "block_tabs_remove": false,
    "block_buttons_remove": false,
    "block_tabs_add": false,
    "block_buttons_add": false,
    "block_buttons_reorder": false,
    "block_buttons_edit": false,
    "hide_menu_item_file_reload_config": false,
    "hide_menu_item_file_open_app_folder": false,
    "hide_menu_item_file_clear_events_list": false,
    "hide_menu_item_settings": false,
    "hide_menu_item_settings_workflow": false,
    "hide_menu_item_settings_workflow_reorder_tabs": false,
    "hide_menu_item_settings_workflow_add_tab": false,
    "hide_menu_item_settings_workflow_remove_current_tab": false,
    "hide_menu_item_settings_workflow_rename_current_tab": false,
    "hide_menu_item_settings_workflow_add_button_to_current_tab": false,
    "hide_menu_item_settings_workflow_reorder_buttons_in_current_tab": false,
    "hide_menu_item_settings_configuration": false,
    "hide_menu_item_help": false,
    "hide_menu_item_help_troubleshooting": false,
    "hide_menu_item_help_about": false
  },
  "tabs": [
    {
      "ID": "2e5feab0-527c-451c-b83c-d838d22dacac",
      "header": "Common actions",
      "buttons": [
        {
          "Id": "01bf5871-442e-4f73-91a3-fa13855b609c",
          "text": "test01",
          "description": "Some test script",
          "script": "scripts\\common\\test01.ps1",
          "scriptpathtype": "relative",
          "scripttype": "powershell",
          "arguments": []
        },
        {
          "Id": "9cdc38fa-fc32-4a9d-be78-cd2bfe264422",
          "text": "Bat script",
          "description": "Some BAT script",
          "script": "scripts\\test02.bat",
          "scriptpathtype": "relative",
          "scripttype": "bat",
          "arguments": []
        },
        {
          "Id": "5ec086d9-7987-43ef-84fb-1d8481b05aea",
          "text": "Absolute path script",
          "description": "",
          "script": "C:\\scripts\\absolute_script.ps1",
          "scriptpathtype": "absolute",
          "scripttype": "powershell",
          "arguments": []
        },
        {
          "Id": "c28abef3-494c-48f5-96d8-a5788ced1a23",
          "text": "test04",
          "description": "Some test 04 script with arguments",
          "script": "scripts\\common\\test04.ps1",
          "scriptpathtype": "relative",
          "scripttype": "powershell",
          "arguments": [
            {
              "argument_question": "What is your name?",
              "argument_answer": ""
            },
            {
              "argument_question": "What is your surname",
              "argument_answer": ""
            },
            {
              "argument_question": "No, really what is your name?",
              "argument_answer": ""
            }
          ]
        }
      ]
    },
    {
      "ID": "42f71e1a-32b9-4c16-8c7d-256cd589c52e",
      "header": "Second Tab",
      "buttons": [
        {
          "Id": "3476554c-77b1-4abd-914e-ab1db866fc5f",
          "text": "And this is button too",
          "description": "no description",
          "script": "scripts\\some_button_script.ps1",
          "scriptpathtype": "relative",
          "scripttype": "powershell",
          "arguments": []
        }
      ]
    }
  ]
}
```

_Note 1: Do not specify argument_answer value, since it will be ignored when executing script_

_Note 2: ID my be any other random GUID number. You may not specify it, application will regenerate it after changes if it is absent or not present._


## Easy access
_CTRL+Left Mouse Click_ on the button will open folder where script attached to the button is located

_SHIFT+Left Mouse Click_ on the button will open the script attached to the button with your default ps1 text editor

## Compilation

1. Download and install .NET 5 SDK from [Here](https://dotnet.microsoft.com/download/visual-studio-sdks)
2. Download source code and extract it to __C:\temp__
3. Open Command Promt (cmd) from the start menu
4. Execute __cd C:\temp\EasyJob-main__
5. Execute __dotnet build -c release__

![image](https://user-images.githubusercontent.com/29357955/136832285-faf648b8-350f-4f23-9a88-7caf0a5a9bfd.png)

6. Open __C:\temp\EasyJob-main\bin\Release\net5.0-windows__ and execute __EasyJob.exe__

![image](https://user-images.githubusercontent.com/29357955/136832429-e348ae24-051a-4e30-af9f-f52d3819270a.png)


## Contributing

Contribution is very much appreciated. Hope that this tool might be useful for you!

Thanks to the contributors:

<a href="https://github.com/akshinmustafayev/EasyJob/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=akshinmustafayev/EasyJob" />
</a>


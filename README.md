# Better Cron Tasks

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)
[![Visual Studio Marketplace Version](https://img.shields.io/visual-studio-marketplace/v/Freaxys.better-cron-tasks?label=VS%20Marketplace)](https://marketplace.visualstudio.com/items?itemName=Freaxys.better-cron-tasks)

Based on the [Cron Tasks](https://github.com/zokugun/vscode-cron)

With [Better Cron Tasks](https://github.com/Freaxys/better-cron-tasks), you can schedule tasks/jobs to run periodically at fixed times, dates, or intervals.

## HowTo

In your settings.json:

```jsonc
"cronTasks.tasks": [
    {
        "at": "* * * * *",
        "run": "workbench.action.tasks.runTask",
        "args": ["nameOfYourTask"]
    },
],
```

-   `at`: a [cron expression](https://en.wikipedia.org/wiki/Cron)
-   `run`: a vscode command
-   `args`: argument you want to pass to the command

## Debugging

The extension always prints out debug information into the channel `Cron Tasks` of the panel `Output` (menu: `View` / `Output`).

But if the property `cronTasks.debug` (`false` by default) is `true` or `"on"`, the extension will bring that channel to focus.

### blank

With `"cronTasks.debug": "useBlank"`, the extension will print out debug information as usual but it won't call the final task.

### test command

The command `cronTasks.showTestMessage` will display a simple notification.

## Notification

The property `cronTasks.notification` (`minor` by default) indicates when to show the update notification.

**Enjoy!**

## Attributions

<a href="https://www.flaticon.com/free-icons/clock" title="clock icons">Clock icons created by Freepik - Flaticon</a>

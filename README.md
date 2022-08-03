## HCL OneTest UI

This action enables you to run HCL OneTest UI tests.

## Pre requisites

1. Create a github repository
2. Create a folder named ".github/workflows" in the root of the repository
3. Create a .yml file with any name inside the ".github/workflows" folder
4. Then you need to code thta yml file as mentioned in the following example.

## Example usage

```yaml
name: HCL OneTest UI

on: workflow_dispatch

jobs:
    UI-Action:
        runs-on: self-hosted
        name: HCL OneTest UI
        steps:
         - name: Execute Test
           uses: anuraag-k/FunctionalTestAction@main
           with:
            projectDirectory: 
            scriptName: 
            iterationCount:
            logFormat:  
            userArguments:

```
5. Push it into the main branch
6. To configure agent:
    1. Go to settings (Repo).
    2. Select action -> runner.
    3. Click Create self-hosted runner, follow the download and configure instruction

7. Go to the Actions section in the repository and select the workflow.
8. Click the Run workflow dropdown and the list of input text boxes are displayed.
9. After entering the input values click on run workflow button

## Inputs

### `projectDirectory`

**Required** Fully qualified path to the HCL OneTest UI project directory.

### `scriptName`

**Required** Name of the script to be executed without the extension. For eg., Script1 or TestFolder.Script1 in case Script1 is in a folder named TestFolder.

### `iterationCount`
**Optional** Number of dataset iterations to be run.

### `logFormat`

**Optional** Format of script execution logs. Choose from Default, none, json, xml, html, text, and TPTP.

### `userArguments`

**Optional** Additional playback arguments, if any. If there are multiple arguments, you must enclose each argument within double quotes and separate the arguments by providing a space between them.



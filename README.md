# Codecov global executable uploader for PowerShell and Windows Command Line.

| [https://codecov.io/](https://codecov.io/) | [@codecov](https://twitter.com/codecov) | [hello@codecov.io](mailto:hello@codecov.io) |
| ------------------------ | ------------- | --------------------- |

**This repository is currently under active development working towards version 0.1.0. All types of contributions are welcome! Feel free to open an issue or ask a question.**

This uploader supports Windows Command Line and PowerShell on Windows 7 (x64) and above. If you need support for OS X or Linux use the [bash global uploader](https://github.com/codecov/codecov-bash).

## Current features

- Upload a coverage report using the following services: AppVeyor, TeamCity (not tested), Git.
- Many Codecov CLI options are supported. Run `.\codecov.exe` or see [Options.cs](https://github.com/codecov/codecov-exe/blob/master/source/codecov/codecov/Program/Options.cs) for more details.
- You can obtain the uploader via
	- NuGet [![NuGet](https://img.shields.io/nuget/v/Codecov.svg)](https://www.nuget.org/packages/Codecov/)
	- Chocolatey [![Chocolatey](https://img.shields.io/chocolatey/v/codecov.svg)](https://chocolatey.org/packages/codecov)
	- As the asset *Codecov.zip* under the release.

For the last option, the following PowerShell (version 5) commands might be helpful

```PowerShell
(New-Object System.Net.WebClient).DownloadFile("<url>", (Join-Path $pwd "Codecov.zip")) # Download Codecov.zip from github release.
Expand-Archive .\Codecov.zip -DestinationPath . # UnZip the file.
.\Codecov\codecov.exe ... # Run codecov.exe with whatever commands you need.
```

## ToDoList

- High Priority
    - Implement (if any) must have CLI options.
    - Bug fixes and code cleanup in order to release version 0.1.0.
- Lower Priority
    - Unit Tests, build scripts, and automation.
    - Support Mercurial and other CI services.
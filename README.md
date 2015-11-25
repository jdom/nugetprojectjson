# nugetprojectjson
Scripting to convert projects with packages.config to a project with project.json nuget depedencies.
Will recusively walk all subfolders of the folder from which it was called.

Please note that it might also convert packages.config that is in your .nuget.
besides converting packages.config to project.json it also changes the csproj files:
* Removes all hint paths to nuget dependency assemblies.
* removes packages.config from csproj
* Removes EnsureNugetPackageBuildImports
* Add project.json file

Add a couple of properties that have been found by users to make sure that for example Nunit assemblies are copied to the output folder.
* add targetFrameworkProfile property
* add CopyNuGetImplementations = true property
* add PlatformTarget AnyCpu

* replace toolsversion with "14.0"


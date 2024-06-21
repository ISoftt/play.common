# play.common
Common library used by Play Economy services.

## Create and publish package
```powershell
$version="1.0.5"
$owner="ISoftt"
$github_personal_access_token="specify here"

dotnet pack src\Play.Common\ --configuration Release -p:PackageVersion=$version -p:RepositoryUrl=https://github.com/$owner/play.common -o ..\packages

dotnet nuget push ..\packages\Play.Common.$version.nupkg --api-key $github_personal_access_token --source "github"
```

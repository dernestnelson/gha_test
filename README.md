# Sample .NET app + GitHub Actions CI/CD

This repository contains a minimal .NET console app and CI/CD workflows.

Projects:
- src/SampleApp: Console app (net8.0)
- tests/SampleApp.Tests: xUnit tests

Workflows:
- .github/workflows/ci.yml — Build, test, publish and upload artifact on push/PR
- .github/workflows/cd.yml — On tags `v*` builds and creates a GitHub Release with the published artifact

Run locally:
- Restore: `dotnet restore`
- Build: `dotnet build`
- Run: `dotnet run --project src/SampleApp`
- Test: `dotnet test`

Suggested git workflow to add these files (from repo root):
```bash
git fetch origin
# update or create the branch locally tracking remote
git checkout -B add-dotnet-sample origin/add-dotnet-sample
# copy the files into the working tree (or create them)
git add .
git commit -m "Add .NET sample app and CI/CD workflows"
git push --set-upstream origin add-dotnet-sample
# then open a PR on GitHub from add-dotnet-sample -> main
```

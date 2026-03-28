# Test

[![GitHub Pages](https://img.shields.io/badge/%20-white?style=social&logo=githubpages&logoColor=black&logoSize=auto)](https://fjrodafo.github.io/Test/)
[![GitHub Stars](https://img.shields.io/github/stars/FJrodafo/Test?style=social&logo=github&logoColor=black&label=Stars&labelColor=white&color=white)](https://github.com/FJrodafo/Test/stargazers)

[![Apache Maven](https://img.shields.io/badge/test-white?style=flat&logo=apachemaven&logoColor=C71A36)](https://github.com/FJrodafo/Test/packages/2915747)
[![Containers](https://img.shields.io/badge/test-white?style=flat&logo=docker&logoColor=2496ED)](https://github.com/FJrodafo/Test/pkgs/container/test)
[![npm](https://img.shields.io/badge/test-white?style=flat&logo=npm&logoColor=CB3837)](https://github.com/FJrodafo/Test/pkgs/npm/test)
[![NuGet](https://img.shields.io/badge/test-white?style=flat&logo=nuget&logoColor=004880)](https://github.com/FJrodafo/Test/pkgs/nuget/test)
[![RubyGems](https://img.shields.io/badge/test-white?style=flat&logo=rubygems&logoColor=E9573F)](https://github.com/FJrodafo/Test/pkgs/rubygems/fjrodafo-test)

## Index

1. [Introduction](#introduction)
2. [Project structure](#project-structure)
3. [Clone the repository](#clone-the-repository)
4. [Apache Maven](#apache-maven)
5. [Containers](#containers)
6. [npm](#npm)
7. [NuGet](#nuget)
8. [RubyGems](#rubygems)
9. [Resources](#resources)

## Introduction

A repository for trying out new things!

This project has been developed on a [Linux](https://github.com/torvalds/linux) system. To learn more about the system, visit the [Dotfiles](https://github.com/FJrodafo/Dotfiles) repository.

## Project structure

```
/
├── docs/
|   ├── _config.yaml
|   ├── CODE_OF_CONDUCT.md
|   ├── README.md
|   └── SECURITY.md
├── Packages/
|   ├── Apache_Maven/
|   ├── Containers/
|   ├── npm/
|   ├── NuGet/
|   └── RubyGems/
├── CONTRIBUTING
└── LICENSE
```

## Clone the repository

Open a terminal in the directory where you store your repositories and clone it with the following command:

```shell
# HTTPS
git clone https://github.com/FJrodafo/Test.git
```

```shell
# SSH
git clone git@github.com:FJrodafo/Test.git
```

## Apache Maven

```shell
# Packages Commands
cd Apache_Maven/
mvn package
java -cp target/test-1.0.0.jar Test
```

```shell
# Deploy to GitHub Packages
mvn deploy
```

## Containers

```shell
# Packages Commands
cd Containers/
docker build -t test .
docker run --rm test:latest
```

```shell
# Push to Docker Hub
docker tag test:latest fjrodafo/test:1.0.0
docker push fjrodafo/test:1.0.0
```

```shell
# Push to GitHub Packages
docker tag test:latest ghcr.io/fjrodafo/test:1.0.0
docker push ghcr.io/fjrodafo/test:1.0.0
```

## npm

```shell
# Packages Commands
cd npm/
npm init -y
npm start
```

```shell
# Publish to npm
npm run publish:npm
```

```shell
# Publish to GitHub Packages
npm run publish:github
```

## NuGet

```shell
# Packages Commands
cd NuGet/
dotnet new console -n test
cd test/
dotnet run
dotnet pack --configuration Release
```

```shell
# Push to NuGet
dotnet nuget push bin/Release/test.1.0.0.nupkg \
    --api-key API_KEY \
    --source https://api.nuget.org/v3/index.json
```

```shell
# Push to GitHub Packages
dotnet nuget push bin/Release/test.1.0.0.nupkg \
    --source "github"
```

## RubyGems

```shell
# Packages Commands
cd RubyGems/
ruby lib/fjrodafo/test.rb
gem build fjrodafo-test.gemspec
```

```shell
# Push to RubyGems
gem push fjrodafo-test-1.0.0.gem
```

```shell
# Push to GitHub Packages
gem push --key github --host https://rubygems.pkg.github.com/FJrodafo fjrodafo-test-1.0.0.gem
```

## Resources

[GitHub Docs](https://docs.github.com/en)
·
[GitHub Actions](https://docs.github.com/en/actions)
·
[GitHub Packages](https://docs.github.com/en/packages)
·
[GitHub Pages](https://docs.github.com/en/pages)

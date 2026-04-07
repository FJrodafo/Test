# Test [![&#x25B2;Vercel](https://img.shields.io/badge/&#x25B2;Vercel-black?style=flat)](https://fjrodafo.vercel.app/)

[![GitHub Pages](https://img.shields.io/badge/%20-FFFFFF?style=social&logo=githubpages&logoColor=black&logoSize=auto)](https://fjrodafo.github.io/Test/)
[![GitHub Stars](https://img.shields.io/github/stars/FJrodafo/Test?style=social&logo=github&logoColor=black&label=Stars&labelColor=FFFFFF&color=FFFFFF)](https://github.com/FJrodafo/Test/stargazers)

[![Apache Maven](https://img.shields.io/badge/test-FFFFFF?style=flat&logo=apachemaven&logoColor=D22128)](https://github.com/FJrodafo/Test/packages/2915747)
[![Containers](https://img.shields.io/badge/test-FFFFFF?style=flat&logo=docker&logoColor=2560FF)](https://github.com/FJrodafo/Test/pkgs/container/test)
[![npm](https://img.shields.io/badge/test-FFFFFF?style=flat&logo=npm&logoColor=CD0000)](https://github.com/FJrodafo/Test/pkgs/npm/test)
[![NuGet](https://img.shields.io/badge/test-FFFFFF?style=flat&logo=nuget&logoColor=004880)](https://github.com/FJrodafo/Test/pkgs/nuget/test)
[![RubyGems](https://img.shields.io/badge/test-FFFFFF?style=flat&logo=rubygems&logoColor=E9573F)](https://github.com/FJrodafo/Test/pkgs/rubygems/fjrodafo-test)

[![Apache Maven](https://img.shields.io/badge/test-D22128?style=flat&logo=apachemaven&logoColor=FFFFFF)](https://github.com/FJrodafo/Test/packages/2915747)
[![Containers](https://img.shields.io/badge/test-2560FF?style=flat&logo=docker&logoColor=FFFFFF)](https://github.com/FJrodafo/Test/pkgs/container/test)
[![npm](https://img.shields.io/badge/test-CD0000?style=flat&logo=npm&logoColor=FFFFFF)](https://github.com/FJrodafo/Test/pkgs/npm/test)
[![NuGet](https://img.shields.io/badge/test-004880?style=flat&logo=nuget&logoColor=FFFFFF)](https://github.com/FJrodafo/Test/pkgs/nuget/test)
[![RubyGems](https://img.shields.io/badge/test-E9573F?style=flat&logo=rubygems&logoColor=FFFFFF)](https://github.com/FJrodafo/Test/pkgs/rubygems/fjrodafo-test)

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
cd Packages/Apache_Maven/
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
cd Packages/Containers/
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
cd Packages/npm/
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
cd Packages/NuGet/
dotnet new console -n test
cd test/
dotnet run
dotnet pack --configuration Release
```

```shell
# Push to NuGet
dotnet nuget push bin/Release/test.1.0.1.nupkg \
    --api-key API_KEY \
    --source https://api.nuget.org/v3/index.json
```

```shell
# Push to GitHub Packages
dotnet nuget push bin/Release/test.1.0.1.nupkg \
    --source "github"
```

## RubyGems

```shell
# Packages Commands
cd Packages/RubyGems/
ruby lib/fjrodafo/test.rb
gem build fjrodafo-test.gemspec
```

```shell
# Push to RubyGems
gem push fjrodafo-test-1.0.1.gem
```

```shell
# Push to GitHub Packages
gem push --key github --host https://rubygems.pkg.github.com/FJrodafo fjrodafo-test-1.0.1.gem
```

## Resources

[GitHub Docs](https://docs.github.com/en)
·
[GitHub Actions](https://docs.github.com/en/actions)
·
[GitHub Packages](https://docs.github.com/en/packages)
·
[GitHub Pages](https://docs.github.com/en/pages)

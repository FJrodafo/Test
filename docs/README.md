# Test

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cubilia sodales pellentesque risus scelerisque volutpat sit turpis. Potenti justo erat, torquent turpis dolor porta proin hac nibh fames. Pellentesque nisi feugiat aptent orci, risus sed, at taciti nisl massa ad. Dapibus conubia eleifend nunc nulla purus nibh. Gravida inceptos varius mauris consectetur scelerisque justo. Accumsan varius quisque blandit malesuada aenean quis quis suscipit. Duis iaculis rutrum suscipit est fusce volutpat blandit libero lacus fames eget. A magna turpis, est litora, inceptos, pharetra maximus. Sapien tristique inceptos massa, diam tincidunt.

## Index

1. [Apache Maven](#apache-maven)
2. [Containers](#containers)
3. [npm](#npm)
4. [NuGet](#nuget)
5. [RubyGems](#rubygems)
6. [Releases](#releases)
7. [Resources](#resources)

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

## Releases

Download the files:

```shell
wget https://github.com/FJrodafo/Test/releases/download/1.0.0/apache_maven-1.0.0.zip
wget https://github.com/FJrodafo/Test/releases/download/1.0.0/apache_maven-1.0.0.tar.gz
wget https://github.com/FJrodafo/Test/releases/download/1.0.0/apache_maven-1.0.0.sha256
wget https://github.com/FJrodafo/Test/releases/download/1.0.0/apache_maven-1.0.0.sigstore.json
```

Verify the signature of the hash file:

```shell
cosign verify-blob \
  --bundle apache_maven-1.0.0.sigstore.json \
  --certificate-identity-regexp="https://github.com/FJrodafo/Test" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com" \
  apache_maven-1.0.0.sha256
```

Verify the files match the hashes:

```shell
sha256sum --check apache_maven-1.0.0.sha256
```

## Resources

[Apache Maven](https://github.com/FJrodafo/Test/packages/2915747)
·
[Containers](https://github.com/users/FJrodafo/packages/container/package/test)
·
[npm](https://github.com/users/FJrodafo/packages/npm/package/test)
·
[NuGet](https://github.com/users/FJrodafo/packages/nuget/package/test)
·
[RubyGems](https://github.com/users/FJrodafo/packages/rubygems/package/fjrodafo-test)

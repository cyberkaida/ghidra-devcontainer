# ghidra-devcontainer
A [devcontainer](https://containers.dev) for Ghidra development!

You can use the GitHub UI, Visual Studio Code or a local tool like [devpod](https://devpod.sh) to create the devcontainer.

## Building Ghidra

Once in the container you can build Ghidra from source. You can either build the latest development version or a specific stable release.

### Building the Latest Development Version

```sh
git clone git@github.com:NationalSecurityAgency/ghidra.git
cd ghidra
gradle -I gradle/support/fetchDependencies.gradle
gradle prepDev
gradle buildGhidra
```

### Building a Specific Release

Since Ghidra 11.3, several new stable versions have been released. You can build any of these specific versions:

**Available Versions (since 11.3):**
- **11.4.1** (July 2025) - Latest stable release
- **11.4** (June 2025)
- **11.3.2** (April 2025)
- **11.3.1** (February 2025)

To build a specific version, checkout the release tag before building:

```sh
git clone git@github.com:NationalSecurityAgency/ghidra.git
cd ghidra
# Checkout specific version (example: 11.4.1)
git checkout Ghidra_11.4.1_build
gradle -I gradle/support/fetchDependencies.gradle
gradle prepDev
gradle buildGhidra
```

You can replace `Ghidra_11.4.1_build` with any of the available release tags:
- `Ghidra_11.4.1_build`
- `Ghidra_11.4_build`  
- `Ghidra_11.3.2_build`
- `Ghidra_11.3.1_build`

## Python Integration

Install the Python3 Ghidra pip package and use PyGhidra:

```sh
pipx install ./Ghidra/Features/PyGhidra/src/main/py/
```

## Extension Development

You can also work on extensions! The devcontainer includes all the necessary tools for Ghidra extension development.

## Release Information

For detailed information about each release, including new features and bug fixes, check the official release pages:
- [Ghidra Releases](https://github.com/NationalSecurityAgency/ghidra/releases)
- [What's New Documentation](https://github.com/NationalSecurityAgency/ghidra/blob/master/Ghidra/Configurations/Public_Release/src/global/docs/WhatsNew.md)

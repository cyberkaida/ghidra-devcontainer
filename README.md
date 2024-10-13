# ghidra-devcontainer
A [devcontainer](https://containers.dev) for Ghidra development!

You can use the GitHub UI, Visual Studio Code or a local tool like [devpod](https://devpod.sh) to create the devcontainer.

Once in the container you can do things like build Ghidra:

```sh
git clone git@github.com:NationalSecurityAgency/ghidra.git
cd ghidra
gradle -I gradle/support/fetchDependencies.gradle
gradle prepDev
gradle buildGhidra
```

Install the Python3 Ghidra pip package and use PyGhidra:

```sh
pipx install ./Ghidra/Features/PyGhidra/src/main/py/
```

You can also work on extensions!

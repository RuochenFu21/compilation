# compilation
Compile Minecraft Mod

this action is VERY simple

so if you wants to compile your mod with a github action and you're too lazy to make one...
just do 
```
name: Compiling

on:
  push:
  pull_request:

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - name: Compile
      uses: Ruochenfu2011/compilation@v1
      
    - name: Archive Artifacts
      uses: actions/upload-artifact@v2
      with:
        name: Artifacts
        path: ./build/libs
```

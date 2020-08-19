# Dotnet - Docker mod for code-server

This mod adds dotnet-sdk to code-server, to be installed/updated during container start.
Current versions:
* 2.1
* 3.1

In code-server docker arguments, set an environment variable `DOCKER_MODS=linuxserver/mods:code-server-dotnet`

If adding multiple mods, enter them in an array separated by `|`, such as `DOCKER_MODS=linuxserver/mods:code-server-dotnet|linuxserver/mods:code-server-mod2`

# Mod creation instructions

* Ask the team to create a new branch named `<baseimagename>-<modname>`. Baseimage should be the name of the image the mod will be applied to. The new branch will be based on the `template` branch.
* Fork the repo, checkout the newly created branch.
* Edit the `Dockerfile` for the mod. `Dockerfile.complex` is only an example and included for reference; it should be deleted when done.
* Inspect the `root` folder contents. Edit, add and remove as necessary.
* Edit this readme with pertinent info, delete these instructions.
* Finally edit the `travis.yml`. Customize the build branch, and the vars for `BASEIMAGE` and `MODNAME`.
* Submit PR against the branch created by the team.
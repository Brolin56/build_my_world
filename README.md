# The Build_My_World Package

This is a standalone package which contains a world file that can be run on a gazebo simulator. This package can also be used in conjunction with other **ROS** packages wherein this package can used to save your customized simulation environments.

## Requirement

- Gaezebo (Version 7 preferable). You can find help for installing gazebo and other related packages [here](http://gazebosim.org/tutorials?tut=ros_installing)

## Working with this package

You can download the package by typing the following command in your terminal

```
$ mkdir custom_environment
$ cd custom_enviroment
$ git init
$ git clone https://github.com/brolinA/build_my_world.git
```
**For those people who are now to git, you can install git by following the guidelines [here](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-16-04) and then follow the steps mentioned above**

After you download the package you can straightaway run the world using the gazebo simulator.

Change directory to _custom_environment_ and use the following commands
```
$ cd build_my_world/world
$ export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/brolin/Documents/projects/build_my_world/build
$ gazebo basement_world.world
```
The export command lets you load the plug-in that show a greeting message when you run the gazebo simulator. **Make sure to edit the path as per your directory path**. You can also add the export command in the _bashrc_ file to load the plugin automatically.

The plug-in is a simple message that you can edit to display your own message. It is intutive can be found in *scripts/description.cpp* .

After you edit the plug-in file, you need to build the file. Change directory to _build_my_world_ and use the following instruction.

```
$cd build
$ cmake ../
$ make
```

## Contributing

You can contribute to this project by adding some of your own custom environments other than what Gazebo normally provide so that it can be useful and time saving for other users who seek a simulation environment in gazebo.

## License

The project can be reused if the Terms mentioned in the [LICENSE](LICENSE) file.

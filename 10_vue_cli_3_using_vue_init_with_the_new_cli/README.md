# 10_vue_cli_3_using_vue_init_with_the_new_cli

1. this latest version of the vue cli supports the old way of creating projects using vue init
2. this way of creating projects is still used by many developers, however in order to use the old command - vue init, we need to install a bridging package globally
3. so if we try to use vue init, then it will not work
vue init webpack-simple test
command vue init requires a global addon to be installed.
we have to run
npm install -g @vue/cli-init 
4. this is kind of like a bridging package to bridge the new vue cli with the old command, then we can use vue init 
5. now we can use vue init
vue init webpack-simple vuecli3-vue-init
6. this is now going to create that project for us using the old command
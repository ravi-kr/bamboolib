# Work in Progress: Plugins - add your own transformations

> __Beta:__ Plugins are currently in Beta and the API is not stable yet. Please expect that the API might change to some extent. However, we will try to minimize any changes and provide backwards compatibility.

## Scenario:
- Are you __missing a special transformation__ in bamboolib?
- Do you want to provide __custom transformations for your team__?


Starting with version 1.3.0 bamboolib enables you to write custom transformation plugins.


## Get started

1) make sure that you are running bamboolib 1.3.0 or higher. You can check this via running: `bam.__version__` If you need to upgrade, please [follow this guide](https://docs.bamboolib.8080labs.com/how-tos/update-to-a-new-version-of-bamboolib)

2) write your own plugin or copy an example

3) execute the plugin code

4) use the plugin from within the bamboolib user interface


## How to permanently add my plugin to bamboolib?

3 things you should know about how plugins work:
- __Plugins are added to bamboolib after you execute the plugin code.__
- If you add a plugin, it will be available as long as the Python kernel is running.
- If you restart your Python kernel, the plugin will no longer be available.

Therefore, there are __multiple alternatives__ how to permanently add your plugin:
1. Put the plugin code into a Python file in the IPython auto startup folder which is located in your home directory at `~/.ipython/profile_default/startup` This code is run by IPython every time you start a new Jupyter Python kernel.
2. Put the plugin code into a Python package and quickly import the package at the top of your Jupyter Notebook. For example, you can quickly create a new Python package with pyscaffold [pyscaffold](https://github.com/pyscaffold/pyscaffold). You might also want to upload your own plugin package to a private or public GitHub repository and collaborate with others to make sure that you will always have the best plugins available for your use case.
3. Combine the alternatives 1. and 2. via adding the import to your package to the IPython auto-import.
4. Just add the plugin code at the top of your Jupyter Notebook. This is a little bit clunky to do it for every new notebook but it would work.


Do you have __another idea__ on how to always execute your plugins? Let us know via the issues. Your approach might be helpful to others as well :)


## Reference
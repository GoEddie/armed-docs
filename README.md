# armed-docs
Repository for the armed vs code extension

<img src="https://github.com/GoEddie/armed-docs/blob/master/ARMED.gif?raw=true" />

# WHAT IS ARMED?

Armed is an extension for vs code that helps write AZURE ARM templates.

Armed has a treeviewer similar to the arm tools fot visual studio except this viewer enumerates all the properties of a respurce instead of just the resources.

Armed's killer feature is the ability to test arm template functions locally so you can test any scripts in the templates *without* having to deploy them, _WoW_

## TODO:

Some functions like reference and listKeys are stubs they dont actually call the real function but I have implemented local versions of pretty much every other function.

## FAQ

### My parameters are not showing or say "(MISSING Parameter ... Value)"

Armed uses the parameters file to get the actual values which overwrite any default values in the main template. If you call your parameters file 'parameters.json' in the same folder as your template then armed finds it and uses it.

If your parameters are in a file with a different name, you can go to the workspace root and find the .vscode directory (you can create it if it doesn't exist) and create an armed.json with this json:

   {
      "parameterFile": "parametersFileName.json"
   }

then try again and the parameters will be picked up.

## STUCK?

Raise an issue here if you get stuck and ill help you :)


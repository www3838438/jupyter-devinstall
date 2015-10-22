# Jupyter devinstall tool
Utility designed to simplify the installation of a Jupyter/IPython development environment.

![Demo screen cast](/demo.gif)

## Installation
Make sure you have iojs (and npm, which is included) installed on your machine, then run:

```
npm install -g jupyter-devinstall
```

(you may need to prefix the line with `sudo `)

## Usage

```
Usage: jupyter-devinstall [options] <githubName> <installdir>

Options:

  -h, --help               output usage information
  -r, --reinstall          reinstall existing repositories, without recloning
  -o, --overwrite          overwrite existing directories
  -u, --upstream [string]  name of the upstream git remote [upstream]
  -g, --global             global install
  -n, --noInstall          don't install
  -s, --silent             don't prompt the user for anything
  -V, --version            output the version number
```

Example for GitHub username `jdfreder` installed to the HOME directory:

```
jupyter-devinstall jdfreder ~/
```

## Notes

If you have specified the `--silent` (`-s` for short) flag, part way through the 
tool will behave like a wizard, prompting you for input.  
  
The tool will ask you if you want to install locally, globally, or not at all:  
- locally - pip install each repository  
- globally - pip install each repository with the `-g` flag.  This may require sudo, which may have undesired side effects.  
- not at all - doesn't pip/npm install anything  

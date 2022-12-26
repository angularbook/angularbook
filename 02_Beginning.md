# Beginning

## Required

* Operation System: Windows, Linux or macOS
* NodeJS
* Git
* IDE or code editor

## NodeJS

The NodeJS a JavaScript runtime environment. Download the latest version from the website:

* [https://nodejs.org](https://nodejs.org)

### Windows Chocolatey package manager

If we have installed Cholotay, you can install the NodeJS next command:

```cmd
choco install nodejs
```

### Install Debian GNU/Linux

You can install the apt command from repository:

```bash
apt install nodejs
```

Or, you can download latest version, but the LTS verson is recommended. Recommended website:

* [https://github.com/nodesource/distributions](https://github.com/nodesource/distributions)

### Checking the commands

```cmd
node --version
npm --version
```

## Install the Angular CLI

### On Windows

```cmd
npm install -g @angular/cli
```

On Windows client set in the PowerShell, the execution policy:

```cmd
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```

Now, you must set the Path environment variable the next directory path:

* c:\Users\user\AppData\Romaing\npm

Change the username to your own.

### On Linux

As root user install:

```bash
npm install -g @angular/cli
```

### Check Angular/CLI

Do not proceed until this works.

```cmd
ng --version
```

## Make new Angular project

Name the new project app01. Then:

```cmd
ng new app01
```

The ng command starts in interctive mode. It asks the following two things:

* Do we want routing?
* How we want to provide style information.

Teh output might look like this:

```cmd
ng new app01
? Would you like to add Angular routing? (y/N)
```

Next question:

```cmd
ng new app01
? Would you like to add Angular routing? No
? Which stylesheet format would you like to use? (Use arrow keys)
❯ CSS 
  SCSS   [ https://sass-lang.com/documentation/syntax#scss                ] 
  Sass   [ https://sass-lang.com/documentation/syntax#the-indented-syntax ] 
  Less   [ http://lesscss.org                                             ] 
```

If we have answered the questions:

```cmd
ng new app01
? Would you like to add Angular routing? No
? Which stylesheet format would you like to use? CSS
CREATE app01/README.md (1059 bytes)
CREATE app01/.editorconfig (274 bytes)
CREATE app01/.gitignore (548 bytes)
CREATE app01/angular.json (3033 bytes)
CREATE app01/package.json (1068 bytes)
CREATE app01/tsconfig.json (863 bytes)
CREATE app01/.browserslistrc (600 bytes)
CREATE app01/karma.conf.js (1422 bytes)
CREATE app01/tsconfig.app.json (287 bytes)
CREATE app01/tsconfig.spec.json (333 bytes)
CREATE app01/.vscode/extensions.json (130 bytes)
CREATE app01/.vscode/launch.json (474 bytes)
CREATE app01/.vscode/tasks.json (938 bytes)
CREATE app01/src/favicon.ico (948 bytes)
CREATE app01/src/index.html (291 bytes)
CREATE app01/src/main.ts (372 bytes)
CREATE app01/src/polyfills.ts (2338 bytes)
CREATE app01/src/styles.css (80 bytes)
CREATE app01/src/test.ts (745 bytes)
CREATE app01/src/assets/.gitkeep (0 bytes)
CREATE app01/src/environments/environment.prod.ts (51 bytes)
CREATE app01/src/environments/environment.ts (658 bytes)
CREATE app01/src/app/app.module.ts (314 bytes)
CREATE app01/src/app/app.component.css (0 bytes)
CREATE app01/src/app/app.component.html (23332 bytes)
CREATE app01/src/app/app.component.spec.ts (953 bytes)
CREATE app01/src/app/app.component.ts (209 bytes)
✔ Packages installed successfully.
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint:   git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint:   git branch -m <name>
    Successfully initialized git.
```

On weaker machines, creating teh project can take even minutes.

## Start the project

If already the project, change the in directory of project:

```cmd
cd app01
```

In the project folder use the next command:

```cmd
ng serve -o
```

## The Code editor

We using Visual Studio Code editor. Download from the website:

* [https://code.visualstudio.com/](https://code.visualstudio.com/)

On Windows, if we have a intalled Choclatey package manager, use this command:

```cmd
choco install vscode.install
```

In new command window check:

```cmd
code --version
```

Change to the project directory if necessary. To start the Visual Studio Code, in commandline use next command:

```cmd
code .
```

The dot represents the current directory.

Recommended extension to Visual Studio Code:

* Angular Language Service

## The project structure

Let's review the project's directories and files.

```txt
app01/
  |-.vscode/
  |-node_modules/
  |-src/
  |-.browserslistrc
  |-.editorconfig
  |-.gitignore
  |-angular.json
  |-karma.conf.js
  |-package-lock.json
  |-package.json
  |-README.md
  |-tsconfig.app.json
  |-tsconfig.json
  `-tsconfig.spec.json
```

Apart from the src directory, all files and directories support the use of the project. The project is developed in the src directory. Let's look at the src directory in more detail.

```txt
src/
  |-app/
  |  |-app.component.css
  |  |-app.component.html
  |  |-app.component.spec.ts
  |  |-app.component.ts
  |  `-app.module.ts
  |-assets/
  |  `-.gitkeep
  |-environments/
  |  |-environment.prod.ts
  |  `-environment.ts
  |-favicon.ico
  |-index.html
  |-main.ts
  |-polyfills.ts
  |-styles.css
  `-test.ts
```

The site's entry point is index.html with the styles.css file.

The index.html content:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>App01</title>
  <base href="/">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="icon" type="image/x-icon" href="favicon.ico">
</head>
<body>
  <app-root></app-root>
</body>
</html>
```

There is an angular element called app-root. The content of app.component.html in the app directory is replaced here.

The styles.css content:

```css
/* You can add global styles to this file, and also import other style files */
```

The CSS file contains only one comment.

In general, we edit the content of the app directory, this gives the content of the website. An Angular web page consists of components. At startup, we have a main component, which can be found in the app directory.

In the app directory, the file app.module.ts is always created next to the main component, in which we register the Angular modules we want to use.

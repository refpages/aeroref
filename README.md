# AeroRef

When developing content for these references pages, we suggest that you preview the website on a local server rather than pushing your changes to this repository and looking at them online. Here is how to preview the website locally on MacOS:

* Open a terminal and go to wherever you put the `aeroref` repository.
* If you haven't done so already, install [Homebrew](https://brew.sh) by running the following command:
```zsh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
* As a reminder, it is good practice to [keep Homebrew up to date](https://docs.brew.sh/FAQ#how-do-i-update-my-local-packages) from time to time by running the following two commands:
```zsh
brew update
brew upgrade
```
* After you have installed Homebrew and have confirmed that it is up to date, install [NodeJS](https://nodejs.org/) by running the following comamnd:
```zsh
brew install node
```
* Install all dependencies by running the following command:
```zsh
npm install
```
* Start the server by running the following command:
```zsh
npm run astro dev --verbose
```
* Open a browser window and navigate to [http://localhost:4321/](http://localhost:4321/).

Changes you make to the pages will appear live in the browser window.


# Running the pages locally (OUTDATED)

These instructions are outdated and will be removed.

## <a id="windows">Windows</a>

### Installing required programs

Download <a href="https://github.com/apps/desktop">GitHub Desktop</a>. Once installed, login using the GitHub account with which you have collaborator access to the aeroref repository. Once logged in clone the aeroref repository.

Download <a href="https://nodejs.org/en/download/prebuilt-installer">NodeJS</a>. By default, the installer should also install Node Package Manager/NPM, but double check that is the case.

### Before running the pages for the first time

Open the Windows command prompt (Windows key + R and type in `cmd`, or type in `cmd` in the search menu.) Make sure it is not ran as administrator, such that the first line reads `C:\Users\<user>`, where `<user>` is the username of the current Windows user.

By default, the repository should be at `C:\Users\<user>\Documents\GitHub\aeroref`. Run the command 
```
cd Documents\GitHub\aeroref
```
You should now see that the beginning of the line reads the correct location referenced previously. 

Install all dependencies by running 
```
npm install
```

### Running the server

Make sure you are in the correct location. If not, refer to the previous section.

To start the server, run the following command:
```
npm run astro dev
```
It should now be accessible in your browser by typing `localhost:4321` in the searchbar. Changes to the pages are automatically refresh them, and therefore changes should appear live.

## <a id="linux">Linux</a>

### Installing required programs

#### Fedora/RHEL

First update your system by running 
```
sudo dnf update
```

To download GitHub Desktop, add the RPM repository and the required GPG keys to your system by running

```
sudo rpm --import https://rpm.packages.shiftkey.dev/gpg.key
```
```
sudo sh -c 'echo -e "[shiftkey-packages]\nname=GitHub Desktop\nbaseurl=https://rpm.packages.shiftkey.dev/rpm/\nenabled=1\ngpgcheck=1\nrepo_gpgcheck=1\ngpgkey=https://rpm.packages.shiftkey.dev/gpg.key" > /etc/yum.repos.d/shiftkey-packages.repo'
```
, then install the package using `dnf`:
```
sudo dnf install github-desktop
```
 Once installed, login using the GitHub account with which you have collaborator access to the aeroref repository. Once logged in clone the aeroref repository.

Download NodeJS by running 
```
sudo dnf install nodejs
```
By default, the installer should also install Node Package Manager/NPM, but double check that is the case.

#### Ubuntu/Debian

To download GitHub Desktop, add the repository and the required GPG keys to your system by running

```
wget -qO - https://apt.packages.shiftkey.dev/gpg.key | gpg --dearmor | sudo tee /usr/share/keyrings/shiftkey-packages.gpg > /dev/null
sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/shiftkey-packages.gpg] https://apt.packages.shiftkey.dev/ubuntu/ any main" > /etc/apt/sources.list.d/shiftkey-packages.list'
```
, then update the system and install the package using `apt`:
```
sudo apt update && sudo apt install github-desktop
```
Once installed, login using the GitHub account with which you have collaborator access to the aeroref repository. Once logged in clone the aeroref repository.

Download NodeJS by running 
```
sudo apt install nodejs
``` 
Run 
```
sudo apt install npm
``` 
to also install Node Package Manager/NPM.

### Before running the pages for the first time

Open your terminal and go to the correct directory with 
```
cd ~/Documents/GitHub/aeroref
``` 
or 
```
cd $HOME/Documents/GitHub/aeroref
```
<u>Note</u>: this is the default location for the aeroref repository. If you changed the default location when installing GitHub desktop, these commands won't work. Instead, use the location you chose.

Install all dependencies by running 
```
npm install
```

<u>Optional</u>:
For easy access, consider creating a symbolic link in your home directory by running:
```
ln -s $HOME/Documents/GitHub/aeroref ./aeroref
```

Now, everytime you launch the terminal, you should be able to access the correct directory with 
```
cd aeroref
```

### Running the server

Make sure you are in the correct location. If not, refer to the previous section.

To start the server, run the following command:
```
npm run astro dev
```
It should now be accessible in your browser by typing `localhost:4321` in the searchbar. Changes to the pages are automatically refresh them, and therefore changes should appear live.

To stop the application, close the terminal window or run `Ctrl + C`.

## <a id="osx">MacOS</a>

### Installing required programs

Download <a href="https://github.com/apps/desktop">GitHub Desktop</a>. Once installed, login using the GitHub account with which you have collaborator access to the aeroref repository. Once logged in clone the aeroref repository.

Download <a href="https://nodejs.org/en/download/prebuilt-installer">NodeJS</a>. By default, the installer should also install Node Package Manager/NPM, but double check that is the case.

### Before running the pages for the first time

Open your terminal and go to the correct directory with 
```
cd ~/Documents/GitHub/aeroref
``` 
or 
```
cd $HOME/Documents/GitHub/aeroref
```
<u>Note</u>: this is the default location for the aeroref repository. If you changed the default location when installing GitHub desktop, these commands won't work. Instead, use the location you chose.

Install all dependencies by running 
```
npm install
```

<u>Optional</u>:
For easy access, consider creating a symbolic link in your home directory by running:
```
ln -s $HOME/Documents/GitHub/aeroref ./aeroref
```

Now, everytime you launch the terminal, you should be able to access the correct directory with 
```
cd aeroref
```

### Running the server

Make sure you are in the correct location. If not, refer to the previous section.

To start the server, run the following command:
```
npm run astro dev
```
It should now be accessible in your browser by typing `localhost:4321` in the searchbar. Changes to the pages are automatically refresh them, and therefore changes should appear live.

To stop the application, close the terminal window or run `Ctrl + C`.

# Manual for setting up DH Leipzig's VM 

Given all the different OS and software versions used by students and workshop participants, we decided to package some tools necessary to run our scripts, libraries, tools in a virtual machine and ship it in a Vagrant box, the `LeipzigDH.box`. This keeps OS specific helpdesking and troubleshooting to a minimum. All one has to do to get `LeipzigDH.box` is to install VirtualBox and Vagrant and initialise the box. Please find more information below. Due to the lack of a secure password / username, please do not save any sensitive information on your virtual machine. `LeipzigDH.box` is a learning environment and not a permament solution for virtualising your research. If you like to build a virtual machine that is similar to `LeipzigDH.box` but safer, we are happy to give some hints and advice.

## What is in the `LeipzigDH.box`?

#### OS

Ubuntu 12.04 LTS, 64bit, 1024 MB RAM (you can alter the RAM later in the vagrantfile)

#### Languages

- Python
  - Python, version 2.7.6
  - Python3, version 3.2.3
- Java 1.7 (also 1.6 and 1.8 use `sudo update-alternatives --config java` to switch between versions)
- R, version 3.2.2 “Fire Safety” / RStudio
- Ruby
  - Ruby 2.2.1p8
  - rubygems 2.4.8
  - Rails 4.2.5
  - RVM 1.26.11 W. Seguin
- Git, 1.7.9.5

#### Libraries, DBs, Software

- Ant
- ExistDB 2.2 (but also the jar for 3.0.RC1 in the downloads folder [caveat: ant-build the repos under Java 1.7, then for installing 3.0.RC1 switch to Java 1.8 (see above)]) (user: admin, pw: vagrant)
- Jekyll
- OpenRefine, 2.6.-beta.1
- NodeJS
- NPM
- Grunt
- Reveal.js
- Chrome / Firefox
- CTS Repositories v. 0.1
- QGIS 2.8
- Gephi 0.8.1 beta

#### To be added

- Passim
- OCRopus
- Kraken
- Nidaba
- libtesseract3
- tesseract-ocr-eng
- liblept
- liblept
- Phaidra

## How can I get the LeipzigDH.box?

You need to install VirtualBox and Vagrant. Then download and initialise `LeipzigDH.box`

### Download VirtualBox

Find VirtualBox here: [(https://www.virtualbox.org)]

### Download Vagrant

Find Vagrant here: [(https://www.vagrantup.com)]

### Download `LeipzigDH.box`

Download the `LeipzigDH.box` from here:

### Setting up `LeipzigDH.box`

1. Create a folder for `LeipzigDH.box` and move `LeipzigDH.box` there and switch to it
E.g. 
```
mkdir ~/somefolder/OPP/vagrant_boxes
cd ~/somefolder/OPP/vagrant_boxes
```
2. Move `LeipzigDH.box` to the new folder
3. Add `LeipzigDH.box` to Vagrant: `vagrant box add leipzigdh LeipzigDH.box`
4. Initialise the LeipzigDH.box: `vagrant init leipzigdh`
5. Start it for the first time:: `vagrant up`
6. Halt the LeipzigDH.box: `vagrant halt`
7. Modify vagrantfile so it starts with a GUI. Find and uncomment in the vagrantfile (open with an editor of your choice):
```
 config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024" # Uncomment this and change it to alter the RAM of your VM
end
```
8. Start again: `vagrant up` 
9. Enjoy all the pre-installed tools and libraries
10. If you want to delete your VM type `vagrant destroy`



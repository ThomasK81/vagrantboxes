# Manual for setting up Vagrant VMs 

## What is in the LeipzigDH.box?

#### OS

Ubuntu 12.04 LTS, 64bit, 1024 MB RAM (you can alter the RAM later in the vagrantfile)

#### Languages

1. Python, version 2.7.6
2. Python3, version 3.2.3
3. Java 1.7 (also 1.6 and 1.8 use “sudo update-alternatives --config java” to switch between versions)
4. R, version 3.2.2 “Fire Safety” / RStudio
5. Ruby 2.2.1p8 / rubygems 2.4.8 / Rails 4.2.5 / RVM 1.26.11 W. Seguin
6. Git, 1.7.9.5

#### Libraries, DBs, Software

1. Ant
2. ExistDB 2.2 (but also the jar for 3.0.RC1 in the downloads folder [caveat: ant-build the repos under Java 1.7, then for installing 3.0.RC1 switch to Java 1.8 (see above)]) (admin, vagrant)
3. Jekyll
4. OpenRefine, 2.6.-beta.1
5. NodeJS
6. NPM
7. Grunt
8. Reveal.js
9. Chrome / Firefox
10. CTS Repositories v. 0.1
11. QGIS 2.8
12. Gephi 0.8.1 beta

## How can I get the LeipzigDH.box?

### Download Virtual Box

### Download Vagrant

### Download the LeipzigDH.box

### Setting up the LeipzigDH.box

1. Create a folder for the LeipzigDH.box
2. Add the LeipzigDH.box to Vagrant
3. Initialise the LeipzigDH.box
4. Start it for the first time:
5. Halt the LeipzigDH.box
6. Modify vagrantfile
7. Start again:
8. Enjoy all the pre-installed tools and libraries



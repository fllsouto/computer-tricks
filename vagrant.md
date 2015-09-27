# Vagrant Tips, commands and references

## CLI commands  
    $vagrant init  

Creates a new Vagrantfile in the current folder  

    $vagrant up  
    
Creates a new boxes with the configurations setted on Vagrantfile or start a existent box if it's off  

    $vagrant reload  
    
Reloads last changes on Vagrantfile  

    $vagrant reload --provision  
    
Quick reload the machine, the flag states for vagrant run the provisioners  

    $vagrant destroy  
    
Destroy the box  

    $vagrant halt  
    
Shut off gracefully the running box  
  
    $vagrant -h  
    
Print the vagrant help, it's possible to specify a command and run with '-h' to describe what command does

## Vagrantfile important statements


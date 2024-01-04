# Virtual Machine vs Docker

## What is virtual machine

A virtual machine (VM) is a digital representation of a physical computer. It's a computer file that behaves like a real computer and can run in a window as a separate computing environment.


## How an OS is made up ?

                    Application layer

                            ^
                            |

                          Kernel

                            |
                            v

                          Hardware


Kernel is **core** of any OS. It interacts with ***hardware*** and ***software*** components

----------------------------------------------------------------------------------

Docker and VM are both virtualization tools now questions come 

## What parts of OS do they virtualize?

### Docker
**Docker virtaulizes application layer**

Docker contains OS application layer

services and apps installed on top of that layer(eg JRE)

It uses kernel of the host as it doesn't have its own kernel


### Virtual Machine

It has application layer as well as kernel, so it virtualizes complete OS


     Containerized Apps                            VM           VM

      App A      App B                            App A        App B          

           Docker                                Guest OS     Guest OS

           Host OS                                      Host OS

        Physical Machine                            Physical Machine


### What effects these differences has?

                      Docker                           VM

images        |  Couple of **MB**  VM images  |   couple of **GB**
containers    |  takes seconds to start  VM   |   takes minutes to start
compatibility |  only with Linux distros      |   with all OS


***Most containers are linux based and docker originally was built for Linux OS later docker made and update developed docker desktop for Windows and Mac which made it possible to run linux based containers on Windows and MacOS***

***Docker desktop uses a hypervisor layer with a lightweight linux distribution***


# OS-dev
Trying to make a new OS

keeping a workflow 
* followed [this](https://www.whoishostingthis.com/resources/os-development/)
* followed [this](http://www.brokenthorn.com/Resources/OSDevIndex.html)
* followed [this](http://www.brokenthorn.com/Resources/OSDev1.html)
* Install Bochs
  * followed [this](https://www.linux.com/news/getting-started-bochs/)
  * download tar file
  * run *./configure --enable-ne2000 --enable-cdrom --enable-x86-64*
  * run *make*
  * facing **uintptr_t** error
    * open the corresponding file and replace *uintptr_t* by *intptr_t*
  * facing **X11** errors, google to find solutions
  * run *sudo make install*
  * run *bximage*
  * edit *.bochsrc* as in the blog
  * run *bochs* to verify
  * download *freeDOS* 
  * edit script as given in blog
  * facing **Bochs is not compiled with lowlevel sound support** error
    * comment the line created this issue in *.bochsrc*
  * run *bochs*
  * follow this, updated since blog was written
    * press 3
    * press 12* 
    * press 15
    * press 1
    * type *cdrom*
    * go to main menu
    * run simulation, press 6
    * follow installation instructions in the emulator window

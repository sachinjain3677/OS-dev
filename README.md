# OS-dev
Trying to make a new OS

Keeping a workflow 
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
 
 **Chapter 3** [link](http://www.brokenthorn.com/Resources/OSDev3.html)
 * write the *Boot1.asm* file as in the tutorial
 * assemble using *nasm* to *Boot1.bin* as it is
 * Instead of following *VFD* and *PartCopy*, follow [this](https://stackoverflow.com/questions/32893607/how-do-i-write-a-bin-file-512-bytes-to-the-first-sector-sector-0-of-a-floppy)
  * it uses *dd* to make a virtual floppy image of 1.44MB and writes *Boot1.bin* in the first sector 
 * follow [this](https://www.cs.princeton.edu/courses/archive/fall06/cos318/precepts/bochs_tutorial.html)
  * setup configurations for *bochs* and save in file called *custom_config*
 * run *bochs*, should see *booting from floppy...*
 * follow *Locating the BIOS ROM* under *Bochs: Testing the bootloader* on the original tutorial if facing error *Bios must end at 0xFFFFF*
 
 **Chapter 4** [link](http://www.brokenthorn.com/Resources/OSDev4.html)
 * Segment:offset addressing
 * Processor modes
  * Real mode
  * PMode
  * Unreal mode
  * Virtual 8086 mode
 * Descriptor tables
 * Routines and interrupts
  * OEM parameter table
  * printing text (char + string)
  * Get RAM 

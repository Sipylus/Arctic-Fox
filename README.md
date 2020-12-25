# Arctic Fox
*A*nother *R*eworked *C*omputer *T*hat *I*ncorporates *C*oding *F*rom *O*S *Xcode*

## Table of Contents

* [The Build](#the-build)
* [Prepare Install Media](#prepare-install-media)
* [Install the Bootloader](#install-the-bootloader)
* [Kernel Extensions](#kernel-extensions)
* [Releases](#releases)
* [License](#license)


## The Build

View the complete [build](https://www.dualbootpc.com/systems/desktop/arctic-fox/specs/) on GixxerPC: http://gixxer.us/2Jslljx

## Prepare Install Media

1. Download the [macOS Sierra installer](https://www.dualbootpc.com/software/system/macos/sierra/) (v10.12.6) from the Mac App Store.
2. Open Terminal and format the target 32GB [USB drive](https://www.dualbootpc.com/hardware/usb/) as with the following command:

    `diskutil partitionDisk /dev/{YOUR_DISK_ID} GPT JHFS+ "GixxerUSB" 100%`
    
3. [Create the bootable macOS installer](https://www.dualbootpc.com/guide/creating-a-usb-installer/): 

    `sudo /Applications/Install\ macOS\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/GixxerUSB /Applications/Install\ macOS\ Sierra.app`

4. Once the program finishes, your [USB drive](https://www.dualbootpc.com/hardware/usb/) should now be called the following:

    `Install macOS Sierra`
    
## Install the Bootloader

Configure Clover

* Download the included installer from [Release v0.1.0](https://github.com/Sipylus/Arctic-Fox/releases/tag/0.1.0)
* Install Clover to the USB device and customize with the following options:
  * Clover for UEFI booting only
  * Install Clover in the ESP
  * UEFI Drivers
    * Recommended drivers
      * ApfsDriverLoader
      * HFSPlus
    * Memory fix drivers
      * OsxAptioFix3Drv
      
## Kernel Extensions

* Mandatory from [Release v.0.1.0](https://github.com/Sipylus/Arctic-Fox/releases/tag/0.1.0)
  * FakeSMC.kext
  * Lili.kext
  * WhateverGreen.kext

* Post Installation from [Release v.1.1.0](https://github.com/Sipylus/Arctic-Fox/releases/tag/1.1.0)
  * AppleALC.kext
  * IntelMausiEthernet.kext
  * USBInjectAll.kext
  * XHCI-200-series-injector.kext

View the list of [kexts](https://www.dualbootpc.com/software/kexts/) available on GixxerPC: http://gixxer.us/3aS5d6m
  
## Releases

See the latest [releases](https://github.com/Sipylus/Arctic-Fox/releases/tag/1.1.0) for the project.
  
## License
  
See the posted [MIT License](https://github.com/Sipylus/Arctic-Fox/blob/main/LICENSE).
  
## Warranty
  
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR<br>
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,<br>
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE<br>
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER<br>
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,<br>
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE<br>
SOFTWARE.

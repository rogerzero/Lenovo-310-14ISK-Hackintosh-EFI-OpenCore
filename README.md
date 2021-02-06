# Lenovo-310-14ISK-Hackintosh-EFI-OpenCore

Don't try this EFI in different lenovo model !!! (Only Lenovo Ideapad 310 14ISK) Do With Your Own Risk !!!

Not recommended for older bios versions (you have to upgrade bios or make your own DSDT with SSDTTime)

If you've got same Laptop model and already upgraded to lastest bios you can just simply use the EFI folder posted above. 

Sorry for my bad english :)

============================================================================

### Lenovo-310-14ISK 

| Laptop Type | Bios Version | Installed macOS | Bootloader |
| ----------- | ----------- | ----------- | ----------- | 
| Lenovo Ideapad 310 14ISK 80SL | LENOVO Insyde 0XCN45WW (Lastest)| Bigsur v11.2 (20D64) | [OpenCore v0.6.6](https://github.com/acidanthera/OpenCorePkg/releases) |

### My Specifications :

| Type | Spec | Status |
| ----------- | ----------- | ----------- |
| Processor | Intel Core i5 6200U Skylake | Working |
| RAM | 4GB DDR4 Onboard + Samsung 4GB DDR4 SODIMM slot (2133 Mhz) | Working |
| IGPU | Intel HD Graphics 520 | Working |
| dGPU | Nvidia GT 920MX | Not Supported Optimus Mode |
| Storage | 1x WD Blue 1TB + 1x Visipro SSD SATA 120GB | Working |
| Wifi | Intel AC 3165 + Bluetooth | Working |
| Ethernet | Realtek RTL8168GU Gigabit Ethernet | Working |
| Touchpad | Synaptic SYN2B58 PS2 Interface | Working |

### System Status :

| Type | Status |
| ----------- | ----------- |
| QE/CI Graphics Intel HD 520 | Working |
| CPU PM | Working |
| Restart and Shutdown | Working |
| Sleep | Not Working |
| Brightness Slider & keys F11 - F12 | Working |
| Battery Precentage | Working |
| Touchpad and gesture | Working |
| SD Card Reader | Untested |
| HDMI Display | Working |
| HDMI  Audio | Working |
| iService | Not Working |

### Used Kext :

| Kext | Info |
| ----------- | ----------- |
| [Lilu.kext](https://github.com/acidanthera/Lilu/releases) | Kernel extension Arbitrary kext and process patching on macOS |
| [WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen/releases) | To disable Nvidia discrete GPU and patch framebuffer Intel HD 520 |
| [AppleALC.kext](https://github.com/acidanthera/AppleALC/releases) | To patch on-board sound controllers|
| [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases) | SMC Emulator Layer |
| [SMCProcessor.kext](https://github.com/acidanthera/VirtualSMC/releases) | VirtualSMC Plugin for Processor Monitoring |
| [SMCSuperIO.kext](https://github.com/acidanthera/VirtualSMC/releases) | VirtualSMC Plugin for Fan Speed Monitoring |
| [SMCBatteryManager.kext](https://github.com/acidanthera/VirtualSMC/releases) | VirtualSMC Plugin for Battery Monitoring |
| [VoodooPS2Controller.kext](https://github.com/RehabMan/OS-X-Voodoo-PS2-Controller/releases) | To Patch Synaptics ps/2 Touchpad & Keyboard |
| [AirportItlwm.kext](https://github.com/OpenIntelWireless/itlwm/releases) | To patch Intel AC 3165 |
| [IntelBluetoothFirmware.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | To patch Intel Bluetooth |
| [HWPEnabler.kext](https://github.com/goodwin/HWPEnable) | Intel Skylake CPU select its own stepping speed without the usage of the CPU Multiplier |
| [VoodooTSCSync.kext](https://bitbucket.org/RehabMan/VoodooTSCSync/downloads) | A kernel extension which will synchronize the TSC on any Intel CPUs |
| [RealtekRTL8111.kext](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases) | To patch The Ethernet |

After you download it, copy and paste/replace all the kext to the EFI folder in EFI-> OC-> Kext)

### Used DSDT & SSDT :

If you've got same Laptop model and already upgraded to lastest bios you can just simply use the DSDT & SSDT Files above. 

| DSDT / SSDT | Info | Guide |
| ----------- | ----------- | ----------- |
| [DSDT.aml](/EFI/OC/ACPI/DSDT.aml) | Differentiated System Description Table which contains the Differentiated Definition Block that supplies the implementation and configuration information about the base system | [Read](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-easy.html#running-ssdttime) |
| [SSDT-EC.aml](/EFI/OC/ACPI/SSDT-EC.aml) | Fix Embedded Controller for hotkeys and battery | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Universal/ec-fix.html) |
| [SSDT-HPET.aml](/EFI/OC/ACPI/SSDT-HPET.aml)  | Patch IRQ Conflicts | [Read](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-easy.html#running-ssdttime) |
| [SSDT-PLUG.aml](/EFI/OC/ACPI/SSDT-PLUG.aml) | Fix Intel Skylake Processor Plugin Type | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Universal/plug.html) |
| [SSDT-PNLF.aml](/EFI/OC/ACPI/SSDT-PNLF.aml)| Fix Backlight Slider | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/backlight.html) |
| [SSDT-SBUS-MCHC.aml](/EFI/OC/ACPI/SSDT-SBUS-MCHC.aml) | Fix Intel System Management Bus | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Universal/smbus.html) |
| [SSDT-dGPU-Off.aml](/EFI/OC/ACPI/SSDT-dGPU-Off.aml) | Disable Nvidia Optimus Discrete GPU | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/laptop-disable.html#optimus-method) |
| [SSDT-UIAC.aml](/EFI/OC/ACPI/SSDT-UIAC.aml)| Blocked Unused Usb Port | - |
| [SSDT-USBX.aml](/EFI/OC/ACPI/SSDT-USBX.aml) | Fix Usb Port Mapping | - |

After you download it, copy and paste/replace all the DSDT/SSDT to the EFI folder in EFI-> OC-> ACPI)

### Patching Battery on DSDT :

#### FIX 16 BIT REGISTERS :

| 16 Bit Registers | 
| ----------- |
| B1SN,   16, |
| B1DV,   16, | 
| B1DC,   16, | 
| B1FC,   16, | 

Apply patch on DSDT with MaciAsl :
```
into device label EC0 code_regex B1SN,\s+16, replace_matched begin BSN0,8,BSN1,8, end;
into device label EC0 code_regex B1DV,\s+16, replace_matched begin BDV0,8,BDV1,8, end;
into device label EC0 code_regex B1DC,\s+16, replace_matched begin BDC0,8,BDC1,8, end;
into device label EC0 code_regex B1FC,\s+16, replace_matched begin BFC0,8,BFC1,8, end;
```

then apply this :
```
into method label B1B2 remove_entry;
into definitionblock code_regex . insert
begin
Method (B1B2, 2, NotSerialized) { Return(Or(Arg0, ShiftLeft(Arg1, 8))) }\n
end;
```

then apply this B1B2 method :
```
B1B2(\_SB.PCI0.LPCB.EC0.BDC0,\_SB.PCI0.LPCB.EC0.BDC1)
B1B2(\_SB.PCI0.LPCB.EC0.BFC0,\_SB.PCI0.LPCB.EC0.BFC1)
B1B2(\_SB.PCI0.LPCB.EC0.BDV0,\_SB.PCI0.LPCB.EC0.BDV1)
B1B2(\_SB.PCI0.LPCB.EC0.BSN0,\_SB.PCI0.LPCB.EC0.BSN1)
```

#### FIX LARGER than 32 BIT REGISTERS  :

| LARGER than 32 BIT Registers| 
| ----------- |
| FWBT,   64, |
| SMDA,   256, | 
| BMN0,   72, | 
| BDN0,   64, | 

Apply patch on DSDT with MaciAsl :
```
into device label EC0 code_regex (FWBT,)\s+(64) replace_matched begin FWBX,%2,//%1%2 end;
into device label EC0 code_regex (SMDA,)\s+(256) replace_matched begin SMDX,%2,//%1%2 end;
into device label EC0 code_regex (BMN0,)\s+(72) replace_matched begin BMNX,%2,//%1%2 end;
into device label EC0 code_regex (BDN0,)\s+(64) replace_matched begin BDNX,%2,//%1%2 end;
```

then apply this :
```
FWBT -  \_SB.PCI0.LPCB.EC0.RECB(0X14,64)
SMDA -  \_SB.PCI0.LPCB.EC0.RECB(0X64,256)
BMN0 -  \_SB.PCI0.LPCB.EC0.RECB(0X8F,72)
BDN0 -  \_SB.PCI0.LPCB.EC0.RECB(0X98,64)
```

then apply this Standart B1B2 method for Larger than 32 BIT Registers :
```
into method label B1B2 remove_entry;
into definitionblock code_regex . insert
begin
Method (\B1B2, 2, NotSerialized)\n
{\n
ShiftLeft (Arg1, 8, Local0)\n
Or (Arg0, Local0, Local0)\n
Return (Local0)\n
}\n
end;

#Standard utility methods to read/write buffers from/to EC

into device label EC0 insert
begin
Method (RE1B, 1, NotSerialized)\n
{\n
OperationRegion(ERAM, EmbeddedControl, Arg0, 1)\n
Field(ERAM, ByteAcc, NoLock, Preserve) { BYTE, 8 }\n
Return(BYTE)\n
}\n
Method (RECB, 2, Serialized)\n
{\n
ShiftRight(Arg1, 3, Arg1)\n
Name(TEMP, Buffer(Arg1) { })\n
Add(Arg0, Arg1, Arg1)\n
Store(0, Local0)\n
While (LLess(Arg0, Arg1))\n
{
	Store(RE1B(Arg0), Index(TEMP, Local0))\n
	Increment(Arg0)\n
	Increment(Local0)\n
}\n
Return(TEMP)\n
}\n
end;

into device label EC0 insert
begin
Method (WE1B, 2, NotSerialized)\n
{\n
   OperationRegion(ERAM, EmbeddedControl, Arg0, 1)\n
   Field(ERAM, ByteAcc, NoLock, Preserve) { BYTE, 8 }\n
   Store(Arg1, BYTE)\n
}\n
Method (WECB, 3, Serialized)\n
{\n
   ShiftRight(Arg1, 3, Arg1)\n
   Name(TEMP, Buffer(Arg1) { })\n
   Store(Arg2, TEMP)\n
   Add(Arg0, Arg1, Arg1)\n
   Store(0, Local0)\n
   While (LLess(Arg0, Arg1))\n
   {\n
       WE1B(Arg0, DerefOf(Index(TEMP, Local0)))\n
       Increment(Arg0)\n
       Increment(Local0)\n
   }\n
}\n
end;
```

### Installer MacOs, and Supporting App :

| Apps/Tools | Info | Link | Guide |
| ----------- | ----------- | ----------- | ----------- |
| gibMacOS | get the installer | [Download](https://github.com/corpnewt/gibMacOS) | - |
| GenSMBIOS | To Generate a new Serial | [Download](https://github.com/corpnewt/gibMacOS) | [Read](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#generate-a-new-serial) |
| ProperTree |  To configure OpenCore config.plist | [Download](https://github.com/corpnewt/ProperTree) | - |
| OpenCore Configurator | To configure OpenCore config.plist | [Download](https://mackie100projects.altervista.org/opencore-configurator/) | - |
| SSDTTime | To get the DSDT and SSDT | [Download](https://github.com/corpnewt/SSDTTime) | [Read](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-easy.html#running-ssdttime) |
| DPCIManager | To see the device properties in macOS | [Download](https://github.com/MuntashirAkon/DPCIManager/releases) | - |
| Hackintool | To see the device properties in macOS | [Download](https://github.com/headkaze/Hackintool/releases) | - |
| IntelPowerGadget | To see CPU Power Management and Performance test | [Download](https://software.intel.com/content/www/us/en/develop/articles/intel-power-gadget.html#attachment-heading) | - |


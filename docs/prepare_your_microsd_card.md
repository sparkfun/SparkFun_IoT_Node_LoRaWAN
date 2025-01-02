Not all microSD cards are created equal. The [capacity, read/write speed, and format](https://learn.sparkfun.com/tutorials/sd-cards-and-writing-images) vary depending on the manufacturer. In order to log data to the microSD card, you will need to ensure that your memory card is formatted as **FAT32**. You can also use FAT16. If the memory card is formatted as a different memory card, the DataLogger IoT will not be able to recognize the microSD card.



## Checking MicroSD Card Format

While you can simply insert the microSD card into your SparkFun IoT Node for LoRaWAN® and start logging, there may be a chance that the it will not recognize the memory card due to the format.



### Checking MicroSD Card Format - Windows

To check to see if it is the correct format on a Windows you could head to the drive, right click, and select **Properties**.

<figure markdown>
[![microSD Card Properties](assets/img/microSD_Card_Properties.jpg){ width="75%" }](assets/img/microSD_Card_Properties.jpg "Click to enlarge")
<figcaption markdown>microSD Card Properties</figcaption>
</figure>



Once the properties are open, you should be able to tell what file system that the memory card uses. In this case, it was exFAT which is not compatible with the DataLogger IoT. You will need to reformat the memory card since it is not formatted as FAT32.

<figure markdown>
[![Check File System Windows](assets/img/microSD_Card_Check_File_System_exFAT.jpg){ width="75%" }](assets/img/microSD_Card_Check_File_System_exFAT.jpg "Click to enlarge")
<figcaption markdown>Check File System Windows</figcaption>
</figure>



### Checking MicroSD Card Format - macOS

To check to see if it is the correct format on a macOS, you could head to the drive on your desktop. Then right click, and select **Get Info**.

<figure markdown>
[![Get Info on MicroSD Card](assets/img/mac_get_info.png){ width="75%" }](assets/img/mac_get_info.png "Click to enlarge")
<figcaption markdown>Get Info on MicroSD Card</figcaption>
</figure>


A window will pop up indicating the microSD card properties. Under **General:** > **Format:**, you should be able to tell what file system that the memory card uses. In this case, it was exFAT which is not compatible with the DataLogger IoT. You will need to reformat the memory card since it is not formatted as FAT32.


<figure markdown>
[![exFAT](assets/img/mac_microSD_exFat.png){ width="75%" }](assets/img/mac_microSD_exFat.png "Click to enlarge")
<figcaption markdown>exFAT</figcaption>
</figure>



## Download Raspberry Pi Imager

There are a few methods and programs available to reformat your microSD card as a FAT32. We found it easier to use the [Raspberry Pi Imager Tool](https://www.raspberrypi.com/software/). Of course, you will only be using the tool to erase the contents of the microSD card and formatting it as a FAT32 system. You will not actually flash any image to the memory card. Click on the button below to download the tool from the Raspberry Pi Foundation. It is supported on *Windows*, *macOS*, and *Ubuntu for x86*.

<div style="text-align: center"><a href="https://www.raspberrypi.com/software/" target="rpi_imager_tool" class="md-button">Raspberry Pi Imager Tool</a></div>



## Formatting as FAT32 using the Raspberry Pi Imager

After downloading and installing the software, open the Raspberry Pi Imager.

<figure markdown>
[![Raspberry Pi Imager](assets/img/Raspberry_Pi_Imager.jpg){ width="75%" }](assets/img/Raspberry_Pi_Imager.jpg "Click to enlarge")
<figcaption markdown>Raspberry Pi Imager</figcaption>
</figure>



Under "**Operating System**", select "**Erase**" to "format card as FAT32."

<figure markdown>
[![Raspberry Pi Imager - Erase : Format as FAT32](assets/img/Raspberry_Pi_Imager_Erase_Format.jpg){ width="75%" }](assets/img/Raspberry_Pi_Imager_Erase_Format.jpg "Click to enlarge")
<figcaption markdown>Raspberry Pi Imager - Erase : Format as FAT32</figcaption>
</figure>


Under "**Storage**", select the drive that the microSD card appeared as on your computer.

<figure markdown>
[![Raspberry Pi Imager - Select Storage Drive](assets/img/Raspberry_Pi_Imager_Select_Drive.jpg){ width="75%" }](assets/img/Raspberry_Pi_Imager_Select_Drive.jpg "Click to enlarge")
<figcaption markdown>Raspberry Pi Imager - Select Storage Drive</figcaption>
</figure>




When ready, select "**Write**". After a few minutes, the microSD card should be formatted with FAT32.

<figure markdown>
[![Raspberry Pi Imager - Write](assets/img/Raspberry_Pi_Imager_Write.jpg){ width="75%" }](assets/img/Raspberry_Pi_Imager_Write.jpg "Click to enlarge")
<figcaption markdown>Raspberry Pi Imager - Write</figcaption>
</figure>



Once the memory card has finished formatting, eject the microSD from your computer. To check to see if the microSD card is formatted as FAT32, you can check its properties as explained earlier with your operating system. Below shows a screenshot from a Windows and macOS showing that the microSD card reformatted as a FAT32 file system.


<figure markdown>
[![Check File System Windows](assets/img/microSD_Card_Check_File_System_FAT32.JPG){ width="75%" }](assets/img/microSD_Card_Check_File_System_FAT32.JPG "Click to enlarge")
<figcaption markdown>Check File System Windows</figcaption>
</figure>

<figure markdown>
[![Check File System macOS](assets/img/mac_microSD_FAT32.png){ width="75%" }](assets/img/mac_microSD_FAT32.png "Click to enlarge")
<figcaption markdown>Check File System macOS</figcaption>
</figure>



<!--
<table class="table table-hover table-striped table-bordered">
  <tr style="vertical-align:middle;">
   <td style="text-align: center; vertical-align: middle;"><a href="https://github.com/sparkfun/SparkFun_DataLogger/blob/main/docs/assets/img/microSD_Card_Check_File_System_FAT32.jpg"><img src="https://github.com/sparkfun/SparkFun_DataLogger/blob/main/docs/assets/img/microSD_Card_Check_File_System_FAT32.jpg" alt="Check File System Windows"></a></td>
   <td style="text-align: center; vertical-align: middle;"><a href="https://github.com/sparkfun/SparkFun_DataLogger/blob/main/docs/assets/img/mac_microSD_FAT32.png"><img src="https://github.com/sparkfun/SparkFun_DataLogger/blob/main/docs/assets/img/mac_microSD_FAT32.png" alt="Check File System macOS"></a></td>
  </tr>
  <tr style="vertical-align:middle;">
  <td style="text-align: center; vertical-align: middle;"><i>Check File System Windows</i></td>
  <td style="text-align: center; vertical-align: middle;"><i>Check File System macOS</i></td>
  </tr>
</table>
-->
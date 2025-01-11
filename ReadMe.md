# OIV Package Tool Documentation - Version: V1 Test Version By SmallBlack

## Overview:
This is a visual application for creating OIV packages based on the OpenIV Package format – Version 2.2 specification. The application allows you to create OIV files for use or distribution.

## Current Features:
- **V1.1** - Supports adding/replacing files within game files.
- **V1.2** - Supports adding text data to XML files within game files.

## Instructions for Use:

### OIV Basic Information Interface
- **Author Link/Author Homepage**: Clicking on the author's name will redirect the user to a webpage (e.g., https://www.lcpdfr.com/profile/451800-smallblack/).

### OIV Appearance Design Interface
- **Select Icon**: Only supports image files with a size of 128*128. If the size does not meet the specification, the OIV package icon display will have issues.

### OIV Installation Content Management Interface
- **Add File**: Select the file you need to create an OIV installation for.
- **Configure Installation Path**: Click on the file you need to configure (e.g., smallblack.jpg), then click the "Configure Installation Path" button or double-click the file.

  For example, if you need to install the smallblack.jpg file into the game directory at `update\update.rpf\common\data\levels\gta5`, enter `update\update.rpf` in the "RPF File Path" (ensure the path ends with rpf, otherwise it does not meet the specification), and enter `common\data\levels\gta5\smallblack.jpg` in the "File Installation Path" (omit the path you filled in the "RPF File Path" and write the remaining path in the "File Installation Path", the end must be the file name you want to install), click OK to complete the path configuration.

  At this point, smallblack.jpg has been set to install into `update\update.rpf` in `common\data\levels\gta5`. The configuration path operation for other files is the same.

  **Note**: Since the program is intended to support GTA5 only, the RPF type does not need to be modified, select RPF7.

- **Add Text Content**: Add text data to XML files within game files.
  
  For example, if you need to add data to `update/update.rpf/common/data/dlclist.xml`:
  ```xml
  <Item>platform:/dlcPacks/lspdfrcn/</Item>
  <Item>platform:/dlcPacks/smallblack/</Item>
  ```
  Enter `update/update.rpf` in the "RPF File Path" (ensure the path ends with rpf, otherwise it does not meet the specification); then enter `common/data/dlclist.xml` in the file path (omit the path you filled in the "RPF File Path" and write the remaining path in the "File Installation Path", the end must be the file name you want to add text data to); the "Xpath" needs to be filled in according to the format in the XML file, for example, the internal format of dlclist.xml is as follows:

  Fill in `/SMandatoryPacksData/Paths` in "Xpath" according to the file format. The addition type is as follows:

  **Note**: Generally, choose First or Last, Before and After are generally not needed. Enter the content in the box (supports one line of data or multiple lines of data, one per line):
  ```xml
  <Item>platform:/dlcPacks/lspdfrcn/</Item>
  <Item>platform:/dlcPacks/smallblack/</Item>
  ```
  After configuration, click OK to complete adding text data to the XML file.

  If you need to modify the file path or data you configured, you can double-click an item in the list to modify it.

## Completion:
Once you have configured the contents and files of the OIV package, click "Create OIV Package" to complete the creation.

## Others:
The program supports multilingual translation. If you need to translate into other languages, please translate in `language.xml`.

Reference Specification Document: https://github.com/OpenIV-Team/OpenIV-PackageFormat/blob/master/specification/versions/2.2.md.

**Disclaimer**: This program is a test version and only provides the function of creating OIV packages. If the OIV package created by this program causes game damage, you are responsible for it! 
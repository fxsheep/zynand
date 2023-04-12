# ZYNand
ZYNand(Zero Yield NAND) is a project aims at reusing old or broken storage devices based on NAND flash, such as SSDs, USB flash drives, SD and microSD cards, eMMCs.

This project consists of 2 aspects:
- Reusing the flash controller
- Reusing the internal NAND flash

## Why
NAND flash based stroage device has been around for quite a while. Today, they are ubiquitous and can be dirt cheap. As a result, it's not uncommon to have one or more of them broken and replaced. Meanwhile, technology develops fast. You suddenly find out the old 4GB flash drive no longer fit in a single video record.  

So what could be done with these old or broken stuffs? Just throwing them away might make you feel reluctant. Electronic hobbyists who are good at soldering have tried to reuse them by taking the NAND chip out and give it a second life with another board. However, this is not the end. There are some boundaries most of us haven't pushed yet:

### Monolithic devices
Things have changed a bit nowadays, as more storage devices switching to monolithic packaging - there's no separate, standard(TSSOP, LGA) packaged NAND flash, instead they are packaged together with the controller. With some efforts, the internal NAND pinout can be found, making it reusable again. 

### Flash controllers
While it might not be obvious, the flash controller can actually be a gold mine. They **are microcontrollers**. The CPU itself might not be attractive: most of them being 8051-based, with some recent ones being 32bit-based. However, they can have a blazing fast host interface and NAND flash interface. It's almost at least USB 2.0 HighSpeed or SATA 3Gb/s with integrated PHY - hardly seen in 'cheap' off the shelf MCUs, but they are right in your pocket, in spare computer parts, and even (about to be) in trashcans! The bad news is that they are almost zero-documented, but the good news is that there is no secret for a determined reverse engineer. And, depending on your needs, gaining the knowledge required can be quite easy.


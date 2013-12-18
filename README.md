ORPSOC
======

## What's This?
ORPSoC is acronym of OpenRISC Reference Platform System-on-Chip.
It is intended to be a development and verification environment for IP cores and SoC designs. 
This is not a repository including OpenRISC design itself but this can configure it,
simulate it, and build it.

## Workflow

1. Download the OpenRISC core and me.
2. Configure ORPSoC.
3. If some cores are not provided by orpsoc-cores, write a core description file (CAPI).
4. Write an ORPSoC system description file (SAPI). This file configures general attributes for the system (name, description) but also how the system must be synthesized.
5. Write a board core description file. This core file configures the board dependencies (which IP are needed to build the system). It also indicates to ORPSoC what are the local verilog files (files which are not included in dependencies). Last but not least, it sets simulation configuration.
6. Generate the system interconnection.
7. Write the system top file.
8. Add board synthesis constraint (sdc file, pinout, synthsis options,...).
9. Build and program the system.

## Preparation and Install

Before the installation, you should install softwares to run the simulation,
and vendor-dependent synthesis tools if you need. It is proprietary tool and 
sometime you have to pay for it. I don't describe how to install it, but you can refer many documents.

### Arch Linux

```bash
$ sudo pacman -S iverilog python
$ git clone git@github.com:openrisc/orpsoc-cores.git
$ git clone git@github.com:openrisc/orpsoc.git
$ cd orpsoc
$ ./configure && make
$ sudo make install
```

Then you have to get synthesis platform like Xilinx vivado or ISE, or Altera QuartusII.
You can refer the how-to on ArchWiki.
See:
- [Xilinx ISE WebPACK](https://wiki.archlinux.org/index.php/Xilinx_ISE_WebPACK)
- [Altera Design Software](https://wiki.archlinux.org/index.php/Altera_Design_Software)

### Debian GNU/Linux

```bash
$ sudo apt-get install iverilog python3
$ git clone git@github.com:openrisc/orpsoc-cores.git
$ git clone git@github.com:openrisc/orpsoc.git
$ cd orpsoc
$ ./configure && make
$ sudo make install
```

Then you have to get synthesis platform like Xilinx vivado or ISE, or Altera QuartusII.

## Configuration
wip

## How to simulate OpenRISC?

Simulation is first process to examine whether HDL design is correct or not.


## How to build and run on FPGA?

### Preparation

### Synthesis

### Append an excutable

## How to run a first program on it?

## OpenRISC Project web site

OpenRISC has two web site.
- [http://opencores.org/or1k](http://opencores.org/or1k)
- [http://openrisc.net](http://openrisc.net)

And also, there are more sites for OpenRISC users.

- wiki: [OR1K:Community portal](http://opencores.org/or1k/OR1K:Community_portal)
- Mailing lists: [lists.opencores.org Mailing Lists](http://lists.opencores.org/)
- forum: [OpenCores](http://opencores.org/forum,OpenRISC)
- git: [openrisc](https://github.com/openrisc)
- IRC log: [IRC logs for #openrisc on irc.freenode.net](http://juliusbaxter.net/openrisc-irc/)
- Old release of OpenRISC(v2): [subversion repositories](http://opencores.org/websvn,listing,openrisc)
- Specification is here: [OpenRISC 1200 IP Core Specification (Preliminary Draft)](http://openrisc.net/or1200-spec.html)

## Hacks


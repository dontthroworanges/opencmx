# openCMX

## The openCMX Standard

openCMX is a proposed Open Source, standardized, modular for factor and I/O specification for small, scalable, general computing devices.

**Goals**

The goal of openCMX is to establish an Open Sourced standard PCB and connector design for small low powered devices that allows an individual to use cost effective USB-C adapters to fully operate the node. In addition to this scenario, the user may also use the same module(s) along with 3rd party designed backplanes, to scale the single node to high density clusters. No extra cables, network switches, or power supplies. 

Some examples of openCMX usaage:

- Home hobbyist
- Embedded Media Applications
- Commercial Thin Clients and low powered desktops
- Industrial embedded applications
- Robotics Development
- Education and Developing Counties
- Homelab Certification
- Large cluster development and testing

**Basics**

- The form factor is built upon the 15mm 2.5" U.2 storage physical specifications. This form factor is well established with OEMs and makes use of existing accessories and tooling. 
- Primary I/O is dependent on reuse of the U.2 SFF-8639 connector to carry a PCIe x4 connection as well as a USB 3.1 connection for power, peripherals, and display output. The use of this edge connector allows for scalability within high density rack enclosures as well as smaller clusters without the need for external power supplies, network switches, etc. 
- In conjunction with the SFF-8639 connection, a second USB 3.1 port (USB-C) is used for use with commodity USB-C Hubs. 
- openCMX modules can be used either as a bare PCB with user customized SoC cooling etc. The module can also reside within an aluminum enclosure doubling as a heatsink. This adds durability and essential heat transfer when in higher density clusters. 

**Compliant I/O**

Each openCMX module must include:

- 1x SFF-8639 with PCIe x4 and USB 3.1 (Mid-Mount)
- 1x USB-C 3.1
- 1x USB-A 3.0 (Mid-Mount)
- 1x mSDXC
- 1x FFC 40pin GPIO

**Physical Requirements**

Each openCMX compliant module must conform to the following physical specifications:

- PCB must fit within an enclosure that conforms to the specifications of a 2.5” u.2 SSD. See “U.2 Mechanical Spec.pdf” for rough external measurements.

- Total Z height of pcb, plus components should not exceed 13mm (to account for enclosure)

 - Components which generate above 50% of the total heat output of the complete module should be located on the “Thick” side of the PCB. Will be known as “Side A.” SOC, Memory, Etc… Enclosure acts as a heatsink for these components when in high density rack environments.

- Components on the Thin Side, otherwise known as “Side B” cannot exceed the height of the SFF-8639 connector as it protrudes from the PCB. 

![opencmx](https://github.com/dontthroworanges/opencmx/blob/main/openCMX%20Side%20A-1034x864.png)

![opencmx](https://github.com/dontthroworanges/opencmx/blob/main/openCMX%20Side%20B-1034x864.png)

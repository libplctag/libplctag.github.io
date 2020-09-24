# libplctag

- [libplctag](#libplctag)
  - [PLC Communications](#plc-communications)
  - [WARNING - DISCLAIMER](#warning---disclaimer)
  - [Features](#features)
    - [High Level Features](#high-level-features)
    - [Detailed Features](#detailed-features)
      - [PLC Support](#plc-support)
  - [Components](#components)
  - [Contact and Support](#contact-and-support)
    - [libplctag Forum](#libplctag-forum)
    - [GitHub](#github)

## PLC Communications

This set of open source C library for Linux, Android, Windows and macOS uses **EtherNet/IP** or **Modbus TCP** to read and write tags in PLCs.  The library has been in production since early 2012 and is used by multiple organizations for many tasks including controlling radio telescopes, large and precision manufacturing, controlling fitness equipment, food handling and many, many more.

## WARNING - DISCLAIMER

Note: **PLCs control many kinds of equipment and loss of property, production or even life can happen if mistakes in programming or access are made.  Always use caution when accessing or programming PLCs!**

We make no claims or warrants about the suitability of this code for
any purpose.

Be careful!

## Features

### High Level Features

- EtherNet/IP and Modbus TCP support.
- Open source licensing.
- Cross platform support.
- Very stable API with almost no changes other than feature additions since 2012.
- Low memory use and very high performance and capacity.  Uses protocol-specific features to increase performance.
- Wrappers for higher level languages like C#/.Net, Julia etc.
- Free!

### Detailed Features

#### PLC Support

- support for Rockwell/Allen-Bradley ControlLogix(tm) PLCs via CIP-EtherNet/IP (CIP/EIP or EIP).
  - read/write 8, 16, 32, and 64-bit signed and unsigned integers.
  - read/write single bits/booleans.
  - read/write 32-bit and 64-bit IEEE format (little endian) floating point.
  - raw support for user-defined structures (you need to pull out the data piece by piece)
  - read/write arrays of the above.
  - multiple-request support per packet.
  - packet size negotiation with newer firmware (version 20+) and hardware.
  - tag listing, both controller and program tags.
- support for Rockwell/Allen-Bradley MicroLogix 8x0 PLCs.
  - Support as for ControlLogix where possible.
- support for older Rockwell/Allen-Bradley such as PLC5 PLCs (E-series with Ethernet), SLC 500 and MicroLogix with Ethernet via CIP.
  - read/write of 16-bit INT.
  - read/write of 32-bit floating point.
  - read/write of arrays of the above (arrays not tested on SLC 500).
- support for older Rockwell/Allen-Bradley PLCs accessed over a DH+ bridge (i.e. a LGX chassis with a DHRIO module) such as PLC/5, SLC 500 and MicroLogix.
  - read/write of 16-bit INT.
  - read/write of 32-bit floating point.
  - read/write of arrays of the above.
- Support for Omron NX/NJ series PLCs as for Allen-Bradley Micro8x0.
- Support for Modbus TCP.

## Components

The following components are part of the libplctag organization.  The core  C library provides low level access to PLCs and performs all networking and PLC-specific protocol handling.  Alternate wrappers in other languages provide higher-level APIs and more convenient programming.

Go to the specific project below for language/project-specific information.

1. [libplctag](https://github.com/libplctag/libplctag) - This is the core C library.   It can be used directly in C or C++ or wrapped in other languages with some sort of FFI system.  The API provided by this library is low level.
2. [libplctag.NET](https://github.com/libplctag/libplctag.NET) - This library wraps the C core library for C# and VB.  It can also be used from Nuget.  It includes the native C DLLs for multiple platforms.
3. [PLCTag.jl](https://github.com/libplctag/PLCTag.jl) - A Julia language wrapper for the core C library.  It is available in the Julia package manager.
4. [libplctag4j](https://github.com/libplctag/libplctag4j) - A Java language wrapper for the core C library.  It includes native DLLs for multiple platforms as well.   Also available for Android as an AAR.  Soon to be available from JCenter.
5. [libplctag4android](http://github.com/libplctag/libplctag4android) - A minimal example application demonstrating use of libplctag and libplctag4j from Android.

## Contact and Support

There are two ways to ask for help or contact us.

### libplctag Forum

If you have general questions or comments about the
library, its use, or about one of the wrapper libraries, please join the Google group
[libplctag](https://groups.google.com/forum/#!forum/libplctag)!

The forum is open to all, but is by request only to keep the spammers down.  The traffic is fairly
light with usually a small number of emails per month.  It is our primary means for users to
ask questions and for discussions to happen.   Announcements about released happen on the forum.

### GitHub

If you find bugs or need specific features, please file them on GitHub's issue tracker for
the specific project.

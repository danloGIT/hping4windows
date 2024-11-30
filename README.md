# Compiling and Running hping3 on Windows

**Prerequisites:**

* **MinGW:** A development environment for Windows.
* **WinPcap or Npcap:** For packet capture.
* **libpcap and libnet:** Libraries for packet manipulation.

**Installation:**

1. **Install MinGW:**
   * Download and install the MinGW installer.
   * Ensure you select `mingw32-gcc-g++` and `mingw32-make` during installation.

2. **Install WinPcap or Npcap:**
   * Download and install Npcap in WinPcap-compatible mode.

3. **Install libpcap and libnet:**
   * Npcap usually includes libpcap.
   * Compile libnet for Windows using MinGW.

**Compiling hping3:**

1. **Download hping3 Source Code:**
   * Clone the hping3 repository:
     ```bash
     git clone [https://github.com/antirez/hping.git](https://github.com/antirez/hping.git)
     cd hping
     ```

2. **Configure the Makefile:**
   * Edit the Makefile to point to the correct paths for libpcap and libnet headers and libraries.

3. **Compile hping3:**
   * Run the `make` command in the hping3 directory.

**Setting Up hping3:**

1. **Add hping3 to the PATH:**
   * Add the directory containing `hping3.exe` to your system's PATH environment variable.

**Testing hping3:**

1. **Verify Installation:**
   * Run `hping3 --version` in the command prompt.

2. **Basic Usage:**
   * Send a SYN packet to a target:
     ```bash
     hping3 -S -p 80 <target-ip>
     ```

**Troubleshooting:**

* **Compilation Errors:**
  * Ensure correct paths for libraries in the Makefile.
  * Verify successful installation of dependencies.
* **Permission Issues:**
  * Run the command prompt as administrator.
* **Missing Libraries:**
  * Double-check library paths and installation.

By following these steps, you should be able to successfully compile and run hping3 on Windows.

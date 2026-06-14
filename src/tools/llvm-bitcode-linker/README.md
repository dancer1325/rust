# LLVM Bitcode Linker

* uses
  * link targets WITHOUT any dependency | system libraries
    * BEFORE compiling the code to native code, the code is linked in llvm-bc 
    * there is NO sensible way to link the native format / some of these targets
      * _Example:_ ptx 
  * link code compiled / such targets

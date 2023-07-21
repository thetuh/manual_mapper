# manual-map-injector
This is a continuation of my [previous project](https://github.com/thetuh/shellcode-injector) that involves injecting a DLL by manual-mapping it. However, the employed procedure requires invoking LoadLibrary to locate/administer any of its missing dependencies. Loading a DLL this way can be easily detected by hooking the function and/or its native equivalent. As such, it is trivial to negate if injection is deemed 'foreign' by performing a return address integrity check against a list of valid modules or checking if the call was never dispatched by the process itself. This updated design evades these security measures through eliminating the need of any LoadLibrary call by recursively manual-mapping any absent dependency not already loaded.
# Resources
[Blackbone](https://github.com/DarthTon/Blackbone)
[frong](https://github.com/jonomango/frong)

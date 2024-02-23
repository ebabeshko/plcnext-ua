[**runSimulation.bat**](https://github.com/ebabeshko/plcnext-ua/blob/main/simulation/runSimulation.bat) - batch file to start PLCnext Engineer Simulation from command line using [qemu](https://github.com/qemu/qemu):

```ps
rem Run PLCnext Engineer Simulation from command line
..\..\..\qemu\qemu-system-arm -machine virt,highmem=off -cpu cortex-a15 -smp 2 -m 512M -device virtio-net-pci,netdev=net0,mac=A8:74:1D:12:34:02 -netdev user,id=net0,hostfwd=tcp::5555-:22,hostfwd=tcp::5050-:443,hostfwd=tcp::41100-:41100,hostfwd=tcp::4840-:4840 -drive file=sim-axcf1152-image-base-sim-axcf2152.ext4.qcow2,if=virtio,format=qcow2 -kernel zImage-sim-axcf2152.bin -append "root=/dev/vda rw highres=off ip=dhcp console=ttyAMA0,115200" -serial mon:stdio -snapshot -nographic
```

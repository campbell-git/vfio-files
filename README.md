This is simply a collection of files that I've used to create a QEMU virtual machine 
with PCI passthrough. Important things to make note of:

- In the grub config file, only things that changed were the first few lines 
denoting the kernel initialization options.
- Make sure to  run "grub-mkconfig -o /boot/grub/grub.cfg" afterwards...
- The /usr/bin/windows-vm file must be executable since it's a launcher, "chmod +x 
/usr/bin/windows-vm".
- Make sure to add vfio.service to systemd with "systemctl enable 
/etc/systemd/system/vfio.service", then "systemctl start vfio".

I'm sure I've missed something, so feel free to check this for changes in case I add 
anything else.

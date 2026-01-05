# 🌌 NebulaOS

NebulaOS is a custom Linux-based operating system built from scratch for learning and experimentation.

## 🚀 Features (so far)
- Custom compiled Linux kernel (6.6)
- Minimal root filesystem
- BusyBox userspace
- Custom `init` (PID 1)
- User & group management
- Clean boot inside QEMU

## 🧠 Tech Stack
- Linux Kernel
- BusyBox
- initramfs
- GRUB (planned)
- QEMU (for testing)

## ▶️ Boot Instructions
```bash
qemu-system-x86_64 \
  -kernel arch/x86/boot/bzImage \
  -initrd build/initramfs.img \
  -nographic \
  -append "console=ttyS0"

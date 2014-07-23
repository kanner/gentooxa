gentooxa
========

Gentoo configuration repository to control changings between several gentoo-based systems

target:
	x86_64 hardened gentoo rolling release

how to install:
	use "git clone (repo_link) ." in '/' (needs root privileges)

what should be updated for your hardware and other settings:
	- '/etc/portage/make.conf' - initially it`s my current work configuration
	- '/etc/portage/*' configuration files (USE-flags, licenses and others, also my current work configuration)
	- '/usr/src/linux[-***]/.config' + kernel recompilation and setup in boot loader
	- '/etc/conf.d/modules'
	- '/etc/fstab' - set your partition layout
	- '/etc/conf.d/net', '/etc/conf.d/hostname', '/etc/hosts'
	- '/etc/conf.d/hwclock'
	- '/etc/conf.d/keymaps'
	- '/etc/locale.gen' (+ '# locale-gen', etc)
	- '/etc/timezone'
	- opengl/opencl and other software settings in eselect (+ 'etc/X11/xorg.conf', emerge some nvidia-/other specific packages - bumblebee, bbswitch, nvidia-settings)
	- '/boot/grub/grub.conf' - set your grub password
	- emerge other packages (current full list in '/root/gentoo-packages.sh', '/var/lib/portage/world')

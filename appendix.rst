
.. _installed-files:

===============
Installed Files
===============

An installation of Singularity {InstallationVersion}, performed as root via
``sudo make install`` consists of the following files, with ownership
and permissions required to use the `setuid` workflow:

.. code-block:: none

    # Container session / state
    var/apptainer root:root 755 (drwxr-xr-x)
    var/apptainer/mnt root:root 755 (drwxr-xr-x)
    var/apptainer/mnt/session root:root 755 (drwxr-xr-x)

    # Main executables
    bin/apptainer root:root 755 (-rwxr-xr-x)
    bin/run-apptainer root:root 755 (-rwxr-xr-x)

    # Helper executables
    libexec/apptainer root:root 755 (drwxr-xr-x)
    libexec/apptainer/bin root:root 755 (drwxr-xr-x)
    libexec/apptainer/bin/starter root:root 755 (-rwxr-xr-x)
    libexec/apptainer/bin/starter-suid root:root 4755 (-rwsr-xr-x)
    libexec/apptainer/cni root:root 755 (drwxr-xr-x)
    libexec/apptainer/cni/bandwidth root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/bridge root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/dhcp root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/firewall root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/flannel root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/host-device root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/host-local root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/ipvlan root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/loopback root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/macvlan root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/portmap root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/ptp root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/static root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/tuning root:root 755 (-rwxr-xr-x)
    libexec/apptainer/cni/vlan root:root 755 (-rwxr-xr-x)

    # Singularity configuration
    etc/apptainer root:root 755 (drwxr-xr-x)
    etc/apptainer/capability.json root:root 644 (-rw-r--r--)
    etc/apptainer/cgroups root:root 755 (drwxr-xr-x)
    etc/apptainer/cgroups/cgroups.toml root:root 644 (-rw-r--r--)
    etc/apptainer/ecl.toml root:root 644 (-rw-r--r--)
    etc/apptainer/global-pgp-public root:root 644 (-rw-r--r--)
    etc/apptainer/network root:root 755 (drwxr-xr-x)
    etc/apptainer/network/00_bridge.conflist root:root 644 (-rw-r--r--)
    etc/apptainer/network/10_ptp.conflist root:root 644 (-rw-r--r--)
    etc/apptainer/network/20_ipvlan.conflist root:root 644 (-rw-r--r--)
    etc/apptainer/network/30_macvlan.conflist root:root 644 (-rw-r--r--)
    etc/apptainer/network/40_fakeroot.conflist root:root 644 (-rw-r--r--)
    etc/apptainer/nvliblist.conf root:root 644 (-rw-r--r--)
    etc/apptainer/remote.yaml root:root 644 (-rw-r--r--)
    etc/apptainer/rocmliblist.conf root:root 644 (-rw-r--r--)
    etc/apptainer/seccomp-profiles root:root 755 (drwxr-xr-x)
    etc/apptainer/seccomp-profiles/default.json root:root 644 (-rw-r--r--)
    etc/apptainer/apptainer.conf root:root 644 (-rw-r--r--)

    # Bash completion configuration
    etc/bash_completion.d root:root 755 (drwxr-xr-x)
    etc/bash_completion.d/apptainer root:root 644 (-rw-r--r--)

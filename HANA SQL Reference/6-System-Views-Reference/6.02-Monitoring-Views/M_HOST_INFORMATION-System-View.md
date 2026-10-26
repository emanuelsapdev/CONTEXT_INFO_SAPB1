# 6.2.128 M_HOST_INFORMATION System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1815–1821

Provides host information such as machine and OS configuration.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | NVARCHAR(64) | Displays the host name. |
| KEY | NVARCHAR(64) | Displays the key. |
| VALUE | NVARCHAR(2000) | Displays the value. |

## Additional Information

This view contains some hostspecific information. The following table describes the contents of the individual lines of the monitor view (`VALUE`), as identified by `KEY:`. The values are updated once per minute. Most values require the INIFILE ADMIN privilege to view, as noted in the table.

| **KEY** | **Description** | **Requires INIFILE ADMIN** |
| --- | --- | --- |
| active | Displays the state of the host's nameserver: Yes (started) or No (stopped). | Y |
| async_io_limit | Displays the maximum number of asynchronous input and output requests. The Kernel parameter is `fs.aio-max-nr`. For more information, see the ACTIVE_ASYNC_IO_COUNT value in the M_HOST_RESOURCE_UTILIZATION System View topic. | Y |
| build_branch | Displays the build branch name in the revision control software. | N |
| build_cloud_edition | Displays the Cloud version number for Cloud releases. | Y |
| build_compiler | Displays the build compiler. | Y |
| build_gen | Displays either "opt" or "dbg". | Y |
| build_time | Displays the build compile time. | Y |
| build_version | Displays the build version number. This is the same as M_DATABASE.VERSION. | N |
| clocksource.current_clocksource | Displays the clock source. | Y |
| container | Displays whether SAP HANA is running inside a Docker container. | Y |
| cpu_clock | Displays the CPU clock in MHz. | Y |
| cpu_cores - Deprecated | Displays the number of CPU cores. | Y |
| cpu_flags | Displays the CPU flags. | Y |
| cpu_manufacturer | Displays the CPU manufacturer. | Y |
| cpu_model | Displays the CPU model. | Y |
| cpu_sockets | Displays the number of CPU sockets per host. | Y |
| cpu_summary | Displays the CPU summary. This is preformatted cpu_cores + cpu_threads + cpu_clock string. | Y |
| cpu_threads | Displays the number of logical CPU cores, for example hyper threading. | Y |
| cpu.cpufreq.scaling_govenor | Displays the cpu_threads mode. | Y |
| cpu.cpuidle.current_driver | Displays the active cpuidle driver. | Y |
| cpu.cpuidle.intel_idle.max_cstate | Displays the maximum depth of the C-state. A value of 0 disables intel_idle and the CPU falls back to acpi_idle. | Y |
| crypto_fips_provider | Displays whether SAP HANA is using a FIPS 140-2 certified crypto provider for crypto operations. | Y |
| crypto_provider | Displays the name of the Cryptographic Provider that is used for SSL, SAML, and so on. | Y |
| crypto_provider_version | If SAP HANA is using a FIPS 140-2 certified crypto provider then this column displays the version. | Y |
| daemon_active | Displays YES if hdbdaemon is running. | Y |
| hw_manufacturer | Displays the hardware manufacturer from BIOS. | Y |
| hw_model | Displays the hardware model from BIOS. | Y |
| kernel.numa_balancing | Displays 0 if the automatic NUMA (non-uniform memory access) balancing is off. | Y |
| kernel.shmall | Displays how much, in 4KB blocks, SysV shared memory is available in the Linux system as a whole. | Y |
| kernel.shmmax | Displays the allowed individual SysV shared memory segment size, in bytes. | Y |
| kernel.shmmni | Displays the system-wide maximum number of shared memory segments. | Y |
| kernel.transparent_hugepage.enabled | Displays the status of the transparent hugepage. | Y |
| mem_phys | Displays the physical memory size in bytes. | Y |
| mem_swap | Displays the swap size in bytes. | Y |
| memory_map_area_limit | Displays the maximum number of virtual memory map areas that a process can own, for example `vm.max_map_count`. | Y |
| net_domain | Displays the domain name of the current host or "-" if not configured. | Y |
| net_hostnames | Displays all known host names of this host. | Y |
| net_nameserver_bindings | Displays all interfaces that the nameserver listens on, as configured with global.ini/[communication]/ listeninterface, [internal_hostname_resolution] and [system_replication...]. | Y |
| net_publicports | Displays the net public ports. | Y |
| net_ip_addresses | Displays all IP addresses of this host. | Y |
| net_port_ephemeral_max_count | Displays the number of unreserved ports, which are in net.ipv4.ip_local_port_range. | Y, available only in SYSTEMDB. |
| net_port_ranges | Displays the relevant ports for SAP HANA and is dependent on the running services. | Y, available only in SYSTEMDB. |
| net_port_unreserved_ranges | Displays the relevant ports for SAP HANA that are not reserved and that are within the net.ipv4.ip_local_port_range. | Y, available only in SYSTEMDB. |
| net_publicname | Displays the public host name used by client interfaces. This can contain a host name, FQDN, or IP address. | N |
| net_realhostname | Real host name if installation was done with a virtual host name, else set to "-" | Y |
| net.core.somaxconn | Displays the size limit of the accept backlog of a listening socket in bytes. | Y |
| net.ipv4.tcp_max_syn_backlog | Displays the size of the SYN backlog in bytes. | Y |
| net.ipv4.tcp_rmem | Displays the minimum, default, and maximum size of the TCP receive buffer in bytes. | Y |
| net.ipv4.tcp_syn_retries | Displays the number of times initial SYNs for an active TCP connection attempt are retransmitted. | Y |
| net.ipv4.tcp_timestamps | Displaying 1 enables TCP timestamps, adding the timestamp field to the TCP header. | Y |
| net.ipv4.tcp_tw_recycle | Displaying 1 reduces the time a connection spends in the TIME_WAIT state. The precondition is `net.ipv4.tcp_timestamps` = 1. | Y |
| net.ipv4.tcp_tw_reuse | Displaying 1 allows SAP HANA to reuse a client port immediately after the connection is closed. The precondition is `net.ipv4.tcp_timestamps` = 1. | Y |
| net.ipv4.tcp_window_scaling | Displays if the TCP window scaling is enabled: TRUE/FALSE. | Y |
| net.ipv4.tcp_wmem | Displays the minimum, default, and maximum size of the TCP send buffer in bytes. | Y |
| open_file_limit | Displays the maximum number of open file descriptor handles on the host. The Kernel parameter is `fs.file-max`. For more information, see the OPEN_FILE_COUNT value in the M_HOST_RESOURCE_UTILIZATION System View topic. | Y |
| os_cpe_name | Displays operating system information. | Y |
| os_kernel_version | Displays the Linux kernel version. | Y |
| os_name | Displays the operating system name, as shown in the PRETTY_NAME field in `/etc/os-release`. | Y |
| os_ppms_name | Displays the operating system name as used by SAP PPMS. | Y |
| os_rlimit_nofile | Displays the Linux RLIMIT_NOFILE value. | Y |
| os_user | Displays the operating system user. | Y |
| platform | Displays "windows" or "unix". | Y |
| sap_retrieval_path | Displays the hostspecific base directory. | Y |
| sap_retrieval_path_shared | Displays "yes" if all sap_retrieval_path directories are located on a shared storage. | Y |
| sapsystem | Displays the two digit SAP system instance number. | N |
| secure_store | Displays "available" if the secure store is present and readable. | Y |
| sid | Displays the three letter SAP system name. | N |
| start_time | Displays the start time of the name server. | Y |
| timezone_base_name | Displays the base time zone name. | Y |
| timezone_dst_name | Displays the daylight savings time zone name. | Y |
| timezone_name | Displays the time zone name. | Y |
| timezone_offset | Displays the time zone offset to GMT, in seconds. | Y |
| timezone_tz_name | Displays the time zone set in the environment variable TZ. | Y |
| topology_mem_info | Displays an error message if shared memory could not be created. | Y |
| topology_mem_type | Always specified as "shared". | Y |

## Related Information

M_HOST_RESOURCE_UTILIZATION System View [→](M_HOST_RESOURCE_UTILIZATION-System-View.md) M_HOST_NETWORK_STATISTICS System View [→](M_HOST_NETWORK_STATISTICS-System-View.md) https://launchpad.support.sap.com/#/notes/2382421 https://www.kernel.org/doc/Documentation/networking/ip-sysctl.txt https://www.kernel.org/doc/Documentation/sysctl/fs.txt https://www.kernel.org/doc/Documentation/sysctl/vm.txt

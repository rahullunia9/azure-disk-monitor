# Azure VM Disk Space Monitoring

Assignment to check for monitoring disk space on Azure Windows and Linux VMs using Azure Monitor, Log Analytics, Azure Policy, and Ansible.

 [Design document](DESIGN.md) — includes the architecture , security, VM discovery/enrollment, alert thresholds, and scaling approach.

## Supporting artifacts

- `docs/Azure VM Disk Space Monitoring Flowchart.png` — high-level architecture diagram
- `ansible/check-windows-disks.yml` — on-demand Windows disk and AMA check
- `ansible/check-linux-disks.yml` — on-demand Linux filesystem and AMA check
- `ansible/inventory.ini.example` — sample inventory (replace example hosts; keep credentials out)
- `kql/disk-warning.kql` — warning query (<15% free)
- `kql/disk-critical.kql` — critical query (<10% free)
- `kql/disk-overview.kql` — latest free space by VM and drive/mount point

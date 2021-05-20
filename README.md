# ansible-telegraf-agent

Ansible playbook for setting up Telegraf agent.

## Example usage

Create `config.yml` file with your minimum configuration.

```yaml
influxdb_urls: ["https://example.com:8086"]
influxdb_database: "telegraf"
influxdb_username: "username"
influxdb_password: "secret"

input_plugins:
  - cpu
  - disk
  - diskio
  - kernel
  - mem
  - processes
  - swap
  - system
  - net
  - netstat
  - interrupts
  - syslog
```

Run ansible playbook:

```bash
ansible-playbook main.playbook.yml -i 192.168.0.1, -u username -K
```

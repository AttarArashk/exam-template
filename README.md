# Scenario 2 — Ansible

Do not change the `inventory/` folder structure.
Put `ansible_user` and `ansible_host` in `inventory/inventory/monitoring.yml`.

## Option 1 — given VM

Use the **second** SSH target from https://auth.fanap.kubelog.ir

Then run:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
ansible-playbook -i inventory main.yml -b --private-key ~/.ssh/id_ed25519_fanap
```

## Option 2 — Vagrant

```bash
vagrant up
```

Set inventory to the Vagrant user and IP (`vagrant` / `192.168.56.10`).
Keep this `Vagrantfile` in the repo.

The code must run. I will run what you leave here.

# Ansible - Nginx Deployment

Tento projekt ukazuje použití **Ansible** pro automatizovanou konfiguraci a nasazení webového serveru **Nginx**.

## Struktura projektu
- `inventory/hosts.ini` – definice cílových serverů  
- `group_vars/all.yml` – globální proměnné pro Ansible  
- `roles/nginx/` – role pro instalaci a konfiguraci Nginx  
  - `tasks/main.yml` – hlavní úkoly pro instalaci a nastavení Nginx  
  - `templates/nginx_site.j2` – šablona konfigurace pro Nginx  
  - `templates/index.html.j2` – jednoduchá ukázková webová stránka  
- `site.yml` – hlavní playbook pro nasazení Nginx  

## Požadavky
- Ansible nainstalovaný na řídícím serveru  
- SSH přístup na cílový server  

## Použití
1. Uprav `inventory/hosts.ini` a nastav správné IP adresy/server  
2. Spusť příkaz:  

   ```bash
   ansible-playbook -i inventory/hosts.ini site.yml


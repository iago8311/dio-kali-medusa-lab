# Enumeração de Serviços

O primeiro passo do laboratório foi identificar os serviços disponíveis na máquina Metasploitable 2.

Foi utilizado o Nmap para realizar a enumeração das portas mais relevantes para o cenário proposto.

```bash
nmap -n -sV -p 21,22,80,139,445 192.168.56.101
```

Resultado obtido:

```text
PORT    STATE SERVICE     VERSION
21/tcp  open  ftp         vsftpd 2.3.4
22/tcp  open  ssh         OpenSSH 4.7p1 Debian 8ubuntu1
80/tcp  open  http        Apache httpd 2.2.8
139/tcp open  netbios-ssn Samba smbd 3.X - 4.X
445/tcp open  netbios-ssn Samba smbd 3.X - 4.X
```

Serviços identificados:

- FTP (porta 21)
- SSH (porta 22)
- HTTP (porta 80)
- SMB/NetBIOS (portas 139 e 445)

Esses serviços foram utilizados nas etapas posteriores do laboratório para demonstração de cenários de autenticação e análise de segurança.

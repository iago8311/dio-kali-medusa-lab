# Análise de Formulário Web (DVWA)

A aplicação DVWA foi utilizada para demonstrar o funcionamento de mecanismos de autenticação em aplicações web.

Durante a análise da página de login foi possível identificar os parâmetros enviados pelo formulário.

Parâmetros observados:

- username
- password
- Login

Os dados foram visualizados por meio das ferramentas de desenvolvedor do navegador.

## Simulação de Testes de Autenticação

```bash
medusa -h 192.168.56.101 -U users.txt -P pass.txt -M http \
-m PAGE:/dvwa/login.php \
-m FORM:"username=USER&password=PASS&Login=Login" \
-m FAIL="Login failed" -t 6
```

A atividade permitiu compreender como aplicações web tratam credenciais de acesso e os riscos associados a mecanismos de autenticação inadequadamente protegidos.

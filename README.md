# Playteca

Projeto desenvolvido com Flask, Python, Bootstrap e HTML, utilização de herança em template para criar novos jogos, fazer login para ter acesso a lista de jogos, visualização da lista e inserir conteudo na lista com nome, categoria e console dos jogos que queira adicionar. Usando também criptografia para que não haja alteração de senhas por cookies. 
Tendo organização no código
Ponte entre HTML e Python
Criações de endpoints (rotas)
Classe, instância de classes POO

## Instalação

Para instalação basta dar git clone: https://github.com/Jullyhein/Playteca.git

Para instalar as bibliotecas: pip install -r requirements.txt

run do vscode jogoteca.py

## Playteca

Para podermos ter uma lista de jogos e ir adicionando mais jogos a lista, precisamos autenticar o usuário para ter esse tipo de acesso. E esse projeto tem esse intuito, conversar com o usuário para ele acessar a listagem de jogos com: nomes, categoria e console, e além disso ele adicionar os jogos que ele quer. A página inicial temos a tela de login que foi configurada com boostrap e um endpoint acessando a o login.html para solicitar os dados do usuário:

![Texto alternativo](https://private-user-images.githubusercontent.com/97550028/303086163-9e1d6e6c-5dfd-4dbb-b322-1e60caafadbe.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDczMjgzMTUsIm5iZiI6MTcwNzMyODAxNSwicGF0aCI6Ii85NzU1MDAyOC8zMDMwODYxNjMtOWUxZDZlNmMtNWRmZC00ZGJiLWIzMjItMWU2MGNhYWZhZGJlLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMDclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjA3VDE3NDY1NVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTk5NjRjMzA4OWY4NDM5ZTNiZTY4ZTliNzA4MWNiNGIxMzM4NTJhNTQ5MjQ0ZTZlMDIxYTAyNzllMjQ5NzFlZGQmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.GEoGe17AD_2EKzT4F329s9Js_23foLl2g6Ohitjmrbo)

A tela de cadastro de jogos novos:

![Texto alternativo](https://private-user-images.githubusercontent.com/97550028/303087461-aee88c66-a8ca-4f53-ac7c-e3131602c336.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDczMjg1ODksIm5iZiI6MTcwNzMyODI4OSwicGF0aCI6Ii85NzU1MDAyOC8zMDMwODc0NjEtYWVlODhjNjYtYThjYS00ZjUzLWFjN2MtZTMxMzE2MDJjMzM2LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMDclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjA3VDE3NTEyOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTNlNmFiYjgyN2ZhZDRiYzA0NjQ0N2Y1YTEyZjhmMWEwYWQ2NmE1N2FiZDI5ZWQzODFhYzVhNjU3MDg3ODgxNDcmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.Fnhy3gI2bsCN7g2OS5sa7E8IuhE61HugGIyttxsRUsk)


E a tela de logout. 

![Texto alternativo](https://private-user-images.githubusercontent.com/97550028/303087687-3e83f418-cc92-42d7-8f35-3ac350cb573d.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDczMjg2NDIsIm5iZiI6MTcwNzMyODM0MiwicGF0aCI6Ii85NzU1MDAyOC8zMDMwODc2ODctM2U4M2Y0MTgtY2M5Mi00MmQ3LThmMzUtM2FjMzUwY2I1NzNkLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMDclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjA3VDE3NTIyMlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTg3YTFkMTE4OWFhODE3YTkwZDBhNGY5YTA0MzE1NTAxMjNjZWVmYzA2ZjY0NTg4OGE3NGVkNWI4ZjQ0MzJhOTImWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.jGDlRkAETlaPtYcOSjpLuBT7EK5u6AuT6Ss5dwpI_64)


## Tech

Linguagem: 

Python <div align="center">
<img src="https://private-user-images.githubusercontent.com/97550028/303081574-27be6432-7d6f-4bd5-8def-6a837556cacc.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDczMjcyODIsIm5iZiI6MTcwNzMyNjk4MiwicGF0aCI6Ii85NzU1MDAyOC8zMDMwODE1NzQtMjdiZTY0MzItN2Q2Zi00YmQ1LThkZWYtNmE4Mzc1NTZjYWNjLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMDclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjA3VDE3Mjk0MlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWNhN2UxM2I0NjA5MzU1NTNlYmQzZDFiYmQ5YTJlOGE2MzAyNGE2NjAzYzJhNzgzMGE2NGU0M2U0OTllOTYxMWMmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.WppXXSIOphslqIHk9Roz1ji-22eaNgeWs6i4-LX97pk" width="50px" />
</div>
Bootstrap <div align="center">
<img src="https://private-user-images.githubusercontent.com/97550028/303083681-42bff79f-f7b0-4401-994f-b5491c84b77f.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDczMjc4MjcsIm5iZiI6MTcwNzMyNzUyNywicGF0aCI6Ii85NzU1MDAyOC8zMDMwODM2ODEtNDJiZmY3OWYtZjdiMC00NDAxLTk5NGYtYjU0OTFjODRiNzdmLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMDclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjA3VDE3Mzg0N1omWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWZjMzIyNWUzMzZjNzBjZjIxMGFjZDBjMTdlNzBiY2Q3NDhiZTlkY2M2YWY4NDU5NDg3MWQzOGFkMWUzY2JlMmQmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.B8LAjSEHh4U8sRr-mogoC51mV1qW09jRxnqJBgu8vk8" width="50px" />
</div>
HTML <div align="center">
<img src="https://private-user-images.githubusercontent.com/97550028/303083821-1a2383b7-6edb-486b-832f-57f25d4087ee.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDczMjc5MDUsIm5iZiI6MTcwNzMyNzYwNSwicGF0aCI6Ii85NzU1MDAyOC8zMDMwODM4MjEtMWEyMzgzYjctNmVkYi00ODZiLTgzMmYtNTdmMjVkNDA4N2VlLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMDclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjA3VDE3NDAwNVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTdhY2M4YTI0YmMxMGRhZjQ2ZWU4MDFmYmRiY2MxMTUyNzczY2I3NjRjYmM5N2M5NTlmYTg0NTY2Mzc4Y2VhODUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.A4Q0fc3HRho--71ucD8IaCJHTQIY1asnvlMR_SV6qlE" width="50px" />
</div>

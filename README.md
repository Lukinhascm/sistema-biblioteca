# Sistema de Biblioteca – Projeto 2

Projeto da disciplina Construção de Backend (IESB). Gerencia autores,
livros, membros e empréstimos com regras de negócio em Django.

## Funcionalidades
- Cadastro de Autores, Livros e Membros pelo Django Admin
- Empréstimo com prazo de 14 dias e controle de estoque
- Devolução com reposição de cópia
- Indicação de empréstimos atrasados
- Relatório de livros mais emprestados

## Como rodar
1. python -m venv venv  e ative o ambiente
2. pip install -r requirements.txt
3. python manage.py migrate
4. python manage.py createsuperuser
5. python manage.py runserver

## Dificuldades Encontradas
A parte que mais me deu trabalho foi entender o controle do estoque. Eu precisava decrementar `copias_disponiveis` na hora do empréstimo e incrementar de novo na devolução, sem deixar o número ficar errado se alguém tentasse devolver duas vezes. Também demorei para encaixar as regras nas Views, principalmente para bloquear empréstimo quando não havia cópia disponível. Outro ponto foi ajustar a property `esta_atrasado` para o badge de atraso aparecer certo no template de "meus empréstimos", porque no começo eu chamava como se fosse um método e o Django não mostrava o atrasado.

## Autor
Lucas de carvalho melo – IESB 2026

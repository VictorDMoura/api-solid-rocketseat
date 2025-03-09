## App

GymPass style app

## RFs (Requisitos funcionais)

- [ ] Deve ser possível se cadastras;
- [ ] Deve ser possível se autenticar;
- [ ] Deve ser possível obter os perfil de um usuário logado;
- [ ] Deve ser possível o usuário obter seu histórico de check-in;
- [ ] Deve ser possível o usuário buscar academias próximas;
- [ ] Deve ser possível o usuário buscar academias pelo nome;
- [ ] Deve ser possível o usuário realizar o check-in em uma academia;
- [ ] Deve ser possível validar o check-in de um usuário;
- [ ] Deve ser possível cadastrar um academia;

## RNs (Regras de negócios)

- [ ] O usuário não deve poder se cadastrar com um e-mail duplicado;
- [ ] O usuário não pode fazer 2 check-ins no mesmo dia;
- [ ] O usuário não pode fazer check-in se não estiver perto (100m) da academia;
- [ ] O check-in só pode ser validado até 20 minutos após criado;
- [ ] O check-in só pode ser validado por administradores;
- [ ] A academia só pode ser cadastrado por administradores;

## RNFs (Requisitos não-funcionais)

- [ ] A senha do usuário precisa estar criptografada;
- [ ] Os dados da aplicação precisam estar persistidos em um banco PostgreSQL;
- [ ] Todas as listas de dados precisam estar paginadas com 20 itens por páginas;
- [ ] O usuário deve ser identificado por um JWT (JSON Web Token)

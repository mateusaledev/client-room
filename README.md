# client-room

Front Angular do gerenciador de salas de reunião.

## Status

Estudo. Não está em produção. Angular 9 (release candidate) — stack antiga de propósito; é o front do exercício.

## Para que serve

Tela para listar, criar, editar e ver detalhes de salas. Consome a API [gerenciador-sala-reuniao](https://github.com/mateusaledev/gerenciador-sala-reuniao). Os dois repos formam o mesmo produto.

## Stack

- Angular 9 RC · TypeScript · RxJS · Bootstrap 4

## Como executar

Pré-requisitos: Node.js compatível com Angular 9 (a CLI do projeto é `9.0.0-rc.7`), npm.

Suba primeiro o backend. O service chama `http://localhost:8082/api/v1/rooms`. O backend padrão sobe na porta **8080** — alinhe `server.port` no Spring ou o `baseUrl` em `src/app/room.service.ts`.

```bash
git clone https://github.com/mateusaledev/client-room.git
cd client-room
npm install
ng serve
```

App em `http://localhost:4200`. Rotas: `/rooms`, `/add`, `/update/:id`, `/details/:id`.

## O que faz

- Lista de salas
- Cadastro e edição
- Detalhe de uma sala
- Exclusão via `RoomService`

## Estrutura

```
src/app/create-room
src/app/room-list
src/app/room-details
src/app/update-room
src/app/room.service.ts
```

## Backend

https://github.com/mateusaledev/gerenciador-sala-reuniao

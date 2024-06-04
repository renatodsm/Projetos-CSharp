# Sistema de Agendamento de Tarefas
---

## Funcionalidades

### Cadastro de Tarefas
- Permite aos usuários cadastrar novas tarefas.

### Atualização de Tarefas
- Permite aos usuários atualizar informações das tarefas existentes.

### Exclusão de Tarefas
- Permite aos usuários excluir tarefas existentes.

### Consulta de Tarefa por ID
- Permite aos usuários consultar uma tarefa específica pelo seu ID.

### Consulta de Todas as Tarefas
- Permite aos usuários consultar todas as tarefas cadastradas.

### Consulta de Tarefas por Título
- Permite aos usuários consultar tarefas pelo seu título.

### Consulta de Tarefas por Data
- Permite aos usuários consultar tarefas por uma data específica.

### Consulta de Tarefas por Status
- Permite aos usuários consultar tarefas pelo seu status.

## Endpoints

### GET /Tarefa/{id}
- Retorna os detalhes da tarefa com o ID especificado.

### PUT /Tarefa/{id}
- Atualiza os dados da tarefa com o ID especificado.

### DELETE /Tarefa/{id}
- Exclui a tarefa com o ID especificado.

### GET /Tarefa/ObterTodos
- Retorna a lista de todas as tarefas cadastradas.

### GET /Tarefa/ObterPorTitulo?titulo={titulo}
- Retorna as tarefas que correspondem ao título especificado.

### GET /Tarefa/ObterPorData?data={data}
- Retorna as tarefas para a data especificada.

### GET /Tarefa/ObterPorStatus?status={status}
- Retorna as tarefas com o status especificado.

## Modelo de Dados (Tarefa)

```json
{
  "id": 0,
  "titulo": "string",
  "descricao": "string",
  "data": "2022-06-08T01:31:07.056Z",
  "status": "Pendente"
}

# Sistema de Estacionamento

Este é um sistema de estacionamento desenvolvido em C# que permite o gerenciamento de veículos estacionados em um determinado local. Ele possibilita a adição, remoção e listagem de veículos, além de calcular o custo do estacionamento com base no tempo de permanência.

## Funcionalidades

### Adicionar Veículo
- Os usuários podem adicionar veículos ao estacionamento.
- O sistema solicita ao usuário que insira a placa do veículo.
- Após a inserção da placa, o veículo é adicionado à lista de veículos estacionados.

### Remover Veículo
- Os usuários podem remover veículos do estacionamento.
- O sistema solicita ao usuário que insira a placa do veículo a ser removido.
- Após a inserção da placa, o sistema solicita a quantidade de horas que o veículo permaneceu estacionado.
- O sistema calcula o custo do estacionamento com base no tempo de permanência e nos preços estabelecidos.
- Após a remoção do veículo, o sistema exibe o custo total do estacionamento para o veículo removido.

### Listar Veículos
- Os usuários podem visualizar uma lista de todos os veículos atualmente estacionados.
- Se não houver veículos estacionados, o sistema exibe uma mensagem informando que não há veículos estacionados.

## Requisitos Não Funcionais

### Usabilidade
- A interface do usuário é simples e intuitiva para facilitar o uso por usuários não técnicos.
- Mensagens claras e informativas são exibidas para orientar os usuários durante a interação com o sistema.

### Eficiência
- O sistema é capaz de lidar com um grande número de veículos estacionados de forma eficiente.
- As operações de adição, remoção e listagem de veículos são realizadas de forma rápida e responsiva.

### Segurança
- Apenas usuários autorizados podem realizar operações de adição e remoção de veículos.
- As informações dos veículos e seus custos de estacionamento são protegidas contra acesso não autorizado.

## Restrições
- O sistema é implementado em C# utilizando o paradigma de programação orientada a objetos.
- Os custos de estacionamento são calculados com base em um preço inicial e um preço por hora, fornecidos durante a inicialização do sistema.

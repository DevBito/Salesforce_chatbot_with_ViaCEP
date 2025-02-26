# Salesforce Einstein Bot + ViaCEP Integration

Projeto que integra o Salesforce Einstein Bot com a API do ViaCEP para obter o endereço a partir de um CEP informado pelo usuário.

## Tecnologias Utilizadas
- Salesforce Einstein Bot
- Apex (Classe: ViaCepService.apxc)
- Salesforce Flow
- API ViaCEP
- Remote Site Settings

## Como Funciona?
- O Einstein Bot pergunta ao usuário qual é o CEP.
- O bot chama um Flow, que executa a Apex Action.
- A classe Apex (ViaCepService.apxc) faz a requisição HTTP para a API do ViaCEP.
- O Flow recebe os dados da API e formata a resposta.
- O bot exibe o endereço formatado para o usuário.

## Estrutura do Código
src
 ├── 📜 ViaCepService.apxc   # Classe Apex para consulta ao ViaCEP
 ├── 📜 README.md            # Documentação do projeto

## Configuração Necessária
- Adicionar https://viacep.com.br em Remote Site Settings.
- Criar um Flow para chamar a Apex Action ViaCepService.buscarEndereco.
- Garantir que o Einstein Bot está configurado corretamente para chamar o Flow.
- Configurar as permissões do usuário do bot para executar o Flow e chamadas externas.
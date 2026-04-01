# Documento de Escopo - Inova Tech

## 1. Identificação do projeto
**Nome do projeto:** Inova Tech  
**Grupo (nomes):** Sarah Alves Lima, Levi Bambam Soares Machado, Victor Hugo Ferreira Cristianini, Sílvio Sapuile, Kelvyn Lee borges de Souza e Enzo dos Santos Neves, Gabriela Cardozo Cardin, Gustavo Felix de Almeida, Marcel Airo Oliveira da Silva.  
**Versão/data:** Versão 3.2 - 04/03/2026

---

## 2. Visão geral da empresa (contexto)
A Inova Tech é uma empresa de pequeno porte especializada em dispositivos móveis e soluções inteligentes, atuando como loja física e hub de distribuição regional na Vila Prudente, São Paulo. Nosso modelo de negócio atende o consumidor final.

Com operação das 08h00 às 22h00, a unidade utiliza totens de autoatendimento para otimizar o fluxo e reduzir filas. A experiência é totalmente integrada: o cliente consulta o estoque em tempo real, compra online e retira no local, garantindo agilidade.

Nossa equipe de 10 colaboradores opera em turnos de 6 horas (escala 5x2), com supervisão constante para manter o padrão de excelência. Investimos pesado em capacitação técnica via plataformas parceiras, garantindo que nossos atendentes sejam especialistas em tendências tecnológicas.

**Desafio e Estratégia:** Embora nossa cultura seja voltada para alta performance em vendas, reconhecemos o desafio de manter a documentação de inventário rigorosa em um ambiente acelerado. Dado que o setor de tecnologia exige um giro rápido para evitar a desvalorização de ativos, priorizamos uma reposição ágil e a acuracidade entre o estoque físico e o sistema. Esse rigor no controle permite compras mais inteligentes, reduz perdas financeiras e consolida a confiança do nosso cliente.

---

## 3. Problema atual (dor) e consequências
O processo de gerenciamento do estoque ocorre por contagem na planilha e comunicação via WhatsApp.
Impactos como atraso nas atualizações do estoque, perda de dados, fornecimento de produtos fora de estoque, podem ocasionar em erros, atrasos e conflitos internos. Informação para toda equipe no sistema, desde a atualização dos produtos para todos os departamentos envolvendo o estoque, dando prioridade para um sistema automático e organizado, deixando um sistema mais otimizado em dias de pico e falta de responsáveis.

A informação estará disponível para todos, representadas por cores (verde e vermelho):
* **VERDE:** Suficiente.
* **VERMELHO:** Em falta/Estoque mínimo.

---

## 4. Objetivo da solução (o que o sistema vai resolver)
**Objetivo principal:**
Implementar um sistema informatizado de gestão de estoque que permita controle em tempo real, redução de erros e melhor planejamento de reposição.

**Benefícios esperados:**
* O sistema resolve falta de controle.
* Registro automático de entrada e saída de mercadorias.
* Atualização em tempo real do estoque na planilha.

---

## 5. Stakeholders e perfis de usuário
* **Supervisor:** (Relatórios)
* **Gerente:** (Corrige)

---

## 6. Escopo do sistema (IN / OUT)

**Dentro do escopo (IN):**
* Cadastro dos produtos
* Edição dos produtos
* Consulta de produtos
* Registro de movimentações de estoque
* Emissão de alerta, caso atinja o estoque mínimo definido

**Fora do escopo (OUT):**
* Uso de chat para conversas
* Opção de entregas em geral
* Interação com o sistema de vendas

---

## 7. Requisitos Funcionais (RF)
* **RF01** – Cadastrar produtos com campos obrigatórios (nome, código, categoria, quantidade em estoque, preço de custo e preço de venda).
* **RF02** – Atualizar a quantidade de produtos automaticamente a cada entrada ou saída registrada.
* **RF03** – Registrar movimentações de estoque (entrada, saída, ajuste), informando data, tipo e responsável.
* **RF04** – Consultar produtos por nome, código ou categoria.
* **RF05** – Emitir alerta quando a quantidade de um produto atingir o estoque mínimo ou falta de estoque definido.
* **RF06** – Gerar relatório de movimentações por período (diário, mensal ou personalizado).
* **RF07** – Permitir a edição e inativação de produtos cadastrados.
* **RF08** – Salvar automaticamente após cada alteração.

---

## 8. Regras de Negócio (RN)
* **RN01** – Não é permitido registrar saída de produto com quantidade superior à disponível em estoque.
* **RN02** – Todo produto deve possuir um código único (não pode haver duplicidade).
* **RN03** – Toda movimentação de estoque deve registrar data, hora e responsável pela operação.
* **RN04** – Produtos com estoque igual ou inferior ao mínimo devem gerar alerta automático.
* **RN05** – Não é permitido excluir produtos que possuam histórico de movimentações; apenas inativá-los.
* **RN06** – O preço de venda não pode ser inferior ao preço de custo.
* **RN07** – Ajustes de estoque devem exigir justificativa obrigatória.

---

## 9. Requisitos Não Funcionais (RNF) e restrições técnicas

### RNF 01 — Usabilidade
* **Descrição:** O sistema deve possuir interface simples e intuitiva, permitindo que o usuário execute suas tarefas com facilidade e sem necessidade de treinamento prévio, evitando perda de tempo durante a utilização.
* **Restrição Técnica:** O sistema deverá ser desenvolvido com interface gráfica padrão para desktop, garantindo que os usuários consigam operar todas as funções sem treinamento adicional.

### RNF 02 — Desempenho do Software
* **Descrição:** O sistema deve apresentar bom desempenho, garantindo velocidade adequada, baixo tempo de resposta e capacidade de processamento sem travamentos.
* **Restrições Técnicas:**
    1. O sistema deverá processar e listar até 100 produtos cadastrados sem apresentar travamentos ou lentidão.
    2. O sistema deve funcionar nos computadores atuais da empresa, sem necessidade de upgrade ou melhoria de hardware.

### RNF 03 — Backup e Persistência de Dados
* **Descrição:** O sistema deve evitar perda de informações, garantindo o armazenamento seguro dos dados e funcionamento mesmo sem conexão com a internet.
* **Restrição Técnica:** O sistema deverá utilizar exclusivamente banco de dados local para armazenamento das informações, garantindo o funcionamento offline.

### RNF 04 — Compatibilidade
* **Descrição:** O sistema deve ser compatível com os computadores da empresa.
* **Restrição Técnica:** O sistema deverá ser desenvolvido para funcionar exclusivamente no sistema operacional Windows, considerando que todos os computadores da empresa utilizam essa plataforma.

### RNF 05 — Segurança
* **Descrição:** O sistema deve garantir controle de acesso, proteção das informações e rastreabilidade das ações realizadas.
* **Restrição Técnica:** Todo usuário deverá realizar autenticação no sistema por meio de login e senha.

---

## 10. Obstáculos, riscos e restrições do mundo real
1.  **Computadores antigos (RNF 02 e RNF 04)** – Como o sistema deve rodar nos computadores atuais da empresa e apenas no Windows, pode haver lentidão se as máquinas forem antigas ou tiverem pouca memória.
2.  **Risco de perda de dados (RNF 03)** – Como o banco de dados será local e o sistema funciona offline, se o computador apresentar defeito ou vírus, pode haver perda de informações caso não seja feito backup.
3.  **Resistência dos funcionários (RNF 01)** – Mesmo sendo um sistema simples, alguns usuários podem ter dificuldade para se adaptar ou podem resistir à mudança.
4.  **Cadastro feito de forma diferente por cada usuário (RNF 02)** – Se não houver um padrão no cadastro dos produtos, podem surgir informações repetidas ou erradas. Isso pode deixar o sistema mais lento, principalmente quando chegar perto dos 5.000 produtos.

---

## 11. Dados principais (entidades) e relacionamentos esperados

* **Cadastro de Produto:** ID Produto, Categoria, Quantidade no estoque, Nome, Valor do Produto, Valor de Venda.
* **Reabastecimento do Estoque:** ID Produto, Quantidade, Data/Hora, Custo.
* **Pesquisa Produto:** ID Produto, Categoria, Nome.
* **Relatório:** Quantidade de produto vendido, Valor total de produto vendido, Entrada e Saída (Custo), Lucro ou Prejuízo.
* **Venda:** ID Venda, Destinatário, Quantidade, Valor, Data/Hora.
* **Estoque:** Total de produtos, ID Estoque, Quantidade, ID Produto.

---

## 12. Casos de uso (lista + breve descrição)

* GERENTE
    * Consultar histórico de produtos: Visualiza entradas, saídas e desempenho dos produtos por período.
    * Editar ou cancelar: Permite corrigir, ativar ou desativar produtos.
    
* SUPERVISOR
    * Atualizar estoque: O sistema ajusta o estoque após cada saída, mantendo tudo correto.
    * Gerar relatório de produtos: Cria relatórios de vendas para ajudar no planejamento e reposição.

---

## 13. Cenários de uso (2 cenários completos)

### CENÁRIO 1 (Fluxo Principal)
1.  O gerente acessa o sistema de estoque com seu login e senha.
2.  O gerente seleciona a opção “Cadastrar Produto”.
3.  O gerente insere as informações do produto (nome, descrição, categoria, quantidade inicial e preço).
4.  O sistema gera automaticamente um ID único de identificação para o produto.
5.  O produto é salvo no sistema e passa a estar disponível para consulta.
6.  Quando ocorre uma venda ou retirada, o gerente acessa a opção “Registrar Saída”.
7.  O gerente informa o produto e a quantidade retirada.
8.  O sistema atualiza automaticamente a quantidade disponível em estoque.
9.  O sistema registra a movimentação no histórico para controle e auditoria.

### CENÁRIO 2 (Erro de operação)
1.  O gerente acessa o sistema de estoque com seu login e senha.
2.  O gerente seleciona a opção “Registrar Saída”.
3.  O gerente informa o produto e a quantidade desejada para retirada.
4.  O sistema verifica a quantidade disponível em estoque.
5.  O sistema identifica que a quantidade solicitada é maior do que a disponível.
6.  O sistema exibe uma mensagem de erro informando: “Estoque insuficiente para realizar a operação.”
7.  A saída não é registrada.
8.  O gerente pode corrigir a quantidade ou cancelar a operação.

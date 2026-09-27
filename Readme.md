# Modelagem de um sistema de gestão de informações para um restaurante

## Metadados

- **Nomes dos alunos e RGM**

- Diego Xavier Ribeiro 47793007
- Luiz Felipe de Brito Carvalho 47857714
- Nicolas Vieira de Lima 47212021
- Renan Caio de Lima  46915575


## 1. Caracterização da Organização

- **Nome e natureza da organização:** Ponto A – Restaurante e Pizzaria.

- **Contexto e porte:** A empresa possui uma equipe estimada entre 40 e 60 funcionários, atuando em diferentes setores e ambientes do estabelecimento. Sendo um resraurante com fins lucrativos e vendas
  
- **Problemas e necessidades identificados:** 
  Por ser um restaurante com grande fluxo de clientes, o Ponto A enfrenta períodos de alta demanda que ocasionam filas e dificuldades na organização do acesso aos ambientes. O Deck é um dos principais pontos de interesse dos clientes, mas a espera para acessá-lo pode ser longa, prejudicando a experiência e aumentando a sobrecarga dos funcionários responsáveis pelo controle. Dessa forma, existe a necessidade de uma solução que organize melhor o acesso aos ambientes, oferecendo maior previsibilidade aos clientes e facilitando o gerenciamento da capacidade do estabelecimento.

  Outro problema está relacionado ao controle de estoque, principalmente das bebidas. O sistema utilizado atualmente apresenta certa complexidade, dificultando o registro e a contagem precisa dos produtos retirados. Como consequência, os funcionários precisam realizar contagens manuais em algumas situações, aumentando a possibilidade de erros e divergências. Assim, uma solução mais simples e automatizada poderia facilitar o acompanhamento das saídas, reduzir processos manuais e melhorar a precisão das informações do estoque.

- **Justificativa da escolha:** 
  A escolha do Ponto A para o desenvolvimento do projeto ocorreu principalmente pela facilidade de acesso às informações e ao ambiente da empresa, já que um dos integrantes do grupo trabalha no estabelecimento e pode contribuir diretamente com o levantamento de dados e a compreensão dos processos internos. Essa proximidade permite identificar problemas reais enfrentados pela empresa e desenvolver uma solução baseada em necessidades concretas. Além disso, o Ponto A apresenta potencial para a aplicação de soluções tecnológicas que possam gerar valor para o negócio. O projeto também representa uma oportunidade para colocar em prática os conhecimentos adquiridos durante a formação acadêmica, ampliar a experiência profissional e desenvolver uma solução para um problema real. Futuramente, caso os resultados sejam positivos, a solução poderá ser aprimorada e adaptada para outros estabelecimentos do mesmo segmento.


- **Evidências da organização:** [Maps](https://maps.app.goo.gl/oVm8L7GaAggko4Ck9), [Site](https://ponto-a.cluvi.com.br), Contato: 01126722292, Endereço: Rua Dante Pellacani, 192 - Vila Reg. Feijó, São Paulo - SP, 03334-070

---

## 2. Processos de Negócio

**os processos de negócio mapeados cobrem toda a operação do restaurante, do momento em que o cliente entra até o encerramento do atendimento, e se organizam em cinco frentes principais.**

 - O primeiro processo mapeado é a identificação e cadastro de clientes, feito de forma física e não digital: na chegada, o cliente recebe uma pulseira numerada (de 1 a 9.999) que funciona como identificador único durante toda a visita, sendo então direcionado a uma mesa ou ambiente disponível — o documento já registra esse ponto como um gargalo, já que em horários de pico a organização do acesso aos ambientes (especialmente o Deck) gera filas e sobrecarrega os funcionários responsáveis pelo controle. A partir da identificação, o cliente consulta o cardápio pelo site do estabelecimento e realiza o pedido diretamente com o garçom, o que caracteriza o processo de emissão de pedidos: o garçom anota e registra o que foi solicitado, mantém a organização da mesa e do ambiente durante o atendimento e, ao final, recolhe a comanda, encaminhando o cliente ao caixa ou realizando a cobrança quando aplicável.

 - Uma vez emitido, o pedido segue para o processo de produção e distribuição, conduzido pelas áreas de bar, cozinha, pizza, sushi e lounge: cada setor recebe a comanda, identifica os itens que lhe cabem, prepara alimentos e bebidas, confere o resultado antes de liberar e entrega o pedido ao cliente. É também nessa etapa que ocorre o controle de estoque, hoje um dos pontos mais frágeis da operação — o acompanhamento da saída de bebidas depende de um sistema pouco intuitivo, o que obriga contagens manuais recorrentes e abre espaço para divergências e erros de registro, sem uma automatização que dê precisão ao processo.

 - O encerramento do atendimento fica a cargo do processo de controle financeiro e arrecadação, operado pelo caixa: a rotina inclui a abertura do caixa no início do expediente, o recebimento das pulseiras para dar baixa no sistema, o processamento dos pagamentos com conferência dos valores, eventuais sangrias e movimentações autorizadas, e o fechamento do caixa ao final do turno — é este processo que formalmente encerra a visita do cliente, associando a baixa da pulseira à quitação da comanda.

- Por fim, existe um processo transversal de gestão operacional, conduzido pela liderança (Meitree/gerente), que não atende diretamente o cliente mas dá suporte a todos os demais: acompanha o funcionamento geral da operação, reforça as áreas em momentos de maior demanda, identifica e ajuda a resolver problemas pontuais, realiza solicitações e pedidos de reposição de estoque e monitora a disponibilidade de produtos e materiais. O fluxo consolidado descrito no documento resume bem essa cadeia — Cliente → Recepção e identificação → Mesa → Pedido → Produção → Entrega → Finalização da comanda → Pagamento → Baixa da pulseira → Encerramento —, com a gestão operacional e o controle de estoque funcionando como processos de apoio contínuo às demais áreas, e não como etapas sequenciais do atendimento em si.


---

## 3. Requisitos do Sistema
  

### 3.1 Requisitos Funcionais
  
  ### **Separados por entidades**

  ### **Cliente**

* **RF01:** Permite acesso ao cardápio digital via QR Code na mesa.

* **RF02:** Identificação automática da mesa a partir do QR Code escaneado.

* **RF03:** Informação de alergias, restrições e preferências alimentares pelo cliente.

* **RF04:** Sugestão de pratos personalizados (Motor de Sugestão) baseada no perfil e restrições.

* **RF05:** Montagem de pré-pedido (escolha de pratos, quantidades e remoção de ingredientes).

* **RF06:** Inclusão de observações personalizadas aos itens do pedido.

* **RF07:** Envio do pré-pedido para validação e confirmação do garçom.

* **RF08:** Exibição detalhada de preço, descrição, imagem e categoria dos pratos.

* **RF09:** Sinalização de alerta para pratos/ingredientes incompatíveis com as restrições declaradas.

### **Garçom**

* **RF10:** Autenticação e login seguro (usuário, senha e token de sessão).

* **RF11:** Visualização de pré-pedidos recebidos em tempo real.

* **RF12:** Edição e ajuste de pré-pedidos antes do envio final.

* **RF13:** Confirmação do pré-pedido, convertendo-o em pedido confirmado.

* **RF14:** Recebimento de notificações em tempo real sobre novos pré-pedidos e alterações de status.

### **Cozinha**

* **RF15:** Painel de exibição para pedidos confirmados, contendo itens e observações.

* **RF16:** Notificações em tempo real ao receber novos pedidos para preparo.

* **RF17:** Atualização do status de preparo do pedido.

* **RF18:** Propagação automática de mudanças de status para garçons e clientes.

### **Administrador**

* **RF19:** Autenticação e login seguro para acesso ao painel de gestão.

* **RF20:** CRUD completo de pratos (cadastrar, editar e remover nome, descrição, preço, imagem, categoria e disponibilidade).

* **RF21:** Cadastro de ingredientes com alertas e marcadores de alérgenos (lactose, glúten, amendoim, frutos do mar, ovo, soja).

* **RF22:** Associação de ingredientes aos pratos, especificando quais podem ser removidos.

* **RF23:** Consulta a relatórios operacionais (pratos mais vendidos, tempo médio de atendimento).

* **RF24:** Geração e armazenamento de relatórios estruturados com tipo, data e dados associados.

### **Sistema / Geral**

* **RF25:** Geração e validação de tokens JWT para autenticação de garçons e administradores.

* **RF26:** Armazenamento e persistência de dados em banco de dados na nuvem.

* **RF27:** Atualização contínua do ciclo de status da mesa durante todo o atendimento.

---



### 3.2 Requisitos Não Funcionais

* **RNF01 (Segurança):** Comunicação entre clientes e API estritamente criptografada via HTTPS.

* **RNF02 (Segurança):** Armazenamento seguro de senhas utilizando algoritmos de *hash*.

* **RNF03 (Segurança):** Gerenciamento de sessões protegidas por tokens JWT com tempo de expiração.

* **RNF04 (Privacidade/LGPD):** Tratamento de dados sensíveis do cliente (alergias, dados pessoais) em conformidade com a LGPD.

* **RNF05 (Desempenho):** Notificações para garçom e cozinha em tempo real via WebSocket com baixa latência.

* **RNF06 (Desempenho):** Implementação de camada de *cache* para consultas frequentes (ex.: cardápio).

* **RNF07 (Usabilidade):** Interface responsiva no App do Cliente via navegador mobile, sem necessidade de instalação.

* **RNF08 (Usabilidade):** Painel Administrativo otimizado para navegação e uso em desktop.

* **RNF09 (Disponibilidade):** Garantia de alta disponibilidade da aplicação durante o horário de funcionamento do restaurante.

* **RNF10 (Escalabilidade):** Arquitetura preparada para suportar o crescimento do volume de mesas e acessos simultâneos.

* **RNF11 (Compatibilidade):** Suporte completo nos principais navegadores (Chrome, Safari, Firefox) em mobile, tablet e desktop.

* **RNF12 (Manutenibilidade):** Código back-end modularizado por domínios/serviços (cardápio, pedidos, autenticação, recomendação, relatórios).

* **RNF13 (Confiabilidade):** Garantia da integridade dos dados dos pedidos mesmo diante de instabilidades temporárias da rede.

---

## 4. Regras de Negócio

 
### 4.1 Regras operacionais
- Um cliente só pode entrar em um ambiente se houver capacidade disponível naquele momento; caso contrário, aguarda em fila até haver vaga. Toda entrada e toda saída de cliente em um ambiente deve ser registrada, para que a ocupação corrente seja sempre calculável.

- Nenhum produto pode ser entregue ao cliente sem estar previamente registrado em um pedido, e todo pedido cancelado também deve ser registrado, não apenas removido.

- Toda saída de bebida ou insumo do estoque deve gerar um registro que atualize a quantidade disponível do produto. Quando um produto atinge a quantidade mínima estabelecida, o sistema deve sinalizar o responsável pelo estoque. O estoque deve ser conferido periodicamente, e qualquer divergência entre o registrado e o existente fica registrada para apuração.

- Todo consumo do cliente deve estar vinculado a uma conta ou comanda aberta, e essa conta só pode ser fechada depois que todos os itens consumidos estiverem registrados nela. Cancelamentos e estornos de pedidos ou contas mantêm histórico — nunca são apagados.

### 4.2 Restrições organizacionais

- O atendimento só ocorre dentro do horário de funcionamento estabelecido pela casa. Áreas de uso exclusivo dos funcionários são proibidas para clientes, como política interna de segurança e organização do espaço.

- Cada funcionário só acessa as funções do sistema compatíveis com seu cargo. Alterações em uma conta já fechada só podem ser feitas por funcionário autorizado, e ficam registradas com autor e motivo, como exigência de auditoria interna.

- A venda e o consumo de bebida alcoólica seguem a legislação vigente, incluindo idade mínima e eventuais horários restritos — uma exigência legal externa, não uma política interna.

- É proibido retirar produtos do estabelecimento sem autorização e danificar equipamentos, móveis ou outros bens da casa, normas de conduta ligadas à responsabilidade patrimonial, não à integridade do banco de dados.

- Cada ambiente pode ter regras próprias de uso — por exemplo, restrição de idade em determinado horário ou código de vestimenta — que os clientes devem respeitar, como política interna variável por ambiente.

---

## 5. Dicionário de Dados Conceitual (Preliminar)

### 5.1 Modelo conceitual
 
Este modelo representa um restaurante operando com cardápio digital sincronizado: o cliente chega e é cadastrado na recepção, recebe uma comanda ou pulseira de controle de acesso e é associado a uma visita e a uma mesa. Na mesa, monta-se o pedido, que segue obrigatoriamente para validação de um garçom antes de chegar à cozinha; ao final da refeição, a conta é quitada e a comanda é baixada na catraca.
 
| Entidade | Relaciona-se com | Cardinalidade |
|---|---|---|
| CLIENTE | VISITA | N:N — um cliente participa de várias visitas ao longo do tempo, e uma visita pode reunir mais de um cliente (ex.: grupo na mesma mesa) |
| MESA | VISITA | N:N — uma mesa recebe várias visitas ao longo do tempo, e uma visita pode ocupar mais de uma mesa (ex.: mesas unidas para um grupo) |
| COMANDA_ACESSO | VISITA | 1:1 — toda comanda/pulseira identifica exatamente uma visita, toda visita está vinculada a uma única comanda |
| VISITA | PEDIDO | 1:N — uma visita gera vários pedidos ao longo do atendimento |
| FUNCIONARIO | PEDIDO | 1:N — um funcionário (papel garçom) atende vários pedidos |
| PEDIDO | PRATO | N:N — um pedido reúne vários pratos, e um prato aparece em vários pedidos ao longo do tempo |
| CATEGORIA_PRATO | PRATO | N:N — uma categoria classifica vários pratos, e um prato pode pertencer a mais de uma categoria |
| VISITA | PAGAMENTO | 1:N — uma visita é quitada por um ou mais pagamentos (permite divisão de conta) |
| FUNCIONARIO | PAGAMENTO | N:N — um funcionário arrecada vários pagamentos, e o diagrama admite mais de um funcionário por pagamento |
 
Diferente da versão anterior deste dicionário, quatro relacionamentos passaram a N:N — REALIZA (Cliente×Visita), RECEBE (Mesa×Visita), CONTEM (Pedido×Prato) e CLASSIFICA (Categoria×Prato) —, e um quinto, ARRECADA (Funcionário×Pagamento), também passou a N:N. Em Entidade-Relacionamento, um relacionamento N:N não pode ser implementado como uma simples chave estrangeira: exige uma entidade associativa na modelagem lógica. Este diagrama ainda não explicita essas entidades — cabe à próxima etapa de projeto (modelo lógico) introduzi-las, por exemplo: VISITA_CLIENTE, VISITA_MESA, PEDIDO_PRATO (retomando o papel que ITEM_PEDIDO cumpria na versão anterior, inclusive para registrar quantidade e preço praticado) e PRATO_CATEGORIA. O relacionamento RECEPCIONA (Funcionário×Visita), presente na versão anterior, não aparece mais neste diagrama.
 
 ---

- **Cliente** é a pessoa física atendida pelo restaurante, identificada por CPF.
 
- **Mesa** é o posto físico de atendimento do salão, identificado por número.
 
- **Comanda/pulseira de acesso** é o meio físico de controle de entrada e saída emitido pela recepção, independente do conteúdo do pedido.
 
- **Visita** é o evento de sessão de atendimento, do check-in ao pagamento, associado a cliente(s), mesa(s) e a uma comanda.
 
- **Funcionário** é a pessoa que opera o sistema em algum papel — garçom, caixa, ou outro indicado por TP_CARGO.
 
- **Categoria de prato** é o agrupamento do cardápio (entrada, principal, sobremesa, bebida, drink).
 
- **Prato** é o item do cardápio, com preço e descrição.
 
- **Pedido** é o conjunto de itens solicitados numa visita, sujeito à validação obrigatória do garçom antes de seguir à cozinha.
 
- **Pagamento** é o evento de quitação, total ou parcial, de uma visita.
 
---

### 5.2 Fluxo de dados (visão de DFD)
 
Cliente(s) chegam à recepção → cadastro/atualização em CLIENTE e emissão da COMANDA_ACESSO, com abertura de VISITA — associada a um ou mais CLIENTEs e a uma ou mais MESAs, conforme a cardinalidade N:N do diagrama atualizado → os clientes montam o pedido no cardápio digital, gerando um registro em PEDIDO associado a um ou mais PRATOs → o pedido só avança para a cozinha após confirmação de um FUNCIONARIO no papel de garçom, regra de negócio central do sistema → ao final da refeição, a VISITA é quitada por um ou mais registros de PAGAMENTO → a confirmação do pagamento libera a COMANDA_ACESSO para a passagem pela catraca, encerrando a VISITA.

---

### 5.3 Convenções do dicionário
 
**SGBD:** MySQL 8, mecanismo de armazenamento InnoDB — cuida da persistência dos arquivos de dados, do log de transações (redo/undo) e mantém o índice primário clusterizado por chave.
 
**Codificação de caracteres:** utf8mb4 com collation utf8mb4_0900_ai_ci. Escolhida em vez de latin1 por cobrir acentuação do português sem perda em campos de nome e texto livre.
 
**Notação formal** (símbolos usados neste dicionário):
 
| Símbolo | Significado |
|---|---|
| `=` | é composto de |
| `+` | e (conecta elementos obrigatórios) |
| `( )` | opcional |
| `{ }`, `n{ }m` | iteração, com limite mínimo n e máximo m |
| `[ \| ]` | escolha obrigatória entre alternativas |
| `/ /` | rótulo de um grupo repetitivo |
| `@` | identificador (chave primária) |
| `* *` | comentário, fora da estrutura formal |
 
**Prefixos:** NM_ nome, DT_ data, ID_ identificador (não sofre operação matemática), CD_ código de domínio, QT_ quantidade, TP_ tipo (categorização), IN_ indicador booleano. Este dicionário também usa DS_ (descrição/texto livre) e VL_ (valor monetário) — extensões ao mesmo princípio, tornando explícito no nome do atributo o tipo de dado que ele representa.
 
**Versão deste dicionário:** v2.0, 26/setembro/2026 — atualizado a partir do modelo conceitual BRModelo Web de 24/09/2026. Qualquer alteração de estrutura deve gerar nova revisão registrada nesta seção.
 
---

### 5.4 Dicionário de dados por entidade
 
### 5.5 CLIENTE
 
```
CLIENTE = @ID_CLIENTE + NM_CLIENTE + ID_CPF + DT_NASCIMENTO + DS_TELEFONE
```
 
**Leitura:** @ID_CLIENTE é o identificador único; ID_CPF usa o prefixo de identificador porque é um documento emitido por órgão externo, não um código interno de domínio — mesmo raciocínio do ID_CRM no estudo de caso de referência. No diagrama atualizado, REALIZA passou a ser N:N: CLIENTE não referencia VISITA diretamente por atributo — a associação entre um cliente e cada visita de que participa será resolvida por uma entidade própria na modelagem lógica (ex.: VISITA_CLIENTE).
 
| Atributo | Tipo físico | Obrigatório | Significado e relevância |
|---|---|---|---|
| ID_CLIENTE (id_cliente) | integer | Sim (PK) | Código de localização do registro do cliente; não sofre operação matemática. |
| NM_CLIENTE (nome) | varchar(160) | Sim | Nome completo; identifica o cliente na comanda e no histórico de pedidos. |
| ID_CPF (cpf) | varchar(14) | Sim (único) | Documento de identificação civil; usado pela recepção para localizar cliente recorrente. |
| DT_NASCIMENTO (data_nasc) | date | Sim | Data de nascimento; suporta verificação em itens com restrição de idade. |
| DS_TELEFONE (telefone) | varchar(20) | Sim | Telefone de contato usado pela recepção. |
 
**Índices:** PK ID_CLIENTE (clusterizado); índice único em ID_CPF (busca de cliente recorrente na recepção).
 
---

### 5.6 MESA
 
```
MESA = @ID_MESA + ID_NUMERO_MESA
```
 
**Leitura:** ID_NUMERO_MESA recebe o prefixo de identificador — e não CD_ — porque é um rótulo físico da mesa, não uma classificação de domínio. No diagrama atualizado, RECEBE passou a ser N:N: além de uma mesa atender várias visitas ao longo do tempo (já esperado), o modelo também admite que uma única visita ocupe mais de uma mesa — cenário de mesas unidas para um grupo maior. Essa associação, em ambos os sentidos, será resolvida por entidade própria na modelagem lógica (ex.: VISITA_MESA).
 
| Atributo | Tipo físico | Obrigatório | Significado e relevância |
|---|---|---|---|
| ID_MESA (id_mesa) | integer | Sim (PK) | Identificador da mesa. |
| ID_NUMERO_MESA (numero) | integer | Sim (único) | Número físico impresso na mesa; usado pela recepção e pelo garçom. |
 
**Índices:** PK ID_MESA; índice único em ID_NUMERO_MESA.
 
---

### 5.7 COMANDA_ACESSO
 
```
COMANDA_ACESSO = @ID_COMANDA + ID_CODIGO_ACESSO
```
 
**Leitura:** ID_CODIGO_ACESSO é o código impresso/gravado na comanda ou pulseira, conferido pela segurança na saída; por ser um identificador físico emitido pelo próprio sistema — não um dado descritivo — recebe o prefixo ID_, e não DS_. A relação com VISITA permanece 1:1 nesta versão do diagrama, inalterada em relação à anterior.
 
| Atributo | Tipo físico | Obrigatório | Significado e relevância |
|---|---|---|---|
| ID_COMANDA (id_comanda) | integer | Sim (PK) | Identificador da comanda/pulseira. |
| ID_CODIGO_ACESSO (codigo) | varchar(64) | Sim (único) | Código impresso/gravado na comanda ou pulseira; conferido pela segurança na saída. |
 
**Índices:** PK ID_COMANDA; índice único em ID_CODIGO_ACESSO (conferência rápida na saída).
 
---

### 5.8 VISITA
 
```
VISITA = @ID_VISITA + ID_COMANDA + DT_CHEGADA + (DT_SAIDA) + TP_STATUS_VISITA
```
 
**Leitura:** ID_COMANDA é obrigatório e único, o que garante o 1:1 com COMANDA_ACESSO — mesmo raciocínio do ID_PACIENTE único em PRONTUARIO no estudo de caso de referência. (DT_SAIDA) é opcional porque a visita permanece aberta até o encerramento. Diferente da versão anterior deste dicionário, VISITA não carrega mais ID_CLIENTE nem ID_FUNCIONARIO como atributos próprios: REALIZA e RECEBE tornaram-se N:N no diagrama atualizado, e o relacionamento RECEPCIONA (que ligava VISITA a FUNCIONARIO) não aparece mais — o check-in deixou de ser modelado como uma associação formal nesta versão.
 
| Atributo | Tipo físico | Obrigatório | Significado e relevância |
|---|---|---|---|
| ID_VISITA (id_visita) | integer | Sim (PK) | Identificador da visita. |
| ID_COMANDA (id_comanda) | integer | Sim (FK, único) | Comanda/pulseira vinculada; a unicidade garante o 1:1 entre visita e comanda. |
| DT_CHEGADA (hora_chegada) | datetime | Sim | Instante de check-in na recepção. |
| DT_SAIDA (hora_saida) | datetime | Não | Instante de encerramento da visita; ausente enquanto a mesa está em atendimento. |
| TP_STATUS_VISITA (status) | varchar(30) | Sim | Situação corrente: aberta, fechada. |
 
**Índices:** PK ID_VISITA; índice único em ID_COMANDA (garante o 1:1).
 
---

### 5.9 FUNCIONARIO
 
```
FUNCIONARIO = @ID_FUNCIONARIO + NM_FUNCIONARIO + TP_CARGO
```
 
**Leitura:** TP_CARGO é uma categorização (recepcionista, garçom, barman, cozinheiro, caixa, administrador, segurança) e por isso recebe o prefixo TP_, e não CD_. No diagrama atualizado, FUNCIONARIO relaciona-se apenas com PEDIDO (atende) e PAGAMENTO (arrecada); o relacionamento com VISITA (recepciona) não está mais representado, de modo que o papel de recepcionista, embora previsto em TP_CARGO, não tem hoje um relacionamento formal correspondente no modelo.
 
| Atributo | Tipo físico | Obrigatório | Significado e relevância |
|---|---|---|---|
| ID_FUNCIONARIO (id_func) | integer | Sim (PK) | Identificador do funcionário. |
| NM_FUNCIONARIO (nome) | varchar(160) | Sim | Nome completo do funcionário. |
| TP_CARGO (cargo) | varchar(40) | Sim | Papel exercido no sistema; determina as telas e ações disponíveis a esse funcionário. |
 
**Índices:** PK ID_FUNCIONARIO.
 
---

### 5.10 CATEGORIA_PRATO
 
```
CATEGORIA_PRATO = @ID_CATEGORIA + NM_CATEGORIA
```
 
**Leitura:** Entidade de domínio simples. No diagrama atualizado, CLASSIFICA passou a ser N:N: um prato pode pertencer a mais de uma categoria (ex.: um prato ao mesmo tempo "principal" e "vegano"), o que exigirá entidade própria na modelagem lógica (ex.: PRATO_CATEGORIA) — antes, PRATO referenciava uma única categoria por atributo direto.
 
| Atributo | Tipo físico | Obrigatório | Significado e relevância |
|---|---|---|---|
| ID_CATEGORIA (id_categ) | integer | Sim (PK) | Identificador da categoria. |
| NM_CATEGORIA (nome) | varchar(60) | Sim | Nome da categoria do cardápio: entrada, principal, sobremesa, bebida, drink. |
 
**Índices:** PK ID_CATEGORIA.
 
---

### 5.11 PRATO
 
```
PRATO = @ID_PRATO + NM_PRATO + DS_DESCRICAO + VL_PRECO + (DS_IMAGEM_URL) + TP_STATUS_PRATO + IN_REQUER_BARMAN
```
 
**Leitura:** VL_ é um prefixo introduzido neste dicionário para valores monetários, pelo mesmo princípio que justificou a introdução de DS_ no estudo de caso de referência (ver §3). PRATO deixou de referenciar ID_CATEGORIA como atributo direto, já que CLASSIFICA agora é N:N (ver leitura de CATEGORIA_PRATO). Da mesma forma, PRATO não referencia PEDIDO por atributo: CONTEM também é N:N e a antiga entidade associativa ITEM_PEDIDO — que registrava quantidade e preço praticado no momento — não está mais representada neste diagrama; sem ela, essas duas informações não têm hoje onde ser armazenadas por pedido.
 
| Atributo | Tipo físico | Obrigatório | Significado e relevância |
|---|---|---|---|
| ID_PRATO (id_prato) | integer | Sim (PK) | Identificador do prato. |
| NM_PRATO (nome) | varchar(160) | Sim | Nome do prato exibido no cardápio. |
| DS_DESCRICAO (descricao) | text | Sim | Composição do prato exibida ao cliente no cardápio digital. |
| VL_PRECO (preco) | decimal(10,2) | Sim | Preço de venda vigente do prato. |
| DS_IMAGEM_URL (imagem_url) | varchar(255) | Não | Endereço da foto do prato exibida no cardápio. |
| TP_STATUS_PRATO (status) | varchar(30) | Sim | Situação corrente: ativo, esgotado, inativo. |
| IN_REQUER_BARMAN (requer_barman) | boolean | Sim | Indica se o preparo do item deve passar pelo barman (tipicamente drinks) em vez da cozinha. |
 
**Índices:** PK ID_PRATO.
 
---

### 5.12 PEDIDO
 
```
PEDIDO = @ID_PEDIDO + ID_VISITA + TP_STATUS_PEDIDO + DT_CRIACAO + (DT_CONFIRMACAO) + (DT_ENVIO_COZINHA) + (DT_PRONTO) + (DT_ENTREGA) + ID_FUNCIONARIO
```
 
**Leitura:** Os quatro campos de data entre ( ) são preenchidos progressivamente conforme o pedido avança de status. ID_VISITA e ID_FUNCIONARIO permanecem atributos diretos porque GERA e ATENDE continuam 1:N nesta versão do diagrama (pedido no lado "1" de cada relação). PEDIDO não referencia PRATO por atributo, pois CONTEM é N:N (ver leitura de PRATO).
 
| Atributo | Tipo físico | Obrigatório | Significado e relevância |
|---|---|---|---|
| ID_PEDIDO (id_pedido) | integer | Sim (PK) | Identificador do pedido. |
| ID_VISITA (id_visita) | integer | Sim (FK) | Visita à qual o pedido pertence. |
| TP_STATUS_PEDIDO (status) | varchar(40) | Sim | rascunho, enviado ao garçom, confirmado pelo garçom, enviado à cozinha, em preparo, pronto, entregue ou cancelado. |
| DT_CRIACAO (hora_criacao) | datetime | Sim | Instante de criação do pedido pelo cliente. |
| DT_CONFIRMACAO (hora_confirmacao) | datetime | Não | Instante em que o garçom confirmou o pedido junto ao cliente. |
| DT_ENVIO_COZINHA (hora_envio_cozinha) | datetime | Não | Instante de envio à cozinha. |
| DT_PRONTO (hora_pronto) | datetime | Não | Instante em que a cozinha concluiu o preparo. |
| DT_ENTREGA (hora_entrega) | datetime | Não | Instante de entrega do pedido ao cliente. |
| ID_FUNCIONARIO (id_func) | integer | Sim (FK) | Garçom responsável pela validação e confirmação do pedido. |
 
**Índices:** PK ID_PEDIDO; índice em ID_VISITA (comanda corrente da mesa); índice em ID_FUNCIONARIO (fila de atendimento por garçom).
 
---

### 5.13 PAGAMENTO
 
```
PAGAMENTO = @ID_PAGAMENTO + ID_VISITA + VL_TOTAL + [TP_DINHEIRO | TP_CREDITO | TP_DEBITO | TP_PIX | TP_VALE] + [TP_LOCAL_MESA | TP_LOCAL_CAIXA] + DT_PAGAMENTO + QT_PERCENTUAL_SERVICO + TP_STATUS_PAGAMENTO
```
 
**Leitura:** Os dois grupos entre [ | ] exigem escolher exatamente uma alternativa cada, no mesmo espírito do [TP_MASC | TP_FEM | TP_INT] do estudo de caso de referência. ID_VISITA permanece atributo direto porque QUITA continua 1:N (pagamento no lado "1"). ARRECADA, porém, passou a N:N: PAGAMENTO não referencia mais ID_FUNCIONARIO por atributo, e o modelo passa a admitir, ao menos formalmente, mais de um funcionário por pagamento — situação atípica na operação real (um pagamento tem um único recebedor); recomenda-se revisar essa cardinalidade caso não seja intencional, revertendo-a para 1:N como na versão anterior deste dicionário.
 
| Atributo | Tipo físico | Obrigatório | Significado e relevância |
|---|---|---|---|
| ID_PAGAMENTO (id_pgto) | integer | Sim (PK) | Identificador do pagamento. |
| ID_VISITA (id_visita) | integer | Sim (FK) | Visita quitada por este pagamento. |
| VL_TOTAL (valor_total) | decimal(10,2) | Sim | Valor total quitado neste pagamento. |
| TP_DINHEIRO \| TP_CREDITO \| TP_DEBITO \| TP_PIX \| TP_VALE (forma_pagamento) | varchar(30) | Sim (escolha) | Forma de quitação utilizada. |
| TP_LOCAL_MESA \| TP_LOCAL_CAIXA (local) | varchar(40) | Sim (escolha) | Local onde o pagamento foi recebido: na mesa (pelo garçom) ou no caixa. |
| DT_PAGAMENTO (hora_pagamento) | datetime | Sim | Instante em que o pagamento foi recebido. |
| QT_PERCENTUAL_SERVICO (percentual_servico) | decimal(5,2) | Sim | Percentual de taxa de serviço aplicado sobre o subtotal da comanda. |
| TP_STATUS_PAGAMENTO (status) | varchar(30) | Sim | confirmado ou estornado. |
 
**Índices:** PK ID_PAGAMENTO; índice em ID_VISITA (suporta divisão de conta, com múltiplos pagamentos por visita).

---
 
### 5.14 Acesso e conformidade com a LGPD
 
Neste recorte do modelo, CLIENTE concentra o único dado pessoal do sistema — nome, CPF, data de nascimento e telefone —, classificado como dado pessoal comum (LGPD, art. 5º, I), tratado com base na execução do contrato de prestação do serviço (art. 7º, V). Restrições e alergias alimentares, quando existentes no sistema completo, envolvem dado de saúde (art. 5º, II) e seguem base legal e controles de acesso próprios, não detalhados neste recorte.
 
Leitura, inserção e atualização de CLIENTE ficam restritas à recepção e à auditoria; exclusão física não é uma operação disponível a nenhum papel — o cadastro é apenas inativado, preservando o histórico de visitas, pedidos e pagamentos vinculados.

---

## 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)

[Modelo conceitual](modeloConceitual.html)

---

## 7. Diagrama Entidade-Relacionamento (DER)


[DER](DER.pdf)

---

## 8. Justificativa Técnica

- O diagrama tem nove entidades porque cada uma passa no teste de existência independente: Cliente, Mesa e Comanda_Acesso ficam separadas de Visita porque cada uma muda por razão própria (cliente existe fora de qualquer visita, mesa existe vazia, comanda tem ciclo próprio de emissão/baixa), e Funcionário é uma única caixa com a bolinha cargo em vez de virar Garçom/Caixa/Recepcionista, já que todos os papéis compartilham os mesmos atributos e losangos.

- Nas cardinalidades, cada par (1,n)/(1,1) reflete uma leitura direta do negócio. comanda_acesso (1,1)-(1,1) visita trava que uma comanda nunca cobre duas sessões ao mesmo tempo. visita (1,n)-(1,1) pedido e visita (1,n)-(1,1) pagamento capturam múltiplas rodadas de pedido e divisão de conta. Funcionario (1,n)-(1,1) atende pedido expressa que cada pedido tem um garçom responsável. Os relacionamentos N:N — Cliente-Realiza-visita, Mesa-Recebe-visita, categoria_prato-classifica-prato e Funcionario-arrecada-pagamento — cobrem os casos reais em que mais de uma ocorrência de cada lado participa ao mesmo tempo: grupos que dividem mesa, mesas unidas para atendimentos maiores, pratos que pertencem a mais de uma categoria do cardápio, e pagamentos com mais de um funcionário envolvido no recebimento.

- Por fim, contem liga pedido direto a prato como N:N sem nenhuma bolinha própria — a associação entre os dois é representada só pela relação em si, cobrindo quais pratos compõem quais pedidos sem introduzir uma entidade extra no diagrama conceitual.
---

## 9. Uso de Inteligência Artificial   


**Não Utilizamos IA**


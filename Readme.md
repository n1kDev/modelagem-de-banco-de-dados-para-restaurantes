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


- **Evidências da organização:** 

- [Foto](FotoDoEstabelecimento.jpeg)
- [Maps](https://maps.app.goo.gl/oVm8L7GaAggko4Ck9) 
- [Site](https://ponto-a.cluvi.com.br)
- Contato: 01126722292
- Endereço: Rua Dante Pellacani, 192 - Vila Reg. Feijó, São Paulo - SP, 03334-070

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

[dicionario_dados](dicionario_dados.html)

---

## 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)
 
### Entidades reconhecidas
 
O modelo reconhece nove entidades. Cada uma foi separada das demais porque tem identidade própria e existe independentemente de uma visita específica.
 
| Entidade | Justificativa |
|---|---|
| **CLIENTE** | Pessoa física atendida pelo restaurante. Precisa de identificação própria (CPF), pois existe antes e depois de qualquer visita e pode voltar outras vezes. |
| **MESA** | Posto de atendimento do salão. Existe e é numerada mesmo vazia, e é reaproveitada por várias visitas ao longo do dia. |
| **COMANDA_ACESSO** | Pulseira numerada (de 1 a 9.999) entregue na chegada, que identifica o cliente durante a visita e é baixada no caixa. Tem ciclo de vida próprio (entrega, uso, baixa), independente do que foi consumido. |
| **VISITA** | Evento de atendimento, da chegada ao encerramento da conta. É o eixo do modelo: liga cliente(s), mesa(s) e comanda, e dela derivam os pedidos e os pagamentos. |
| **FUNCIONARIO** | Pessoa que opera o sistema em alguma função (garçom, caixa, produção ou gerência). Suas ações precisam de um responsável identificado. |
| **CATEGORIA_PRATO** | Agrupamento do cardápio (ex.: pizzas, culinária japonesa, pratos tradicionais, bebidas). Organiza os pratos sem depender de nenhum prato específico. |
| **PRATO** | Item do cardápio, alimento ou bebida. Tem preço próprio e existe mesmo antes de ser pedido. |
| **PEDIDO** | Conjunto de pratos solicitados numa visita. Tem ciclo próprio (registrado, em preparo, pronto, entregue ou cancelado), e uma visita pode ter vários pedidos. |
| **PAGAMENTO** | Quitação, total ou parcial, da conta de uma visita. Pode haver mais de um por visita (divisão de conta). |
 
### Atributos e classificações
 
Classificações usadas: **identificador** (chave primária), **identificador natural** (código usado no dia a dia, com regra de unicidade), **descritivo**, **data**, **monetário** e **domínio fechado** (conjunto fixo de valores possíveis).
 
| Entidade | Atributo | Classificação |
|---|---|---|
| CLIENTE | `id_cliente` | Identificador (chave primária) |
| CLIENTE | `nome` | Descritivo, obrigatório |
| CLIENTE | `CPF` | Identificador natural, obrigatório e único |
| CLIENTE | `data_nasc` | Data, obrigatório |
| CLIENTE | `telefone` | Descritivo (contato), obrigatório |
| MESA | `id_mesa` | Identificador (chave primária) |
| MESA | `Numero` | Identificador natural, obrigatório e único |
| COMANDA_ACESSO | `id_comanda` | Identificador (chave primária) |
| COMANDA_ACESSO | `codigo` | Identificador natural, valor de 1 a 9.999, único entre as comandas em uso |
| VISITA | `id_visita` | Identificador (chave primária) |
| VISITA | `status` | Domínio fechado: aberta ou fechada |
| FUNCIONARIO | `id_func` | Identificador (chave primária) |
| FUNCIONARIO | `cargo` | Domínio fechado: garçom, caixa, produção ou gerente |
| CATEGORIA_PRATO | `id_categ` | Identificador (chave primária) |
| CATEGORIA_PRATO | `nome` | Descritivo, obrigatório e único |
| PRATO | `id_prato` | Identificador (chave primária) |
| PRATO | `preco` | Monetário, obrigatório e maior que zero |
| PEDIDO | `id_pedido` | Identificador (chave primária) |
| PEDIDO | `status` | Domínio fechado: registrado, em preparo, pronto, entregue ou cancelado |
| PAGAMENTO | `id_pgto` | Identificador (chave primária) |
| PAGAMENTO | `valor_total` | Monetário, obrigatório e maior que zero |
 
### Relacionamentos pertinentes
 
| Relacionamento | Entidades | Cardinalidade | Como as entidades se conectam |
|---|---|---|---|
| **Realiza** | CLIENTE – VISITA | N:N | Um cliente participa de várias visitas ao longo do tempo, e uma visita pode reunir mais de um cliente (ex.: grupo na mesma mesa). |
| **Recebe** | MESA – VISITA | N:N | Uma mesa recebe várias visitas ao longo do tempo, e uma visita pode ocupar mais de uma mesa. |
| **Identifica** | COMANDA_ACESSO – VISITA | 1:1 | Cada comanda em uso identifica uma única visita, e cada visita tem uma única comanda. |
| **Gera** | VISITA – PEDIDO | 1:N | Uma visita gera vários pedidos ao longo do atendimento, e cada pedido pertence a uma única visita. |
| **Atende** | FUNCIONARIO – PEDIDO | 1:N | Um funcionário atende vários pedidos, e cada pedido é atendido por um único funcionário. |
| **Contém** | PEDIDO – PRATO | N:N | Um pedido reúne vários pratos, e um prato aparece em vários pedidos ao longo do tempo. |
| **Classifica** | CATEGORIA_PRATO – PRATO | N:N | Uma categoria classifica vários pratos, e um prato pode pertencer a mais de uma categoria. |
| **Quita** | VISITA – PAGAMENTO | 1:N | Uma visita é quitada por um ou mais pagamentos (divisão de conta), e cada pagamento pertence a uma única visita. |
| **Arrecada** | FUNCIONARIO – PAGAMENTO | N:N | Um funcionário arrecada vários pagamentos, e um pagamento pode envolver mais de um funcionário (ex.: o garçom realiza a cobrança e o caixa finaliza). |
 
### Restrições e políticas organizacionais aplicadas ao modelo
 
**Regras operacionais refletidas no modelo**
 
| Regra operacional | Como aparece no modelo |
|---|---|
| Nenhum produto é entregue ao cliente sem estar registrado em um pedido. | Todo prato servido chega ao cliente por meio de um PEDIDO, pelo relacionamento Contém. |
| Pedidos cancelados são registrados, não removidos. | O `status` de PEDIDO inclui "cancelado"; o pedido permanece no banco. |
| Todo consumo está vinculado a uma conta (visita) aberta, e a conta só é encerrada depois que os itens consumidos estão registrados. | Os relacionamentos Gera e Quita ligam pedidos e pagamentos à VISITA; o `status` da visita só passa a "fechada" após o registro dos itens e a quitação. |
| Cancelamentos e estornos mantêm histórico. | Nenhum papel apaga registros de PEDIDO ou PAGAMENTO; as ocorrências ficam no log de auditoria. |
| Cada comanda em uso pertence a uma única visita, e a baixa da pulseira encerra o atendimento. | Relacionamento Identifica (1:1) e atributo `codigo` único entre as comandas em uso. |
 
**Restrições organizacionais refletidas no modelo**
 
| Restrição ou política | Natureza | Como aparece no modelo |
|---|---|---|
| Cada funcionário só acessa as funções do sistema compatíveis com seu cargo. | Política interna de acesso | O atributo `cargo` (domínio fechado) define as permissões de cada funcionário. |
| Alterações em conta já fechada só por funcionário autorizado, com registro de autor e motivo. | Auditoria interna | Restrição sobre PAGAMENTO, aplicada por permissão de acesso e registrada no log de auditoria do SGBD. |
| A venda e o consumo de bebida alcoólica seguem a legislação vigente. | Exigência legal | O atributo `data_nasc` de CLIENTE permite verificar a idade mínima. |
| Os dados pessoais dos clientes seguem a LGPD. | Exigência legal | CLIENTE concentra os dados pessoais (nome, CPF, data de nascimento e telefone); a exclusão física não é permitida, apenas a anonimização ao fim da retenção. |
 
**Regras reconhecidas na organização e deixadas para as próximas etapas**
 
Nesta primeira etapa o modelo cobre o fluxo de atendimento, do cliente que chega até o pagamento. As regras abaixo foram levantadas na organização, mas dependem de entidades que ainda não fazem parte do DER, e serão tratadas quando o modelo for ampliado:
 
- **Controle de acesso aos ambientes:** capacidade máxima de cada ambiente, fila de espera quando o ambiente está lotado, registro de entrada e saída e regras específicas de cada ambiente.
- **Controle de estoque de bebidas:** registro de toda saída, atualização da quantidade disponível, aviso de estoque mínimo e conferência periódica com registro das divergências.
- **Horário de funcionamento e áreas restritas aos funcionários:** políticas da casa que orientam a operação, sem dado próprio a registrar nesta etapa.
- **Normas de conduta** (não retirar produtos sem autorização, não danificar o patrimônio): regras de convivência que não alteram a estrutura do banco de dados.



---

## 7. Diagrama Entidade-Relacionamento (DER)


[DER](DER.jpg)

---

## 8. Justificativa Técnica

- O diagrama tem nove entidades porque cada uma passa no teste de existência independente: Cliente, Mesa e Comanda_Acesso ficam separadas de Visita porque cada uma muda por razão própria (cliente existe fora de qualquer visita, mesa existe vazia, comanda tem ciclo próprio de emissão/baixa), e Funcionário é uma única caixa com a bolinha cargo em vez de virar Garçom/Caixa/Recepcionista, já que todos os papéis compartilham os mesmos atributos e losangos.

- Nas cardinalidades, cada par (1,n)/(1,1) reflete uma leitura direta do negócio. comanda_acesso (1,1)-(1,1) visita trava que uma comanda nunca cobre duas sessões ao mesmo tempo. visita (1,n)-(1,1) pedido e visita (1,n)-(1,1) pagamento capturam múltiplas rodadas de pedido e divisão de conta. Funcionario (1,n)-(1,1) atende pedido expressa que cada pedido tem um garçom responsável. Os relacionamentos N:N — Cliente-Realiza-visita, Mesa-Recebe-visita, categoria_prato-classifica-prato e Funcionario-arrecada-pagamento — cobrem os casos reais em que mais de uma ocorrência de cada lado participa ao mesmo tempo: grupos que dividem mesa, mesas unidas para atendimentos maiores, pratos que pertencem a mais de uma categoria do cardápio, e pagamentos com mais de um funcionário envolvido no recebimento.

- Por fim, contem liga pedido direto a prato como N:N sem nenhuma bolinha própria — a associação entre os dois é representada só pela relação em si, cobrindo quais pratos compõem quais pedidos sem introduzir uma entidade extra no diagrama conceitual.
---

## 9. Uso de Inteligência Artificial   


**Não Utilizamos IA**


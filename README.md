# Desafio Github Markdown | DIO

Este repositório apresenta uma visão objetiva dos principais conceitos relacionados à Arquitetura de Software, reunindo fundamentos essenciais para quem está iniciando no desenvolvimento de sistemas. O conteúdo foi estruturado para servir como base de estudo e como referência para futuros projetos.

# Fundamentos de Arquitetura de Software

## Objetivo

Fornecer um material conciso e bem organizado sobre os modelos arquiteturais mais utilizados, seus propósitos e como contribuem para aplicações mais estáveis, escaláveis e fáceis de manter.
___

## Introdução à Arquitetura de Software

A Arquitetura de Software é a estrutura fundamental de um sistema, formada por seus componentes principais, a forma como eles interagem e as diretrizes que orientam sua construção. Ela define a organização do software em um nível mais alto do que o código, funcionando como o “projeto arquitetônico” de uma aplicação.

### 1. Arquitetura

A arquitetura determina se um sistema será sustentável ou um problema futuro. Algumas vantagens são:

- Evolução do sistema sem grandes retrabalhos.

- Facilidade de manutenção e legibilidade.

- Distribuição clara de responsabilidades.

- Redução de riscos e aumento da confiabilidade.

- Escalabilidade horizontal ou vertical conforme o crescimento do sistema.

### 2. Principais Modelos Arquiteturais

#### 2.1 Monolito

O monolito é um modelo em que toda a aplicação funciona como uma única unidade. Seus benefícios são:

- Mais simples para iniciar.

- Fácil de implantar (um único artefato).

- Menos complexidade técnica inicial.

Pontos de atenção:

- Pode se tornar difícil de escalar à medida que cresce.

- Deploys mais arriscados (tudo ou nada).

- Código tende a se acoplar com facilidade se não houver disciplina.

- Ideal para: aplicações pequenas ou equipes reduzidas.


#### 2.2 Arquitetura em Camadas (Layered Architecture)

Um dos modelos mais tradicionais do mercado. Organiza o sistema em camadas com responsabilidades específicas. Cada camada interage apenas com a imediatamente abaixo dela sendo ideal para sistemas corporativos, CRUDs, back-ends iniciantes e intermediários. Por exemplo:

1. Apresentação → onde ficam interfaces e controle de entrada.

2. Aplicação → orquestra o fluxo da aplicação.

3. Domínio → regras de negócio puras.

4. Infraestrutura/Dados → persistência, comunicações externas.

Vantagens:

- Código mais organizado.

- Separação clara de responsabilidades.

- Fácil manutenção inicial.

Desvantagens:

- Pode virar um monolito organizado demais (mas ainda monolito).

- Pode gerar dependências rígidas entre camadas.

#### 2.3 MVC (Model–View–Controller)

Padrão muito usado em aplicações web.

- Model: regras de negócio + dados.

- View: a interface (HTML, JSON, templates).

- Controller: recebe as requisições e decide o que fazer.

Vantagens:

- Organização clara de responsabilidades.

- Boa separação entre apresentação e lógica.

- Muito utilizado, fácil de encontrar suporte e bibliotecas.

Desvantagens:

- Em projetos maiores, “Controllers gordos” são comuns.

- Pode não ser suficiente para sistemas complexos sozinho.

- Ideal para: aplicações web e APIs de médio porte.

#### 2.4 Microserviços

Modelo onde a aplicação é dividida em vários serviços pequenos, independentes, cada um responsável por um domínio específico. Ideal para grandes sistemas, alto volume de usuários e equipes experientes.

Vantagens:

- Escalabilidade individual por serviço.

- Maior resiliência: falha isolada.

- Deploys independentes.

- Times trabalhando de forma autônoma.

Desvantagens:

- Mais complexidade (monitoramento, logs, rede).

- Requer maturidade da equipe.

- Comunicação entre serviços precisa ser planejada (REST, mensageria).

### 3. Arquitetura em Camadas

#### 3.1 Camada de Apresentação (Presentation Layer)

Responsável por:

- Interfaces de usuário (HTML, telas, frontend).

- Controllers e endpoints.

- Entrada e saída de dados.

- Não deve conter regra de negócio. Seu trabalho é “receber” e “entregar”.

#### 3.2 Camada de Aplicação (Application Layer)

Responsável por:

- Orquestrar a lógica da aplicação.

- Chamar serviços e casos de uso.

- Manipular fluxo entre as camadas.

- Ela coordena, mas não toma decisões específicas de negócio.

#### 3.3 Camada de Domínio (Domain Layer)

Essa camada não deve ter dependência para infraestrutura. Ela representa o conhecimento da empresa (O coração da aplicação). Ela contém:

- Regras de negócio puras.

- Entidades.

- Serviços de domínio.

- Validações internas.

#### 3.4 Camada de Dados/Infraestrutura (Infrastructure Layer)

É a camada mais “sujeita a mudanças”, por isso fica isolada. Responsável por:

- Conexão com banco de dados.

- Persistência (Repositories).

- Integração com APIs externas.

- Comunicação com sistemas terceiros.

### 4. Princípios Essenciais

#### 4.1 Separação de Responsabilidades (SoC)

Cada componente faz apenas o que lhe compete. Evita sistemas confusos, difíceis de manter e cheios de “jeitinhos”.

#### 4.2 Alta Coesão

Módulos fazem poucas coisas, mas fazem muito bem. Gera código mais claro e previsível.

#### 4.3 Baixo Acoplamento

Componentes não dependem rigidamente uns dos outros. Facilita testes, substituições e evolução do sistema.

#### 4.4 Modularidade

Dividir o sistema em módulos independentes melhora:

- Manutenção

- Reutilização

- Testabilidade

#### 4.5 Clareza e Simplicidade

Arquitetura não é sobre inventar complexidade. É sobre tornar o sistema compreensível.

### 5. Boas Práticas Arquiteturais

- Organize a estrutura de pastas: previsibilidade facilita manutenção.

- Evite duplicação de lógica: centralize regras de negócio.

- Use interfaces/contratos para abstrair implementações.

- Documente decisões importantes (Architecture Decision Records – ADRs).

- Mantenha camadas limpas: apresentação não fala com o banco, por exemplo.

- Evite “atalhos”: eles viram dívidas técnicas.

- Pense antes de codar: arquitetura vem antes de implementação.

### 6. Repositórios sobre Arquitetura de Sofware

- https://github.com/marco-mendes/arquitetura-software

- https://github.com/marco-mendes/projeto-arquitetura-software

## Contato

- LinkedIn: https://www.linkedin.com/in/murilolincons/ <br>
- E-mail: murilolincons@gmail.com
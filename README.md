# 1. O que é o Cypress e para que serve?
O Cypress é um framework dr javascript, e uma ferramenta que serve para a realização de testes automatizados.  Com ele, é possível configurar, escrever, rodar e **debugar** testes de forma simples e rápida.
Os Testes automatizados ajudam a garantir a qualidade de softwares, além de reduzir custos e ajudar na implementação de novas funcionalidades.
# 2.1 Vantagens em relação a outras ferramentas de teste
- O Cypress oferece recursos para a realização de testes ponta-a-ponta (end-to-end) e é capaz de simular a experiência de usuários reais, além de testes de componente e testes de API;
- All-in-one: Diferente das outras ferramentas de testes, ele unifica vários frameworks, bibliotecas e ferramentas em um só lugar, facilitando muito a experiência do desenvolvedor na fase de testagem;
- Ele tem acesso ao front-end e back-end da aplicação;
- esponde aos eventos em tempo real, e opera em tempo real na camada de rede
- É instalado localmente = pode realizar ações como screenshots ee gravar vídeos
- Altavelocidade em relação a outras ferramentas
- É open source e tem uma documentação clara e completa
- Possui um serviço de dashboards (gratuito e pago) para gerenciar os testes
- O erro na hora de execução tem um link que direciona para uma possível solução do problema 
# 2.1 Desvantagens
- É voltado mais para aplicações web, e não é adequado para testes de aplicativos móveis ou desktop
- Limitação em relação a navegadores como o safari
- Requer conhecimento de JavaScript: Pode ser uma desvantagem para equipes com pouca experiência em JavaScript.
# 3. Arquitetura
A imagem a seguir descreve com clareza a arquitetura e funcionamento da ferramenta:

![arquitetura](/assets/arq.png)

Além disso, O Cypress contem 3 componentes principais em sua arquitetura:

- **Runner**: Interface gráfica onde os testes são escritos, executados e depurados.
- **Automation Engine**: Controla o navegador e executa os testes.
- **Dashboard**: Fornece insights e informações sobre a execução dos testes em diferentes ambientes.

# 4. Seletores de elementos
Os seletores de elementosservem para localizar e interagir com elementos HTML dentro da página durante a execução de testes, e permitem que os testes simulem interações do usuário, como clicar em botões.

Exitem tipos de seletores como CSS, XPath ou por atributos específicos. Nesse sentido, alguns exemplos comuns incluem:

- cy.get('selector'): Seleciona um elemento usando um seletor CSS.
- cy.contains('text'): Seleciona um elemento que contém o texto especificado.
- cy.xpath('xpath-selector'): Seleciona um elemento usando XPath.
# 5. Comandos e asserções
Uma das vantagens do Cypress é a grande variedade de comandos prontos e asserções para interagir com elementos e verificar o estado da aplicação. Isso facilita muito a realizaçãoo dos testes, visto que traz lógicas prontas para funções essenciais, de forma compreensível e simples.

Dessa forma, alaguns exemplos de comandos e asserções são:
- cy.click(): Simula um clique em um elemento.
- cy.type(): Insere texto em um campo de entrada.
- cy.get().should('have.text', 'expected text'): Verifica se um elemento tem o texto esperado.
# 6. Descrição das etapas de preparação de um testes de interface, execução e verificação
### Preparação:

1. Instale o Cypress e configure seu ambiente.
-      npm install cypress --save-dev
3. Escreva os testes usando a sintaxe do Cypress.
4. Organize os testes em arquivos de especificação.

### Execução:
1. Inicie o Cypress Runner.
2. Selecione o teste a ser executado.
3. Execute o teste e observe os resultados em tempo real.
-      ./node_modules/.bin/cypress open 
ou
-      npx cypress open

### Verificação:
1. Verifique se todos os testes passaram.
2. Analise os resultados e depure qualquer problema encontrado.
3. Refatore os testes conforme necessário.
# 7. Como estruturar testes de forma eficiente no Cypress?
Afim de aproveitar ao máximo as funcionalidades oferecidas pelo Cypress, é importante uma organização dos testes em pastas e arquivos de acordo com a funcionalidade, a utilização de fixtures para dados de teste reutilizáveis e a reutilização de código através de comandos personalizados. Além de manter os testes simples, focados e independentes entre si.

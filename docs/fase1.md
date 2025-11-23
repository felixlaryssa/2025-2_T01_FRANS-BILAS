# Fase 1 — Estabelecer Requisitos de Avaliação

<div style="text-align: center;">
  <img src="../assets/images/sougov.png" alt="SouGov.br" style="max-width: 100%; height: auto;">
</div>
<div style="text-align: center; margin: 0; font-size: 14px;">
  Imagem 1: Logo SouGov
</div>

<details>
  <summary>Versão SouGov Mobile</summary>
  Versão 5.573 — Versão mobile utilizada ao longo desta avaliação.
</details>

## 1. Objetivo
O objetivo desta fase é **definir os requisitos de avaliação de qualidade** do sistema **SouGov.br**, com ênfase nas características de **Adequação Funcional** e **Confiabilidade**. 

Este documento apresenta o escopo da avaliação, identifica as partes interessadas e descreve o modelo de qualidade que orientará as próximas etapas da análisee, utilizando o diagnóstico automatizado de reviews como ferramenta de mensuração.


## 2. Requisitante e Partes Interessadas
A avaliação envolve os seguintes stakeholders, dada a natureza pública e crítica do 
software: 

- **Requisitante/Gestor:** Ministério da Gestão e Inovação em Serviços Públicos (MGI).  
- **Fornecedor/Desenvolvedor:** Serviço Federal de Processamento de Dados (Serpro).  
- **Usuários finais:** Servidores públicos federais ativos, aposentados, pensionistas e anistiados.
- **Avaliadores: Grupo Frans Bilas, responsável por conduzir a análise e interpretar 
os resultados gerados pela ferramenta de PLN.   
- **Operadores:** Órgãos de gestão de pessoas da Administração Pública Federal.  
- **Outras partes interessadas:** Órgãos de controle (CGU, TCU), gestores públicos e cidadãos que utilizam os serviços indiretos da plataforma.  


## 3. Descrição do Software
O **SouGov.br** é um aplicativo móvel e uma plataforma web que centralizam funcionalidades de **gestão de pessoas do setor público federal**.  
Entre os [principais serviços oferecidos](https://www.gov.br/servidor/pt-br/assuntos/sou-gov.br/servicos-disponiveis-aplicativo-sou-gov.br) estão:  

- Consulta de contracheque;  
- Solicitação e acompanhamento de benefícios;  
- Atualização cadastral de dados pessoais e funcionais;  
- Prova de vida digital;  
- Gestão de consignações e dependentes;  
- Serviços relacionados à saúde e licenças.  


## 4. Classificação do Tipo de Produto

- **De acordo com a [IEEE 1062](https://homepages.dcc.ufmg.br/~rodolfo/GPS1-Turma11/padraoIEEEProcessoAquisicao.pdf):**  
  O SouGov.br enquadra-se na categoria **COTS (Commercial Off-The-Shelf Software)**, por ser disponibilizado de forma padronizada a todos os usuários. Nesse contexto, o “fabricante” é o próprio governo, que provê o software como serviço público.  

- **De acordo com [Pressman](https://archive.org/details/pressman-engenharia-de-software-uma-abordagem-profissional-8a/mode/1up):**  
  Apesar de não ter finalidade comercial direta, o sistema aproxima-se da definição de **Software Comercial**, considerando que busca **automatizar processos sociais e integrar serviços governamentais**, beneficiando grande número de usuários.  

## 5. Organograma Funcional do SouGov.br

O **SouGov.br** opera através de uma arquitetura em camadas bem definida, conforme apresentado no organograma funcional a seguir:

```
Organograma Funcional do SouGov.br
│
├── 1. Camada de Governança e Gestão
│   ├── Ministério da Gestão e Inovação (MGI) → Define diretrizes e políticas.
│   └── Órgãos de Controle (CGU, TCU) → Monitoram conformidade.
│
├── 2. Camada de Desenvolvimento e Infraestrutura
│   └── Serpro (Fornecedor/Desenvolvedor)
│       ├── Desenvolvimento e manutenção (Android, iOS, Web).
│       ├── Infraestrutura em nuvem e hospedagem.
│       └── Integração com sistemas estruturantes.
│
├── 3. Camada de Integrações
│   ├── Gov.br → Autenticação e login unificado.
│   ├── SIAPE → Dados funcionais e folha de pagamento.
│   ├── Banco Central / Instituições Financeiras → Consignações.
│   └── Prova de Vida Digital (Dataprev/INSS) → Autenticação biométrica.
│
├── 4. Camada de Aplicação (SouGov.br)
│   └── Módulos Centrais
│       ├── Consulta de contracheque.
│       ├── Solicitação de benefícios.
│       ├── Atualização cadastral.
│       ├── Prova de vida digital.
│       ├── Gestão de consignações.
│       ├── Carteira funcional digital.
│       ├── Posse digital.
│       └── Gestão de estagiários e anistiados.
│
└── 5. Camada de Usuários
    ├── Servidores Ativos → Acessam contracheque, férias, licenças, etc.
    ├── Aposentados → Realizam prova de vida, consultam histórico.
    ├── Pensionistas → Gerenciam pagamentos, benefícios, prova de vida.
    ├── Estagiários → Gerenciam contratos, frequência, documentos.
    └── Anistiados → Acessam benefícios, histórico e cadastros.
```

Esta estrutura hierárquica demonstra como o sistema opera de forma integrada, conectando diferentes níveis organizacionais desde a **governança** até os **usuários finais**, passando por **infraestrutura técnica**, **integrações sistêmicas** e **funcionalidades de aplicação**.


## 6. Propósito da Avaliação e Uso Pretendido
A avaliação tem como propósito verificar se o software atende às necessidades de seus usuários em termos de **adequação funcional** e **confiabilidade**, considerando sua relevância para a gestão pública.  

Os resultados da avaliação visam:  
1. Identificar lacunas funcionais e riscos associados à confiabilidade, baseado na 
percepção do usuário final (reviews);  
2. Apoiar o planejamento de evolução e manutenção do sistema;  
3. Contribuir para decisões de melhoria contínua;  
4. Sustentar a transparência e a confiança nos serviços digitais oferecidos pelo governo.  


## 7. Modelo de Qualidade

O modelo de qualidade prioriza duas características críticas da ISO/IEC 25

### 7.1 Adequação Funcional

Esta característica foca na capacidade do produto de software de fornecer funções que 
satisfaçam as necessidades.

- **Completude funcional:** verificação da presença de todas as funções necessárias;  
- **Correção funcional:** avaliação da precisão dos resultados produzidos;  
- **Adequação à tarefa:** análise da contribuição das funções para o alcance dos objetivos do usuário.  

### 7.2 Confiabilidade
- **Maturidade:** estabilidade do sistema durante a operação;  
- **Disponibilidade:** capacidade de estar operacional quando necessário;  
- **Tolerância a falhas:** continuidade do funcionamento mesmo diante de falhas parciais;  
- **Recuperabilidade:** capacidade de retornar ao estado operacional após falhas.  


## 8. Critérios de Priorização
- A **adequação funcional** possui prioridade máxima, visto que assegura que as necessidades dos usuários sejam plenamente atendidas.  
- A **confiabilidade** assume papel essencial, considerando o tratamento de **dados pessoais sensíveis** e a execução de **processos críticos** para a administração pública.  


## 9. Escopo, Profundidade e Objetos de Avaliação

O escopo da avaliação é detalhado por perfil de usuário e objetos técnicos de mensuração 
pela ferramenta de análise de reviews.

### 9.1 Escopo de Usuários

A análise da ferramenta deve focar na correlação do feedback de texto com os serviços 
críticos de cada perfil: 

- **Servidores ativos:** contracheque, férias, licenças, consignações, gestão de dependentes, oportunidades internas, prova de vida, posse digital e carteira funcional.

- **Aposentados:** manutenção de benefícios, prova de vida digital, consulta de contracheques, atualização cadastral e acesso a documentos funcionais digitais.

- **Pensionistas:** acesso e atualização de dados do benefício, consultas de pagamentos, prova de vida e manutenção de vínculo.

- **Estagiários:** gestão do contrato de estágio, documentos comprobatórios, acompanhamento de frequência e comunicações administrativas (quando aplicável).

- **Anistiados:** gestão dos benefícios, histórico funcional, consulta a pagamentos e atualização cadastral.

### 9.2 Escopo Técnico

Escopo Técnico: Aplicativo móvel (Android) e Integrações com sistemas 
estruturantes da Administração Pública (SIAPE, Gov.br, Prova de Vida Digital, 
serviços do Serpro e demais sistemas de apoio). 

### 9.3 Profundidade da Avaliação
- **Adequação Funcional:** análise de todas as funções críticas relacionadas a cada perfil de usuário.

- **Confiabilidade:** verificação da estabilidade, consistência e recuperação do aplicativo em diferentes cenários de uso.

### 9.4 Objetos de Avaliação

Os reviews devem ser correlacionados primariamente aos seguintes serviços: 

- **Servidores Ativos:** contracheque, férias, licenças, consignações, posse digital, carteira funcional e solicitações de benefícios.

- **Aposentados:** prova de vida, contracheque, atualização cadastral e histórico funcional.

- **Pensionistas:** prova de vida, manutenção de benefício, consultas de pagamentos e documentos funcionais.

- **Estagiários:** gestão do vínculo, termos de compromisso, comprovação de frequência e documentos administrativos.

- **Anistiados:** benefícios concedidos, registros funcionais, histórico de pagamentos e atualizações cadastrais. 


## 10. Relação com os [Objetivos de Desenvolvimento Sustentável (ODS)](https://brasil.un.org/pt-br/sdgs)

A avaliação se alinha aos seguintes ODS:

- **ODS 16 — Paz, Justiça e Instituições Eficazes**  
  O SouGov.br contribui para a **transparência**, o **fortalecimento institucional** e a **eficiência** da gestão pública ao digitalizar processos administrativos.  

- **ODS 9 — Indústria, Inovação e Infraestrutura**  
  O sistema promove a **inovação tecnológica no setor público**, ao disponibilizar uma infraestrutura digital acessível e confiável para milhões de cidadãos.  

**Justificativa:** A plataforma representa um avanço na modernização da infraestrutura digital da administração pública, aumentando a eficiência institucional e fortalecendo a confiança social nos serviços governamentais.  

## 11. Conclusão
Esta documentação apresenta a Fase 1 da avaliação de qualidade do SouGov.br, 
estabelecendo o escopo, as partes interessadas e o modelo de qualidade com foco em 
Adequação Funcional e Confiabilidade, ancorado na metodologia de análise de reviews.  

As etapas subsequentes consistirão em:  
- Definir métricas específicas de avaliação;  
- Selecionar métodos de mensuração;  
- Elaborar planos de teste para validação prática.  

Essas ações possibilitarão a análise aprofundada das características avaliadas e subsidiarão a melhoria contínua do sistema.

---------------------

## Tabela de Contribuição - Grupo Frans Bilas

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 4: Contribuições dos Membros do Grupo
</div>

| Matrícula | Nome do aluno | Atividade Realizada | % de Contribuição |
| --------- | ------------- | ------------------- | ----------------- |
| 200060783 | Ana Beatriz W. Massuh | Refinamento e Revisão final | 18,6% |
| 190085584 | Carlos Eduardo Mendes |  Pesquisa inicial e Setup inicial | 18,6% |
| 231034707 | Giovana Ferreira Santos | Refinamento e Revisão final | 18,6% |
| 231026840 | Laryssa Felix |  Pesquisa e Criação final do gitpages  | 22% |
| 202070064 | Matheus do Vale | Pesquisa e Criação final do gitpages | 22% |

---------------------

## Bibliografia

> PRESSMAN, R. S.; MAXIM, B. R. *Engenharia de Software: uma abordagem profissional*. 8. ed. McGraw Hill, 2016.

> SOMMERVILLE, I. *Engenharia de Software*. 10. ed. Pearson, 2019.

> KITCHENHAM, B. *Software Quality: The elusive target*. IEEE Software.

> ORGANIZAÇÃO DAS NAÇÕES UNIDAS (ONU). *Transformando Nosso Mundo: A Agenda 2030 para o Desenvolvimento Sustentável*. ONU, 2015.

> ONU Brasil. *Objetivo 9: Indústria, inovação e infraestrutura*. Disponível em: <https://brasil.un.org/pt-br/sdgs/9>. Acesso em: 27 setembro 2025.

> ONU Brasil. *Objetivo 16: Paz, justiça e instituições eficazes*. Disponível em: <https://brasil.un.org/pt-br/sdgs/16>. Acesso em: 27 setembro 2025.

> Ministério da Gestão e da Inovação em Serviços Públicos (MGI). *SouGov – Aplicativo oficial de serviços do servidor público federal*. Disponível em: <https://www.gov.br/servidor/pt-br/sou-gov>. Acesso em: 27 setembro 2025.

> Governo Federal. *Plataforma Gov.br – Serviços digitais para o cidadão*. Disponível em: <https://www.gov.br>. Acesso em: 27 setembro 2025.

-----------------

## Histórico de versão

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 3: Tabela de Versionamento
</div>

| Versão | Data       | Descrição                             | Autor(a) |
| ------ | ---------- | ------------------------------------- | -------- |
| 1.0    | 28/09/2025 | Versão inicial e incompleta da fase 1 | [Carlos Edurado](https://github.com/CarlosEduardoMendesdeMesquita)   |
| 2.0    | 28/09/2025 | Versão completa da fase 1 | [Laryssa Felix](https://github.com/felixlaryssa) e  [Matheus do Vale](https://github.com/delvale412)  |
| 3.0    | 29/09/2025 | Versão aprimorada da fase 1 | [Laryssa Felix](https://github.com/felixlaryssa)  |
| 4.0    | 01/10/2025 | Adicionando referênciação | [Ana Beatriz Massuh](https://github.com/AnaBeatrizMassuh) |
| 5.0    | 01/10/2025 | Adicionando Organograma e Escopo | [Matheus do Vale](https://github.com/delvale412) e [Giovana Ferreira Santos](https://github.com/gih7915) |

<div style="text-align: center; margin: 0; font-size: small;">
Fonte: 
<a href="https://github.com/AnaBeatrizMassuh">Ana Beatriz Massuh</a>, 
<a href="https://github.com/CarlosEduardoMendesdeMesquita">Carlos Eduardo Mendes</a>, 
<a href="https://github.com/gih7915">Giovana Ferreira</a>, 
<a href="https://github.com/felixlaryssa">Laryssa Felix</a>, e
<a href="https://github.com/delvale412">Matheus Do Vale</a>.
</div>

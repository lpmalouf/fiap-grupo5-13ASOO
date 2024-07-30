# fiap-grupo5-13ASOO

#Sumario Executivo

Repositório para Solution Sprint fase 04 e 05 - grupo5 13ASOO MBA Arquitetura de Soluções

# Descrição do projeto 

Descrição do Projeto: Sistema de Gerenciamento de Playlists Musicais da SpotMusic
A SpotMusic um sistema de gerenciamento de playlists musicais. A arquitetura adotada para este projeto foi planejada para garantir escalabilidade, flexibilidade e alta performance. Abaixo está uma breve descrição das principais componentes e tecnologias adotadas:
Arquitetura Geral
1.	Front-end:
        •	Tecnologia: Python Flask
        •	Descrição: Utilizado para desenvolver a interface web do sistema, proporcionando uma base sólida e flexível para a criação de uma interface de usuário responsiva e                 eficiente.
        Mobile:
        •	Tecnologia: Ionic com Capacitor
        •	Descrição: Escolhido pela sua alta produtividade e capacidade de personalização de layout para diferentes plataformas, o Ionic permite o desenvolvimento rápido e                   eficaz de aplicações móveis para Android e iOS.
2.	Back-end:
        •	Tecnologia: Microsserviços em Python
        •	Descrição: A arquitetura de microsserviços permite o desenvolvimento, implantação e escalabilidade independentes de cada funcionalidade do sistema, melhorando a                    manutenção e a atualização contínua do serviço.
3.	Banco de Dados:
        •	Tecnologias: Amazon RDS for MySQL e Amazon DynamoDB
        •	Descrição: Amazon RDS for MySQL é utilizado para armazenamento de dados estruturados, enquanto o Amazon DynamoDB é usado para armazenamento de dados NoSQL, 
                proporcionando flexibilidade e performance nas operações de leitura e escrita.
4.	Serviços de Mensageria:
        •	Tecnologia: Apache Kafka
        •	Descrição: Utilizado para comunicação eficiente entre microsserviços, garantindo a integridade e a rapidez na troca de informações.
5.	Monitoramento e Logging:
        •	Tecnologia: Amazon CloudWatch
        •	Descrição: Implementado para monitoramento contínuo da infraestrutura e das aplicações, além de coleta e análise de logs, permitindo a detecção proativa de                         problemas e a manutenção da saúde do sistema.
6.	Ferramenta de Analytics:
        •	Tecnologia: Amazon QuickSight
        •	Descrição: Usado para análise de dados e criação de dashboards interativos, fornecendo insights valiosos sobre o comportamento dos usuários e a performance das                                músicas.
Estratégia de Repositório de Código
        •	Plataforma: GitHub
        •	Fluxo de Trabalho: GitFlow
        •	Estrutura: Repositórios separados para cada microsserviço e um repositório monolítico para o front-end e aplicações mobile.
        •	Regras de Commit: Mensagens de commit padronizadas para garantir clareza e rastreabilidade das mudanças.
        •	Integração Contínua e Deploy Contínuo (CI/CD): Implementação de pipelines automatizados com GitHub Actions para build, teste e deploy.

# Estratégia padrão adotada para o Repositório de Código na SpotMusic
# Estrutura de Repositórios
1.	Repositórios Separados para Microsserviços
	•	Decisão: Cada microsserviço terá seu próprio repositório.
	•	Justificativa: Essa abordagem facilita a manutenção e a atualização independente de cada serviço, promovendo a modularidade e permitindo que diferentes equipes trabalhem 			    simultaneamente em serviços distintos.
	•	Ganhos: Melhor organização, independência no desenvolvimento, facilidade de integração contínua e deploy contínuo (CI/CD).
2.	Repositório Monolítico para o Front-end e Aplicações Mobile
	•	Decisão: O código do front-end desenvolvido em Flask e das aplicações mobile em Ionic com Capacitor serão armazenados em um repositório monolítico.
  •	Justificativa: Manter o código do front-end e das aplicações mobile juntos facilita a gestão das interfaces de usuário e garante consistência entre as diferentes plataformas.
  •	Ganhos: Facilidade de manutenção e sincronização entre versões de front-end e aplicações mobile, melhoria na colaboração entre desenvolvedores front-end e mobile.
    Estratégia de fluxo de trabalho adotada
1.	GitFlow
  •	Decisão: Adotamos o GitFlow como fluxo de trabalho.
  •	Justificativa: O GitFlow é um modelo de ramificação que utiliza branches dedicadas para desenvolvimento, testes e produção, garantindo um processo estruturado de integração e      entrega contínua.
  •	Ganhos: Controle de versão eficiente, capacidade de gerenciar múltiplas versões e funcionalidades paralelamente, e maior estabilidade no código de produção.
2.	Branches de Desenvolvimento
  •	Decisão: Implementar branches específicas para features, releases, hotfixes e suporte.
  •	Justificativa: Utilizar branches dedicadas para diferentes estágios do desenvolvimento promove organização e controle sobre o ciclo de vida do código.
  •	Ganhos: Melhor organização do código, controle sobre o desenvolvimento de novas funcionalidades e correções, e facilitação do processo de integração e deploy.
3.	Regras de Commit
  •	Decisão: Estabelecer regras claras e padronizadas para mensagens de commit.
  •	Justificativa: Mensagens de commit claras e padronizadas melhoram a rastreabilidade e a compreensão das mudanças no código.
  •	Ganhos: Melhor rastreamento do histórico de mudanças, facilidade na revisão de código e maior clareza na comunicação entre desenvolvedores.
Regras de Commit Propostas:
Formato: [Tipo]: [Descrição]
  •	Tipos: feat (nova funcionalidade), fix (correção de bug), docs (mudanças na documentação), style (formatação e estilo do código), refactor (refatoração de código), test            (adição ou modificação de testes), chore (tarefas diversas).
Exemplo: feat: adiciona nova funcionalidade de login com OAuth
4.	Pull Requests e Revisões de Código
  •	Decisão: Utilizar pull requests (PRs) para integrar mudanças ao código-base.
  •	Justificativa: Pull requests permitem a revisão de código antes da integração, garantindo a qualidade e a conformidade com os padrões de codificação estabelecidos.
  •	Ganhos: Melhoria na qualidade do código, detecção precoce de erros, promoção de boas práticas e colaboração entre desenvolvedores.
5.	Integração Contínua e Deploy Contínuo (CI/CD)
  •	Decisão: Configurar pipelines de CI/CD para automação de testes e deploy.
  •	Justificativa: Automatizar o processo de integração e deploy acelera a entrega de novas funcionalidades e correções, além de garantir que o código seja constantemente testado      e validado.
  •	Ganhos: Redução de erros manuais, aumento na velocidade de deploy, e maior confiabilidade nas novas versões da aplicação.
Ferramentas e Integrações
1.	Integração com GitHub Actions
  •	Decisão: Utilizar GitHub Actions para pipelines de CI/CD.
  •	Justificativa: GitHub Actions oferece uma integração nativa com repositórios do GitHub, facilitando a configuração e execução de workflows automáticos.
  •	Ganhos: Automação de processos de build, teste e deploy, maior agilidade no ciclo de desenvolvimento, e visibilidade clara do status das builds.
2.	Gerenciamento de Issues e Projetos
  •	Decisão: Utilizar GitHub Issues e Projects para rastreamento de tarefas e gerenciamento de projetos.
  •	Justificativa: Essas ferramentas integradas ao GitHub permitem um gerenciamento centralizado das tarefas e melhoram a comunicação e a organização do trabalho em equipe.
  •	Ganhos: Melhoria na organização das tarefas, rastreamento de bugs e funcionalidades, e promoção da colaboração e transparência entre as equipes de desenvolvimento.


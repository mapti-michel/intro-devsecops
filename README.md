# Introdução ao DevSecOps - Notebook: DevSecOps do zero ao professional
Criando o segundo cérebro para complementar conhecimentos introdutório de DevSecOps no notebookLM.
NotebookLM: https://notebook.google.com/notebook/6a6bc8d8-0899-4a80-94be-7ed48e347ae8

📄 CONTEXTOS E OBJETIVOS: Criar o segundo cérebro para complementar conhecimentos introdutório de DevSecOps. É uma área pouco mencionada, mas de muito valor no mercado de trabalho. Unificada com as tarefas de Dev (Desenvolvimento) + Sec (Security) + Ops (Operação automatizada), apresenta um bom desempenho na criação de softwares, automatizando as tarefas e analisando a segurança do código e do software. Particularmente, estou fascinado pelo cargo e sua cultura, pois permite-me desenvolver e analisar os pontos preocupantes no código.

📝 CURADORIA DE FONTES: 

	VÍDEO: 

	https://www.youtube.com/watch?v=CCp30BD9uRo

	https://www.youtube.com/watch?v=cxAn9toR8yc

	https://www.youtube.com/watch?v=g85PQvDI8Cc

	https://www.youtube.com/watch?v=eCruLk9h3I4

	https://www.youtube.com/watch?v=xSDMEt6csRo

	https://www.youtube.com/watch?v=iGJxNtjj_VE

	TEXTO (Deep Research): "Introdução ao DevSecOps" e "DevSecOps do zero ao professional"

 	NOTA: Comporte-se em ser amigável e animado, para que o consultante sinta-se à vontade em ler.

📂 ENGENHARIA DE PROMPTS E "CICATRIZES":

As perguntas realizadas e suas respostas em questão, são:
1 - Quais são os pilares do devsecops ?

	Os pilares do DevSecOps baseiam-se na integração da segurança em todas as etapas do ciclo de vida de desenvolvimento de software, transformando-a em uma responsabilidade compartilhada entre as equipes de desenvolvimento, segurança e operações.
	De acordo com as fontes, os principais pilares e conceitos fundamentais são:
	- Cultura e Responsabilidade Compartilhada: A segurança deixa de ser um setor isolado e torna-se dever de todos os envolvidos no projeto. Isso exige uma mudança cultural para eliminar silos organizacionais e promover a colaboração desde o início.
	- Automação: Para garantir que a segurança não se torne um gargalo, as verificações e testes devem ser automatizados dentro do pipeline de CI/CD. A automação permite que os controles sejam rápidos, escaláveis e eficazes na detecção de vulnerabilidades.
	- Shift Left (Deslocamento para a Esquerda): Este pilar consiste em mover as práticas de segurança para as fases iniciais do desenvolvimento, como planejamento e codificação, em vez de tratá-la apenas no final do ciclo. Identificar falhas precocemente reduz drasticamente os custos e o tempo de correção.
	- Monitoramento Contínuo: Implementa a visibilidade em tempo real da postura de segurança das aplicações e infraestruturas, permitindo respostas rápidas a incidentes.
	- Integração: Ferramentas e processos de segurança são incorporados diretamente no fluxo de trabalho existente, tornando-se parte natural do processo de entrega.
	No âmbito técnico da segurança de aplicações, as fontes frequentemente destacam três tecnologias como pilares essenciais:
	- SAST (Static Application Security Testing): Análise estática do código-fonte em busca de vulnerabilidades antes da execução.
	- SCA (Software Composition Analysis): Análise de dependências de terceiros e bibliotecas de código aberto para identificar riscos conhecidos e conformidade de licenças.
	- DAST (Dynamic Application Security Testing): Testes dinâmicos realizados durante o tempo de execução, simulando ataques externos para encontrar falhas em tempo real.
	Além desses, o modelo de governança também é citado como um pilar de suporte, através da Governança Adaptativa, que ajusta os controles de segurança com base no risco e permite manter a agilidade sem comprometer a conformidade.

2 - Quais são os softwares utilizados na prática do DevSecOps ?

	A prática de DevSecOps utiliza uma ampla variedade de softwares e ferramentas para automatizar a segurança em todas as etapas do ciclo de vida de desenvolvimento (SDLC). Essas ferramentas são geralmente categorizadas de acordo com sua função no pipeline:
	1. Plataformas de CI/CD e Orquestração

	Estas ferramentas gerenciam a integração e entrega contínua, servindo como a "espinha dorsal" para a execução de testes de segurança.
	- GitLab CI/CD: Uma plataforma completa que incorpora scanners de segurança diretamente no fluxo de trabalho.
	- GitHub Actions: Amplamente utilizado para automatizar pipelines através de "Actions" personalizadas para segurança.
	- Jenkins: Ferramenta de automação de código aberto altamente customizável via plugins.
	- ArgoCD: Focada em GitOps, garante que o estado da infraestrutura no Kubernetes corresponda ao definido no repositório Git.
	- Jit: Uma plataforma de orquestração que unifica diversas ferramentas de segurança de código aberto em uma única interface.

	2. Testes de Segurança de Aplicações (SAST, DAST, SCA)

	Essas ferramentas analisam o código, as dependências e a aplicação em execução.
	- SAST (Análise Estática): Analisa o código-fonte sem executá-lo. Exemplos incluem SonarQube, Snyk Code, Semgrep, Checkmarx e Njsscan.
	- SCA (Análise de Composição): Identifica vulnerabilidades em bibliotecas de terceiros. Exemplos: Snyk, Dependabot, Renovate e OWASP Dependency-Check.
	- DAST (Análise Dinâmica): Simula ataques em aplicações em execução. Destacam-se o OWASP ZAP, Burp Suite, StackHawk e Nuclei.

	3. Segurança de Infraestrutura como Código (IaC) e Nuvem

	Softwares voltados para validar configurações de infraestrutura (como Terraform e Kubernetes) antes do provisionamento.
	- Checkov: O padrão da indústria para escanear arquivos Terraform e Kubernetes em busca de configurações incorretas.
	- Spacelift: Plataforma para governança de políticas e conformidade de infraestrutura.
	- KICS (Keep Infrastructure as Code Secure): Ferramenta de código aberto que suporta múltiplos formatos como Ansible e Helm.
	- Prowler: Utilizada para auditoria de conformidade e segurança em ambientes AWS, Azure e GCP.
	- Open Policy Agent (OPA): Permite escrever e aplicar "políticas como código" em toda a stack tecnológica.

	4. Gerenciamento de Segredos e Varredura de Credenciais

	Ferramentas essenciais para evitar o vazamento de senhas e chaves de API.
	- HashiCorp Vault: Líder em gerenciamento de identidades e criação de segredos dinâmicos de curta duração.
	- GitLeaks e TruffleHog: Scanners que detectam segredos hardcoded em repositórios Git, inclusive em históricos antigos.
	- Spectral: Scanner focado em desenvolvedores para detecção rápida de tokens e chaves em código e logs.

	5. Segurança de Contêineres e Runtime

	Softwares que protegem a execução de microsserviços e imagens de contêiner.
	- Trivy: Um scanner versátil para imagens de contêiner, sistemas de arquivos e configurações de Kubernetes.
	- Falco e Sysdig: Focadas em segurança de runtime, monitorando comportamentos anômalos em tempo real.
	- Kyverno: Um controlador de admissão para Kubernetes que gerencia e valida políticas de segurança no cluster.

	6. Novas Tendências: Remediação com IA

	- Plexicus: Representa a nova geração de ferramentas que utilizam IA não apenas para detectar, mas para gerar automaticamente correções (Pull Requests) para as vulnerabilidades encontradas.

3 - Qual é a importância do DevSecOps no atual mercado de trabalho e no ciclo de desenvolvimento de softwares ?
trabalho e no ciclo de desenvolvimento de softwares ?

	O DevSecOps tornou-se o padrão para a entrega de software moderno e é considerado um requisito básico para a competitividade digital em 2026. Sua importância reside na transformação da segurança de um "obstáculo" final em uma responsabilidade compartilhada e automatizada em todas as etapas do ciclo de vida de desenvolvimento (SDLC).
	Abaixo, detalho a importância dessa prática sob duas perspectivas principais:

	1. No Mercado de Trabalho Atual
   
	O mercado de DevSecOps está em franca expansão devido à necessidade crítica de proteger dados e infraestruturas em nuvem:
	Alta Demanda por Profissionais: Estima-se que até 2025 o mercado de tecnologia gere cerca de 565 mil vagas, das quais aproximadamente 125 mil serão específicas para cloud e segurança. No LinkedIn, já existem milhares de oportunidades para trabalho remoto com o termo "DevSecOps".
	Expectativa das Grandes Empresas: Gigantes como Microsoft, Google, AWS e GitLab buscam engenheiros que não dominem apenas ferramentas (como Kubernetes ou Terraform), mas que possuam um pensamento "security-first" para construir plataformas seguras por padrão.
	Valorização Salarial e Carreira: Por ser uma área que unifica competências de desenvolvimento, segurança e operações, profissionais que transitam entre esses mundos são altamente valorizados, especialmente diante do crescimento global do mercado de DevOps, projetado para atingir US$ 25,5 bilhões até 2028.

	2. No Ciclo de Desenvolvimento de Software (SDLC)
    
	A integração da segurança no pipeline de CI/CD traz benefícios operacionais e financeiros tangíveis:
	Redução Drástica de Custos (Shift-Left): Identificar e corrigir uma falha durante a codificação pode ser até 100 vezes mais barato do que corrigi-la após o deploy em produção. Práticas de Shift-Left permitem que os desenvolvedores recebam feedback imediato enquanto escrevem o código.
	Mitigação de Riscos e Vulnerabilidades: Organizações que implementam segurança desde o início reduzem vulnerabilidades em produção em até 50%. Isso é vital considerando que o custo médio de uma violação de dados atingiu US$ 4,88 milhões em 2024.
	Velocidade com Segurança: O DevSecOps permite que equipes classificadas como "elite performers" realizem deploys sob demanda (várias vezes ao dia) sem comprometer a integridade do sistema.
	Resposta a Novos Desafios (IA): Com a IA gerando até 80% do código em algumas empresas, o DevSecOps é essencial para filtrar bibliotecas desatualizadas e códigos vulneráveis que modelos de linguagem (como o ChatGPT) podem introduzir acidentalmente.
	Conformidade Contínua: O uso de ferramentas como Checkov e Prowler garante que a infraestrutura esteja sempre em conformidade com normas como GDPR, HIPAA e LGPD, gerando evidências automáticas para auditorias.
	Em suma, o DevSecOps não é apenas uma escolha técnica, mas uma estratégia de crescimento e proteção da reputação. Ele garante que a inovação seja entregue de forma resiliente, confiável e eficiente, atendendo às exigências de um ambiente digital cada vez mais hostil.


🧾 MINIGUIA DE ESTUDO:

	Guia introdutório e professional do DevSecOps.

	ARQUIVO: Manual_DevSecOps.pptx




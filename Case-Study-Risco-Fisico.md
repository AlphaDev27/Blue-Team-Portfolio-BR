# 🛡️ Mitigação de Risco Crítico de Segurança Física e Hardening de Infraestrutura

#### 1. Contexto Operacional

* **Ambiente:** Infraestrutura crítica de TI em operação 24/7 (Hotel/Varejo de Alto Fluxo), responsável pela sustentação de serviços essenciais, como controle de acesso, faturamento e redes para milhares de usuários.
* **Papel:** Ponto focal e único responsável pela **disponibilidade** e **integridade** dos ativos de TI.

#### 2. Vulnerabilidade Crítica Identificada

Identificação de uma falha grave de **Segurança Física** com alto potencial de impacto na **Disponibilidade** e **Confidencialidade** da operação:

* **Ativo Exposto:** O **Rack** central (contendo servidores, *core* de rede e sistemas críticos) estava **aberto e sem controle de acesso físico**.
* **Risco Físico Imediato:** O servidor essencial estava posicionado no chão, aumentando o risco de danos acidentais, falha elétrica e exposição à poeira.
* **Referência (GRC):** Violação direta do controle de **Segurança Física (ISO 27001 - A.11)**.

#### 3. Ações de Mitigação Implementadas (Hardening)

As ações foram executadas com urgência, motivadas pela mentalidade de **redução de danos** e **proatividade** em ambiente crítico:

* **Controle de Acesso Físico:** Implementação de uma política e mecanismo para **travar o rack**, garantindo que apenas pessoal autorizado pudesse intervir nos ativos de TI.
* **Gestão de Ativos:** Remoção do servidor do chão e instalação adequada no rack, eliminando o risco de falha por impacto ou condições ambientais.
* **Hardening Lógico e de Processo:**
    * Mapeamento de toda a rede corporativa e sistemas.
    * Implementação de uma **política de senhas fortes** em alinhamento com os padrões de segurança.
    * Reestruturação do cabeamento (*cable management*) para facilitar a manutenção e o **diagnóstico rápido** durante incidentes (*troubleshooting*).

#### 4. Impacto e Lições Aprendidas (Mindset de Segurança)

* **Resultado:** Eliminação de uma vulnerabilidade de alto impacto, melhorando a **resiliência** e o **compliance** da infraestrutura.
* **Lição (Mindset):** A experiência reforçou que o sucesso no Blue Team depende da **proatividade** (agir antes do incidente), da **disciplina operacional** (organização e *hardening*) e da **calma sob pressão** (resiliência 24/7), habilidades desenvolvidas através do estudo contínuo em *mindset* e desenvolvimento humano.

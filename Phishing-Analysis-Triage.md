# 🎣 Projeto: Análise de Phishing e Triage de Incidentes

Este projeto demonstra a capacidade de um Analista SOC Nível 1 de analisar a origem de uma ameaça de e-mail e aplicar ações de contenção na camada de rede.

#### 1. 🚨 O Cenário: E-mail Suspeito Reportado

* **O Alerta:** Um usuário reportou um e-mail com alta suspeita de Phishing, contendo um link para uma URL que o time de Threat Intel classificou como maliciosa.
* **Ação Típica de SOC N1:** Isolar o e-mail, extrair o link e o endereço IP de destino para análise de autenticidade e contenção.

#### 2. 🔎 A Investigação do Cabeçalho (Análise de Rede)

A primeira etapa é investigar a origem real do e-mail.

* **Ferramenta de Análise:** Uso de ferramenta de visualização de cabeçalhos de e-mail.
* **Foco na Autenticidade:** Verificação dos protocolos de autenticação:
    * **SPF/DKIM/DMARC:** Procurar por resultados **"Fail"** ou **"Softfail"** nos *headers* (`Authentication-Results`), o que indica que a origem não foi autorizada a enviar em nome do domínio legítimo.
    * **Endereço de Origem:** Comparar o IP no campo `Received: from` com o domínio real.
* **Conclusão:** A falha na autenticação e o uso de um IP/URL malicioso externo confirmam a ameaça.

#### 3. 🛡️ Resposta, Contenção e Erradicação (Playbook de Ação)

A prioridade é impedir que o *malware* se propague ou que o usuário clique no link.

* **Ação Imediata (Contenção - Perímetro):**
    1.  **Bloqueio de IP Malicioso:** **Bloquear o endereço IP de destino** do link malicioso no **Firewall** ou **Gateway** de e-mail, aplicando a regra tanto para tráfego **de entrada** quanto **de saída**. Isso impede que usuários comprometidos se comuniquem com o C2 (Command and Control).
    2.  **Criação de Regra no SIEM:** Criar uma regra de detecção no SIEM/Sigma para monitorar qualquer outro tráfego relacionado a esse IP.
* **Erradicação:**
    1.  Usar o EDR ou a ferramenta de e-mail para **remover o e-mail** da caixa de entrada de todos os usuários da empresa.
    2.  Notificação urgente à empresa e à Gerência de Risco.


# Análise de Incidente de Segurança: Ataque de Força Bruta e Redirecionamento Malicioso

## Visão Geral do Projeto

Este projeto é um estudo de caso prático do [Google Cybersecurity Professional Certificate](https://www.coursera.org/google-certificates/cybersecurity-certificate), demonstrando o processo de ponta a ponta na resposta a um incidente de segurança. O cenário envolveu a análise de tráfego de rede (`tcpdump`) para identificar uma ameaça, a documentação dos achados em um relatório formal e a recomendação de controles de segurança profissionais para prevenir a reincidência.

---

## O Cenário

A análise foi baseada em um incidente onde um ex-funcionário mal-intencionado comprometeu o servidor web da empresa `yummyrecipesforme.com`. O ataque se desenrolou da seguinte forma:

1.  **Acesso Inicial:** O atacante realizou um ataque de **força bruta** contra o painel de administração, explorando uma senha padrão que não havia sido alterada.
2.  **Comprometimento:** Após obter acesso, o atacante injetou um código JavaScript malicioso no site.
3.  **Ação Maliciosa:** O script solicitava que os visitantes do site baixassem um arquivo executável falso.
4.  **Redirecionamento:** Após a execução do arquivo, o navegador do usuário era redirecionado para um site falso (`greatrecipesforme.com`), que continha malware e era controlado pelo atacante.

---

## Ferramentas e Metodologia

Para investigar e responder ao incidente, a seguinte metodologia foi aplicada:

* **Ambiente Controlado (Sandbox):** O site suspeito foi acessado em um ambiente de sandbox para observar seu comportamento sem arriscar a rede de produção.
* **Análise de Tráfego de Rede:** A ferramenta `tcpdump` foi utilizada para capturar e analisar os pacotes de rede, permitindo reconstruir a sequência de eventos.
* **Análise de Logs:** Os logs do `tcpdump` foram inspecionados para identificar as consultas DNS, os handshakes TCP e as requisições HTTP que confirmaram o redirecionamento malicioso.
* **Documentação Técnica:** Todas as descobertas foram consolidadas em um relatório de incidente de segurança formal.

---

## Relatórios do Incidente (PDF)

Os relatórios completos, detalhando a análise e as conclusões, estão disponíveis nos links abaixo. Eles foram criados em português e também traduzidos para o inglês para demonstrar proficiência em ambos os idiomas.

* 📄 **[Relatório do Incidente - Versão em Português (PDF)](https://github.com/cleyandson/case-study-brute-force-attack/blob/3f15d0579bf0de00601d81eaf3c1396d7d355f57/Documents/%5BPT-BR%5D%20Security%20incident%20report%20template.pdf)**

---

## Mitigações Propostas

Com base na causa raiz do ataque (credenciais fracas e falta de controles), foram recomendadas as seguintes ações de remediação, alinhadas com as melhores práticas da indústria como **NIST** e **CIS Controls**:

* **Implementação de Política de Senhas Fortes:** Exigir complexidade e comprimento mínimo para todas as senhas.
* **Mecanismo de Bloqueio de Conta (Account Lockout):** Bloquear contas automaticamente após múltiplas tentativas de login falhas.
* **Autenticação Multifator (MFA):** Habilitar a MFA para todas as contas administrativas como a defesa mais eficaz contra o comprometimento de credenciais.

---

## Competências Demonstradas

Este projeto destaca as seguintes habilidades essenciais em cibersegurança:

-   ✅ **Análise de Tráfego de Rede** com `tcpdump`
-   ✅ **Resposta a Incidentes de Segurança**
-   ✅ **Análise de Protocolos de Rede** (DNS, TCP, HTTP)
-   ✅ **Redação de Relatórios Técnicos** e Documentação de Incidentes
-   ✅ **Análise de Causa Raiz (RCA)**
-   ✅ **Recomendação e Implementação de Controles de Segurança**

---

## Contato

* **LinkedIn:** [Cleyandson Fragoso](https://www.linkedin.com/in/cleyandson-fragoso/)
* **E-mail:** cleyandsontech@gmail.com

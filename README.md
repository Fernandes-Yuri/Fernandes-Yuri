# Olá, eu sou o Yuri Fernandes 👋

### 🚀 Analista e Desenvolvedor de Software

Atuo na análise, conceção e desenvolvimento de sistemas distribuídos, aplicações móveis e soluções orientadas a microsserviços. Tenho o **Python** como linguagem principal de eleição 🐍, operando com facilidade e solidez em ecossistemas modernos com **Kotlin** (Android nativo & Jetpack Compose), **TypeScript**, **JavaScript** e **Node.js**.

Trabalho combinando análise técnica aprofundada, boas práticas de segurança/LGPD e ferramentas modernas de automação e inteligência artificial: orquestro esteiras de integração contínua com **Harness** e emprego ferramentas como **DeepSeek**, **Hermes**, **OpenAI Codex**, **Google Antigravity** e **OpenCode** para apoiar o fluxo de desenvolvimento, testes e entrega contínua de software.

---

### 🏥 Ecossistema em Destaque: Braga Saúde

> Plataforma completa de autocuidado clínico preventivo, automonitorização de hábitos e suporte familiar remoto (Modo Cuidador).

<table>
  <tr>
    <td>
      <h3>📱 Plataforma Integrada Braga Saúde</h3>
      <p>
        Solução completa com arquitetura multicamadas, garantindo integridade de dados clínicos autorreportados (SBC, SBD e OMS) e comunicação síncrona/assíncrona entre pacientes e cuidadores.
      </p>
      <ul>
        <li><strong>App Android Nativo:</strong> Desenvolvido em <strong>Kotlin</strong> com <strong>Jetpack Compose</strong>, seguindo arquitetura MVVM/MVI, persistência local cifrada via <strong>Room Database</strong> (SQLCipher e migrações versionadas), sincronização resiliente com <strong>WorkManager</strong> e integração com <strong>Google Health Connect</strong>.</li>
        <li><strong>PWA Cuidador (Web):</strong> Interface reativa e segura (Zero-Trust) em TypeScript/PWA para acompanhamento de sinais vitais, checklists de medicamentos e avisos em tempo real.</li>
        <li><strong>Backend Gateway & Microsserviços (Python):</strong> Núcleo em <strong>Python</strong> responsável pelo roteamento de APIs, processamento de regras clínicas, extração e validação de laudos e orquestração de microsserviços.</li>
        <li><strong>Módulo de IA &amp; Voz:</strong> Assistente conversacional com <strong>Rasa</strong> (NLU e gestão de diálogo) e <strong>motor determinístico em Kotlin</strong> para regras críticas, orquestração via WebSocket, transcrição de áudios (Whisper), síntese neural e integração com WhatsApp Business Cloud API.</li>
        <li><strong>Dados, Nuvem & LGPD:</strong> Infraestrutura com <strong>PostgreSQL dedicado</strong>, autenticação OTP em duas etapas, armazenamento autenticado de exames e esteiras de build/deploy contínuo com <strong>Harness</strong> e GitHub Actions.</li>
      </ul>
      <p>
        🌐 <strong>Conheça a plataforma:</strong> <a href="https://bragasaude.online" target="_blank">bragasaude.online</a>
      </p>
    </td>
  </tr>
</table>

---

### 🧠 Estratégia de IA Híbrida — Redução de Custos com Inferência Cloud

> *"Nem tudo precisa de um LLM: o que é crítico roda em código determinístico, o que é conversa roda na ferramenta mais enxuta possível."*

<table>
  <tr>
    <td>
      <h4>🎙️ Modelos de Voz On-Device</h4>
      <p>
        Exploração ativa de modelos de <strong>speech-to-text e text-to-speech compactos</strong> que rodam inteiramente no dispositivo Android, eliminando a dependência de APIs de voz na nuvem (Whisper API, Google Cloud Speech, etc.). A longo prazo, essa abordagem <strong>zera o custo por requisição de áudio</strong> — cada transcrição e síntese acontece localmente, sem latência de rede e sem cobrança por minuto de áudio processado.
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <h4>🧩 Rasa + Motor Determinístico em Kotlin</h4>
      <p>
        Em vez de enviar toda interação para um LLM generalista na nuvem, a arquitetura conversacional é dividida em camadas, cada uma com o nível de previsibilidade adequado à tarefa:
      </p>
      <ul>
        <li><strong>Rasa (NLU &amp; gestão de diálogo):</strong> classificação de intenções, extração de entidades e fluxos conversacionais estruturados com um framework open source treinado no vocabulário do nicho de saúde preventiva — sem cobrança por token.</li>
        <li><strong>Motor determinístico em Kotlin (on-device):</strong> tudo o que <strong>não admite margem de erro</strong> — horários e confirmação de doses de medicamentos, cálculos e faixas de referência de métricas biométricas, regras de alerta e escalonamento para o cuidador — é executado por regras explícitas e testáveis diretamente no app, nunca por um modelo probabilístico.</li>
        <li><strong>LLM na nuvem apenas como exceção:</strong> reservado para o que realmente exige linguagem livre, reduzindo drasticamente o volume de chamadas pagas.</li>
      </ul>
      <p><strong>Por que essa estratégia reduz custos (e riscos):</strong></p>
      <ul>
        <li><strong>Menos inferência paga:</strong> a maior parte do tráfego é resolvida por regras locais e pelo Rasa, transformando custo variável por requisição em custo praticamente fixo de infraestrutura.</li>
        <li><strong>Zero alucinação no que é crítico:</strong> decisões clínicas sensíveis seguem lógica determinística, auditável e coberta por testes unitários.</li>
        <li><strong>Funciona offline:</strong> as regras críticas rodam no próprio dispositivo, sem depender de conexão ou de roundtrip à nuvem.</li>
        <li><strong>Privacidade nativa:</strong> dados clínicos usados nas regras críticas não precisam sair do aparelho, reforçando a conformidade com a LGPD.</li>
      </ul>
      <p>
        <strong>Lição aprendida:</strong> antes dessa arquitetura, testei o fine-tuning de um <strong>Qwen 0.5B</strong> para inferência 100% on-device. Os resultados não atingiram a confiabilidade necessária para um contexto de saúde — e isso reforçou a premissa atual: <strong>onde não pode haver erro, use código determinístico; onde há linguagem, use a ferramenta mais simples que resolve</strong>.
      </p>
    </td>
  </tr>
</table>

---

### 💻 Stack & Tecnologias

<p align="left">
  <!-- Python -->
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <!-- Kotlin -->
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin" />
  <!-- Android -->
  <img src="https://img.shields.io/badge/Android_Compose-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android Compose" />
  <!-- TypeScript -->
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <!-- JavaScript -->
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <!-- Node.js -->
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <!-- PostgreSQL -->
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <!-- Rasa -->
  <img src="https://img.shields.io/badge/Rasa-5A17EE?style=for-the-badge&logo=rasa&logoColor=white" alt="Rasa" />
</p>

---

### ⚙️ CI/CD, Ferramentas & Ecossistema de IA

> *"Trânsito fluido entre automação de pipelines, modelagem de regras de negócio e desenvolvimento orientado por agentes de IA."*

<p align="left">
  <!-- Harness -->
  <img src="https://img.shields.io/badge/Harness-00A4E4?style=for-the-badge&logo=harness&logoColor=white" alt="Harness" />
  <!-- DeepSeek -->
  <img src="https://img.shields.io/badge/DeepSeek-1E293B?style=for-the-badge&logo=deepseek&logoColor=4D6BFE" alt="DeepSeek" />
  <!-- OpenAI Codex -->
  <img src="https://img.shields.io/badge/OpenAI_Codex-10A37F?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI Codex" />
  <!-- Google Antigravity -->
  <img src="https://img.shields.io/badge/Google_Antigravity-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google Antigravity" />
  <!-- Nous Hermes -->
  <img src="https://img.shields.io/badge/Hermes-6366F1?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0id2hpdGUiPjxwYXRoIGQ9Ik0xMiAyTDIgN2wxMCA1IDEwLTUtMTAtNXpNMiAxN2wxMCA1IDEwLTUtMTAtNS0xMCA1em0wLTVsMTAgNSAxMC01LTEwLTUtMTAgNXoiLz48L3N2Zz4=&logoColor=white" alt="Hermes" />
  <!-- OpenCode -->
  <img src="https://img.shields.io/badge/OpenCode-0F172A?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMzhCRkY4IiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI+PHBvbHlsaW5lIHBvaW50cz0iMTYgMTggMjIgMTIgMTYgNiIvPjxwb2x5bGluZSBwb2ludHM9IjggNiAyIDEyIDggMTgiLz48L3N2Zz4=&logoColor=38BFF8" alt="OpenCode" />
  <!-- Git -->
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
</p>

---

### 📌 Competências & Foco de Atuação

- 🌐 **Backend & Microsserviços:** Construção de gateways de API, pipelines de integração em Python e modelagem relacional estruturada em PostgreSQL.
- 📱 **Desenvolvimento Mobile:** Aplicações Android modernas com Kotlin e Compose, offline-first e alta segurança em dados biométricos.
- 🛡️ **Segurança & Governança:** Implementação de princípios Privacy by Design, isolamento multi-tenant, conformidade com a LGPD e fluxos de autenticação sem senhas (OTP).
- 🔄 **Pipelines CI/CD:** Automação de compilação, testes automatizados e releases controlados via Harness.
- 🧠 **IA Conversacional & Motores Determinísticos:** Assistentes com Rasa (NLU e diálogo) combinados a regras de negócio em Kotlin para tarefas críticas sem margem de erro, reduzindo a dependência — e o custo — de inferência em LLMs na nuvem.

---

### 📊 Métricas do GitHub

<p align="center">
  <img src="https://img.shields.io/badge/Repositórios-2_Públicos-7F52FF?style=for-the-badge&logo=github&logoColor=white" alt="Repositórios Públicos" />
  <img src="https://img.shields.io/badge/Seguidores-1-00A4E4?style=for-the-badge&logo=github&logoColor=white" alt="Seguidores" />
  <img src="https://img.shields.io/badge/Status-Ativo-10B981?style=for-the-badge&logo=githubactions&logoColor=white" alt="Status" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Fernandes-Yuri&theme=tokyonight&hide_border=true" alt="Sequência de Contribuições no GitHub" />
</p>

---

### 🌐 Contacto & Conexões
<p align="center">
  <a href="mailto:workfjsyuri@gmail.com" target="_blank">
    <img src="https://img.shields.io/badge/Email-workfjsyuri%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  &nbsp;
  <a href="https://www.linkedin.com/in/yuri-fernandes-901247385" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Yuri_Fernandes-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <br><br>
  <a href="https://huggingface.co/fernandes-yuri" target="_blank">
    <img src="https://img.shields.io/badge/Hugging_Face-fernandes--yuri-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face" />
  </a>
  &nbsp;
  <a href="https://bragasaude.online" target="_blank">
    <img src="https://img.shields.io/badge/Braga_Saúde-bragasaude.online-00A884?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Braga Saúde" />
  </a>
</p>

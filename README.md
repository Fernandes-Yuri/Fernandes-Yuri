# Olá, eu sou o Yuri Fernandes 👋

### 🚀 Engenharia de Software | Sistemas Distribuídos & Mobile

Atuo na concepção, arquitetura e desenvolvimento de sistemas distribuídos, aplicações móveis de alta criticidade e soluções orientadas a microsserviços. Tenho o **Python** como linguagem principal de eleição 🐍, operando com profundidade e solidez em ecossistemas com **Kotlin** (Android nativo, Jetpack Compose, Room), **FastAPI**, **TypeScript**, **React/Next.js** e **PostgreSQL**.

Minha atuação é pautada por rigor de engenharia: desenho arquiteturas que unem **conformidade regulatória (LGPD / RDC 657/2022 SaMD)**, **regras clínicas determinísticas**, **segurança Zero-Trust** e esteiras robustas de integração contínua com **GitHub Actions**. Adoto desenvolvimento assistido por agentes de IA de última geração (**DeepSeek**, **Google Antigravity**, **OpenAI Codex**, **Hermes**, **OpenCode**) para elevar velocidade de entrega e qualidade de cobertura de testes.

---

### 🏥 Ecossistema em Destaque: Braga Saúde

> Plataforma completa de autocuidado clínico preventivo, automonitorização de hábitos e suporte familiar remoto (Modo Cuidador).

<table>
  <tr>
    <td>
      <h3>📱 Plataforma Integrada Braga Saúde</h3>
      <p>
        Solução completa com arquitetura multicamadas, integridade rigorosa de dados clínicos autorreportados (diretrizes SBC, SBD e OMS) e telemetria síncrona/assíncrona entre pacientes e cuidadores.
      </p>
      <ul>
        <li><strong>App Android Nativo (Kotlin &amp; Jetpack Compose):</strong> Arquitetura MVVM/MVI, persistência local cifrada via <strong>Room Database (SQLCipher)</strong>, sincronização resiliente com <strong>WorkManager</strong>, integração <strong>Google Health Connect</strong>, rastreio de passos eficiente via hardware (<code>Sensor.TYPE_STEP_COUNTER</code>) e suporte a exames 100% locais por padrão.</li>
        <li><strong>Site institucional (bragasaude.online):</strong> Landing page, página de download do APK, termos e privacidade, publicados no Firebase Hosting. <em>(O PWA Cuidador em React foi encerrado e é mantido apenas como experiência histórica.)</em></li>
        <li><strong>Portal Administrativo &amp; Operações (Next.js):</strong> Painel de observabilidade com métricas clínicas agregadas, detecção de atividade suspeita (rate limit por IP/UID) e ferramentas de moderação conectadas ao backend.</li>
        <li><strong>Backend Gateway &amp; Microsserviços (FastAPI &amp; Python):</strong> Roteamento de alta performance, processamento de regras clínicas, barramento de segurança com rate limiting, emissão de relatórios médicos executivos em PDF e mensageria WhatsApp Cloud API.</li>
        <li><strong>Dados, Nuvem &amp; Automação:</strong> Infraestrutura na <strong>AWS (EC2 &amp; RDS PostgreSQL)</strong> com porta 22 (SSH) estritamente fechada. Os deploys não são manuais: são 100% automatizados via <strong>GitHub Actions orquestrando AWS SSM</strong> diretamente nas instâncias (zero atalhos humanos), cobrindo migrations, restarts com health check e compilação de APKs assinados com entrega OTA.</li>
      </ul>
      <p>
        🌐 <strong>Conheça a plataforma:</strong> <a href="https://bragasaude.online" target="_blank">bragasaude.online</a>
      </p>
    </td>
  </tr>
</table>

---

### 🧠 Estratégia de IA Híbrida & On-Device: Inteligência sem Desperdício Cloud

> *"Onde não pode haver erro, código determinístico e auditável; onde há linguagem e conversa humana, o modelo mais enxuto e eficiente."*

<table>
  <tr>
    <td>
      <h4>🎙️ Síntese de Voz Nativa Resiliente & Aprendizados On-Device</h4>
      <p>
        A vocalização do assistente clínico é executada via <code>TextToSpeech</code> nativo do sistema operacional com camada de auto-reconexão resiliente, seleção proativa de engines públicas e ciclo de Push-to-Talk fluído.
      </p>
      <ul>
        <li><strong>Custo Zero &amp; Sem Dependência de Nuvem:</strong> A síntese roda 100% no hardware do aparelho, eliminando cobranças recorrentes por caractere em APIs de voz externas.</li>
        <li><strong>Latência Mínima &amp; Push-to-Talk Fluido:</strong> Fim de buffers pesados ou streaming picado; vocalização imediata e encerramento limpo da escuta.</li>
        <li><strong>Arquitetura Descomplicada:</strong> Eliminação de bibliotecas binárias pesadas em C++/JNI, mantendo o APK enxuto (~38 MB) e livre de atritos de inicialização em diferentes fabricantes (Samsung OneUI, Xiaomi, Motorola).</li>
      </ul>
      <p>
        <em>💡 <strong>Lição de Engenharia:</strong> Treinei e implementei uma voz neural própria com fine-tuning em pt-BR baseada em <strong>Piper TTS</strong> e exportação ONNX para execução on-device. Na prática de produção, contudo, a abordagem se mostrou excessivamente complexa — inflava o APK em +48 MB, exigia workers pesados em background e aumentava o consumo de bateria — sem entregar uma qualidade perceptivelmente superior aos sintetizadores modernos já otimizados no próprio sistema operacional (Google Speech Services / Samsung TTS). A decisão técnica pragmática foi aposentar o Piper e manter o TTS nativo com camada de reconexão: custo zero, redução de ~80% no tamanho do app e eliminação total dos problemas de compatibilidade e fragilidade que o Piper trazia.</em>
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <h4>🧩 NLU On-Device em Kotlin + LLM Cloud sob Demanda</h4>
      <p>
        Em vez de enviar toda e qualquer interação a LLMs caros na nuvem sujeitos a alucinações perigosas na área da saúde, a camada conversacional opera em um funil inteligente:
      </p>
      <ul>
        <li><strong>NLU On-Device (Kotlin puro):</strong> Classificação de intenções e extração de entidades clínicas com regex e regras especializadas em saúde preventiva e regionalismos brasileiros, executadas 100% no aparelho (sem runtime Python, sem cobrança por token). O que o roteador não reconhece é delegado à LLM cloud.</li>
        <li><strong>Motor Determinístico Nativo (Kotlin On-Device):</strong> Tarefas críticas com <strong>tolerância zero a falhas</strong> — triagem de emergência médica (SAMU 192), horários e estoques de medicamentos, validação de limites de pressão/glicemia e regras de escalonamento — são executadas por algoritmos estritos com cobertura de testes unitários diretamente no app.</li>
        <li><strong>LLM Cloud sob Demanda:</strong> Modelos maiores em nuvem (ex: Groq Cloud) atuam estritamente como retaguarda para diálogos abertos não mapeados.</li>
      </ul>
      <p>
        <em>💡 <strong>Lição de Engenharia:</strong> Testei o fine-tuning de um SLM (Qwen 0.5B) para rodar inteiramente on-device. Os resultados práticos evidenciaram que, para limites de segurança clínica e saúde geriátrica, modelos estocásticos de pequeno porte oferecem risco de inconsistência inaceitável. A solução adotada foi combinar NLU em Kotlin on-device para linguagem com lógica determinística para precisão matemática — o Rasa, avaliado em fases de projeto, não está integrado ao app em produção.</em>
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <h4>📄 Triagem de Receitas &amp; Exames com Tolerância Zero a Erro</h4>
      <p>
        Pipeline de conferência rigorosa para mitigar riscos regulatórios (SaMD RDC 657/2022):
      </p>
      <ul>
        <li><strong>Análise de Receitas em 3 Motores:</strong> OCR estrito (PyMuPDF) + Visão Multimodal (Gemini Flash com fallback Groq) + <strong>Árbitro ANVISA</strong> cruzando catálogo farmacológico. Divergências forçam conferência humana antes de salvar — o sistema jamais "adivinha" dosagens.</li>
        <li><strong>Exames com Processamento On-Device &amp; Nuvem Opcional:</strong> OCR local via ML Kit com filtro Laplaciano contra imagens borradas e higienização automática de PII (remoção de CPF e dados de laboratório). Por padrão, exames ficam no dispositivo do paciente e a sincronização com nuvem é opcional e expressamente autorizada.</li>
      </ul>
    </td>
  </tr>
</table>

---

### 💻 Stack & Tecnologias

<p align="left">
  <!-- Python -->
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <!-- FastAPI -->
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
  <!-- Kotlin -->
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin" />
  <!-- Android -->
  <img src="https://img.shields.io/badge/Android_Compose-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android Compose" />
  <!-- TypeScript -->
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <!-- Next.js -->
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <!-- PostgreSQL -->
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <!-- AWS -->
  <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white" alt="AWS" />
  <!-- ONNX -->
  <img src="https://img.shields.io/badge/ONNX-005CED?style=for-the-badge&logo=onnx&logoColor=white" alt="ONNX" />
</p>

---

### ⚙️ CI/CD, Ferramentas & Engenharia com IA

> *"Automação contínua e pipelines declarativos complementados pela alavancagem de agentes de IA na engenharia de software."*

<p align="left">
  <!-- GitHub Actions -->
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions" />
  <!-- Docker -->
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <!-- DeepSeek -->
  <img src="https://img.shields.io/badge/DeepSeek-1E293B?style=for-the-badge&logo=deepseek&logoColor=4D6BFE" alt="DeepSeek" />
  <!-- Google Antigravity -->
  <img src="https://img.shields.io/badge/Google_Antigravity-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google Antigravity" />
  <!-- OpenAI Codex -->
  <img src="https://img.shields.io/badge/OpenAI_Codex-10A37F?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI Codex" />
  <!-- Nous Hermes -->
  <img src="https://img.shields.io/badge/Hermes-6366F1?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0id2hpdGUiPjxwYXRoIGQ9Ik0xMiAyTDIgN2wxMCA1IDEwLTUtMTAtNXpNMiAxN2wxMCA1IDEwLTUtMTAtNS0xMCA1em0wLTVsMTAgNSAxMC01LTEwLTUtMTAgNXoiLz48L3N2Zz4=&logoColor=white" alt="Hermes" />
  <!-- OpenCode -->
  <img src="https://img.shields.io/badge/OpenCode-0F172A?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMzhCRkY4IiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI+PHBvbHlsaW5lIHBvaW50cz0iMTYgMTggMjIgMTIgMTYgNiIvPjxwb2x5bGluZSBwb2ludHM9IjggNiAyIDEyIDggMTgiLz48L3N2Zz4=&logoColor=38BFF8" alt="OpenCode" />
  <!-- Git -->
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
</p>

---

### 📌 Competências & Foco de Atuação

- 🌐 **Backend, APIs & Microsserviços:** Construção de gateways de alto throughput em FastAPI, barramentos de mensageria, modelagem relacional avançada com PostgreSQL e migrations seguras.
- 📱 **Engenharia Mobile Nativa (Android):** Domínio de Kotlin moderno, Jetpack Compose, bancos locais protegidos (Room + SQLCipher), processamento assíncrono (WorkManager) e serviços de plataforma (TextToSpeech resiliente, SpeechRecognizer, Health Connect).
- 🛡️ **Segurança, Governança & LGPD:** Princípios de Privacy by Design, isolamento multi-tenant, sanitização determinística de dados sensíveis (PII), auditoria granular de acessos e conformidade com a regulação SaMD (RDC 657/2022).
- 🔄 **DevOps & Integração Contínua:** Esteiras 100% automatizadas no GitHub Actions com gatekeepers de lint/testes, compilação de APKs assinados e deploys na AWS orquestrados via SSM (processo totalmente automatizado via pipeline, sem intervenção manual, mantendo a porta 22/SSH fechada).
- 🧠 **IA Pragmática & Eficiente:** Arquitetura de IA híbrida orientada a custo sustentável — NLU determinístico em Kotlin on-device, vocalização nativa resiliente (TTS do sistema operacional), regras clínicas estritas com testes unitários e integração com LLMs de ponta apenas onde agregam valor real.

---

### 📊 Métricas do GitHub

<p align="center">
  <img src="https://img.shields.io/badge/Status-Ativo-10B981?style=for-the-badge&logo=githubactions&logoColor=white" alt="Status" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Fernandes-Yuri&theme=tokyonight&hide_border=true" alt="Sequência de Contribuições no GitHub" />
</p>

---

### 🌐 Contato & Conexões
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

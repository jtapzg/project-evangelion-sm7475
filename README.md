 ⚙️ Project Evangelion v3.0

![Magisk](https://img.shields.io/badge/Magisk-Compatible-00AF9C?style=for-the-badge&logo=magisk)
![KernelSU](https://img.shields.io/badge/KernelSU-Compatible-10B981?style=for-the-badge)
![Device](https://img.shields.io/badge/Device-Poco_F5_(SM7475)-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-GPL%203.0-lightgrey?style=for-the-badge)

**Project Evangelion** é um módulo de *kernel tuning* e otimização extrema, desenvolvido especificamente para extrair 100% do hardware do **Poco F5 (SM7475 / Snapdragon 7+ Gen 2)**. 

O coração do projeto é a **EVA Sync Engine**: um daemon inteligente (escrito do zero) que monitora uso de CPU, GPU, temperatura e a engine do jogo em tempo real, adaptando o celular dinamicamente para garantir FPS máximo sem fritar o aparelho.



## 🔥 Principais Funcionalidades (Features)

* **🤖 EVA Sync Engine (Adaptive Daemon):** Lê parâmetros do sistema a cada 2 segundos e alterna entre 5 modos automáticos: `IDLE`, `NORMAL`, `COMBAT`, `BERSERK` e `THERMAL`.
* **🚀 GPU Burst Mode Dinâmico:** Destrava os clocks, buses e rails da GPU (Adreno 725) forçando a performance máxima apenas quando um jogo pesado é detectado.
* **🌡️ Smart Thermal Control (Fail-safe):** Proteção real de hardware. Se a temperatura bater 50°C, o módulo corta os boosts, ativa o *throttling* seguro e relaxa o scheduler (6ms latência) para resfriar o SoC imediatamente.
* **🎯 Game Thread Pinning & Schedtune:** Isola as threads pesadas dos jogos (Unity, Unreal, Godot) nos núcleos A715 (Big + Prime) usando `taskset f0` e prioridade máxima.
* **⚡ Game Loading Boost:** Ao abrir um jogo, a GPU é forçada ao clock máximo por 30 segundos para engolir telas de loading. Caches RAM antigos são limpos automaticamente (`drop_caches`).
* **📱 SurfaceFlinger Optimizer:** Ajusta os *phase offsets* de renderização da tela dinamicamente de acordo com a sua taxa de atualização (60Hz / 90Hz / 120Hz) para eliminar *micro-stutters*.
* **🌐 Network Low Latency:** Ativação instantânea de BBR, `tcp_low_latency` e `tcp_nodelay` durante o gameplay para derrubar o ping.


 📊 Monitoramento em Tempo Real (WebUI)
O Evangelion possui uma interface web integrada para monitoramento. Se você usa o **MMRL** ou o app do **KernelSU**, pode acessar a WebUI para ver gráficos em tempo real de:
* Uso de CPU e GPU (%)
* Temperatura (°C)
* Modo atual da EVA Engine
* App em primeiro plano


 ⚠️ Requisitos e Compatibilidade
* **Dispositivo Mínimo:** Poco F5 (`marble` / `marblein`) ou aparelhos com SoC Snapdragon SM7475. *Não use em hardwares mais fracos!*
* **Root Necessário:** Magisk (v24+), KernelSU ou APatch.
* **Aviso:** Este módulo altera profundamente propriedades de I/O, governadores de GPU/CPU, ZRAM e gerenciamento de rede. **Use por sua própria conta e risco.**



 📦 Como Instalar

1. Baixe o arquivo `project-evangelion-v3.0-SM7475.zip` localizado na página inicial (ou na aba [Releases](../../releases)).
2. Abra o seu gerenciador de Root (Magisk, KernelSU ou APatch).
3. Vá na aba de Módulos e selecione "Instalar a partir do armazenamento".
4. Selecione o arquivo `.zip` baixado.
5. Reinicie o dispositivo.
6. Aguarde a notificação toast: Projeto EVANGELION ativo.

 🗑️ Como Desinstalar
Basta desativar ou remover o módulo pelo seu gerenciador de root e reiniciar o aparelho. Todos os parâmetros do kernel e propriedades do sistema voltarão ao estado Stock automaticamente.


*Desenvolvido com ☕ e foco extremo em performance adptavel.*

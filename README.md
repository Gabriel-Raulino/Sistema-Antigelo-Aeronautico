# ✈️ Aeronautical Anti-Ice System (De-Ice Boots) / Sistema Antigelo Aeronáutico

<details>
<summary>🇺🇸 <b>Read in English</b></summary>
<br>

This project consists of an advanced embedded monitoring and control system designed to prevent ice formation on aircraft wings. The system uses a network of sensors and actuators to analyze environmental conditions in real time and trigger de-icing mechanisms (inflatable rubber boots) as needed.

### 🛠️ Technical Specifications
* **Microcontroller:** Microchip PIC16F877A.
* **Language:** C (XC8 Compiler).
* **Development Environment:** MPLAB X IDE v5.35.
* **Simulation and Design:** Proteus (Schematic and PCB).
* **Interface:** 16x2 LCD Display.

### 📡 System Architecture

#### Inputs (Analog Sensors)
The system acquires data via A/D conversion to monitor:
* **Internal/External Temperature:** Using LM35 sensors.
* **Humidity and Pressure:** Simulated via potentiometers for critical condition analysis.
* **Manual Override:** Implemented via hardware interrupts, allowing immediate system activation by the pilot.

#### Outputs and Actuators
* **Visual Interface:** LCD display showing real-time temperature, humidity, and pressure.
* **Status Indicators (LEDs):**
    * 🟢 **Green:** Operation within normal parameters.
    * 🟡 **Yellow:** Warning of approaching critical limits.
    * 🔴 **Red:** Critical situation with response system activation.
* **Active Response:** Activation of a **Buzzer** (sound alarm), **Heating Resistor**, and **Compressor** to inflate the anti-ice boots.

### ⚙️ Operation and Processing Logic
The firmware continuously processes data and executes conditional responses based on predefined thresholds:

1. **Monitoring:** Collection and conversion of analog signals from sensors.
2. **Comparison:** Dynamic evaluation of readings against minimum and maximum levels.
3. **Maintenance Tracking (Timer):** The system utilizes the `TMR1L` and `TMR1H` registers to create a 16-bit counter that records the total number of compressor activations, facilitating later analysis and preventive maintenance.

### 🚀 How to Run (Simulation)

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Gabriel-Raulino/Sistema-Antigelo-Aeronautico.git
   ```
2. **Compile the Firmware:**
   * Open the project in **MPLAB X IDE (v5.35)**.
   * Ensure the **XC8 Compiler** is configured.
   * Build the project to generate the `.hex` executable file.
3. **Run the Simulation:**
   * Open the circuit schematic file in **Proteus** (`Sistema Antigelo.pdsprj`).
   * Double-click the PIC16F877A microcontroller in the schematic.
   * In the "Program File" field, load the generated `.hex` file.
   * Click Play to start the simulation and interact with the potentiometers and switches.

---
**Developed by:** Gabriel Raulino Dal Pont & Danilo Silveira Ramos.

</details>

<details>
<summary>🇧🇷 <b>Ler em Português (BR)</b></summary>
<br>

Este projeto consiste em um sistema avançado de monitoramento e controle embarcado projetado para prevenir a formação de gelo nas asas de aeronaves. O sistema utiliza uma malha de sensores e atuadores para analisar condições ambientais em tempo real e acionar mecanismos de degelo (borrachas infláveis) conforme a necessidade.

### 🛠️ Especificações Técnicas
* **Microcontrolador:** Microchip PIC16F877A.
* **Linguagem:** C (Compilador XC8).
* **Ambiente de Desenvolvimento:** MPLAB X IDE v5.35.
* **Simulação e Design:** Proteus (Esquemático e PCB).
* **Interface:** Display LCD 16x2.

### 📡 Arquitetura do Sistema

#### Entradas (Sensores Analógicos)
O sistema realiza a aquisição de dados via conversão A/D para monitorar:
* **Temperatura Interna/Externa:** Utilizando sensores LM35.
* **Umidade e Pressão:** Simuladas através de potenciômetros para análise de condições críticas.
* **Acionamento Manual:** Implementado via interrupção de hardware, permitindo a ativação imediata do sistema pelo piloto.

#### Saídas e Atuadores
* **Interface Visual:** Display LCD exibindo temperaturas, umidade e pressão em tempo real.
* **Indicadores de Status (LEDs):**
    * 🟢 **Verde:** Operação dentro dos parâmetros normais.
    * 🟡 **Amarelo:** Alerta de aproximação de limites críticos.
    * 🔴 **Vermelho:** Situação crítica com ativação dos sistemas de resposta.
* **Resposta Ativa:** Acionamento de **Buzzer** (alarme sonoro), **Resistência** de aquecimento e **Compressor** para inflar as borrachas antigelo.

### ⚙️ Lógica de Operação e Processamento
O firmware processa continuamente os dados e executa respostas condicionais baseadas em limites predefinidos:

1. **Monitoramento:** Coleta e conversão dos sinais analógicos dos sensores.
2. **Comparação:** Avaliação dinâmica das leituras contra níveis mínimos e máximos.
3. **Controle de Manutenção (Timer):** O sistema utiliza os registradores `TMR1L` e `TMR1H` para criar um contador de 16 bits que registra o número total de ativações do compressor, facilitando análises posteriores e manutenção preventiva.

### 🚀 Como Executar (Simulação)

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/Gabriel-Raulino/Sistema-Antigelo-Aeronautico.git
   ```
2. **Compile o Firmware:**
   * Abra o projeto no **MPLAB X IDE (v5.35)**.
   * Certifique-se de que o compilador **XC8** está configurado.
   * Faça o Build (compilação) do projeto para gerar o arquivo executável `.hex`.
3. **Rode a Simulação:**
   * Abra o arquivo de esquema elétrico no **Proteus** (`Sistema Antigelo.pdsprj`).
   * Dê um duplo clique no microcontrolador PIC16F877A no circuito.
   * No campo "Program File", carregue o arquivo `.hex` gerado no passo anterior.
   * Clique em Play para iniciar a simulação e interaja com os potenciômetros e botões.

---
**Desenvolvido por:** Gabriel Raulino Dal Pont & Danilo Silveira Ramos.

</details>

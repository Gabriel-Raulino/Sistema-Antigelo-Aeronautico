# ✈️ Sistema Antigelo Aeronáutico (De-Ice Boots)

Este projeto consiste em um sistema avançado de monitoramento e controle embarcado projetado para prevenir a formação de gelo nas asas de aeronaves. O sistema utiliza uma malha de sensores e atuadores para analisar condições ambientais em tempo real e acionar mecanismos de degelo (borrachas infláveis) conforme a necessidade.

## 🛠️ Especificações Técnicas
* **Microcontrolador:** Microchip PIC16F877A.
* **Linguagem:** C (Compilador XC8).
* **Simulação e Design:** Proteus (Esquemático e PCB).
* **Interface:** Display LCD 16x2.

## 📡 Arquitetura do Sistema

### Entradas (Sensores Analógicos)
O sistema realiza a aquisição de dados via conversão A/D para monitorar:
* **Temperatura Interna/Externa:** Utilizando sensores LM35.
* **Umidade e Pressão:** Simuladas através de potenciômetros para análise de condições críticas.
* **Acionamento Manual:** Implementado via interrupção, permitindo a ativação imediata do sistema pelo piloto

### Saídas e Atuadores
* **Interface Visual:** Display LCD exibindo temperaturas, umidade e pressão em tempo real.
* **Indicadores de Status (LEDs):**
    * 🟢 **Verde:** Operação dentro dos parâmetros normais.
    * 🟡 **Amarelo:** Alerta de aproximação de limites críticos.
    * 🔴 **Vermelho:** Situação crítica com ativação dos sistemas de resposta.
* **Resposta Ativa:** Acionamento de **Buzzer** (alarme sonoro), **Resistência** de aquecimento e **Compressor** para inflar as borrachas antigelo.

## ⚙️ Lógica de Operação e Processamento
O firmware processa continuamente os dados e executa respostas condicionais baseadas em limites predefinidos:

1. **Monitoramento:** Coleta e conversão dos sinais analógicos dos sensores.
2. **Comparação:** Avaliação dinâmica das leituras contra níveis mínimos e máximos.
3. **Controle de Manutenção (Timer):** O sistema utiliza os registradores **TMR1L** e **TMR1H** para criar um contador de 16 bits que registra o número total de ativações do compressor, facilitando análises posteriores e manutenção preventiva.

---
**Desenvolvido por:** Gabriel Raulino Dal Pont & Danilo Silveira Ramos.

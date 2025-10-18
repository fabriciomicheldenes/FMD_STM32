# Estudo progressivo do STM32 — de HAL a Bare-Metal e FreeRTOS

Este repositório tem como objetivo documentar o aprendizado progressivo da programação de microcontroladores STM32, começando com a linha **Blue Pill (STM32F103C8T6)** e evoluindo em camadas de abstração e complexidade.

---

## 🎯 Objetivos principais

1. **Compreender e dominar a HAL (Hardware Abstraction Layer)** da ST, configurando manualmente periféricos sem depender da CubeMX.
2. **Implementar e documentar o USB-CDC** (dispositivo serial virtual), desde o setup básico até o envio/recebimento de dados com buffers circulares.
3. **Migrar gradualmente para níveis mais baixos**, explorando:
   - libopencm3
   - registradores diretos (bare-metal)
   - FreeRTOS para multitarefa e sincronização
4. **Adotar práticas modernas de engenharia de firmware**:
   - uso de **CMake** e **VSCode**
   - integração de **testes unitários** (baseado no livro *Test-Driven Development for Embedded C*)
   - depuração com **JTAG/SWD** e OpenOCD
   - controle de versão limpo e modular

---

## 📚 Estrutura planejada

stm32f103-hal-to-baremetal/

├── 00_docs/ # Tutoriais, notas e diagramas

├── 01_hal_usb_cdc/ # Projeto inicial com HAL e USB-CDC

├── 02_libopencm3/ # Versão equivalente usando libopencm3

├── 03_baremetal/ # Reimplementação direta com registradores

├── 04_freertos_usb/ # USB-CDC + FreeRTOS + multitarefa

├── 05_tests/ # Testes unitários (Unity/Ceedling)

├── CMakeLists.txt

└── README.md


---

## 🧰 Ferramentas

- **Compilador:** `arm-none-eabi-gcc`  
- **Build system:** `CMake`  
- **Editor:** `Visual Studio Code`  
- **Debug:** `OpenOCD + ST-Link V2`  
- **Testes:** `Ceedling / Unity`  
- **Documentação:** Markdown + Doxygen

---

## 🚀 Etapas de aprendizado

| Etapa | Tópico | Status |
|-------|--------|--------|
| 1 | Configuração do ambiente (CMake, toolchain, OpenOCD) | 🔜 |
| 2 | Blink LED básico com HAL sem CubeMX | 🔜 |
| 3 | USB-CDC com HAL manual | 🔜 |
| 4 | Reimplementação USB-CDC com libopencm3 | 🔜 |
| 5 | Comunicação serial + buffers circulares | 🔜 |
| 6 | Testes unitários em firmware | 🔜 |
| 7 | FreeRTOS + USB + Debug | 🔜 |
| 8 | Bare-metal total | 🔜 |

---

## 💡 Filosofia do projeto

> “Aprender de cima para baixo e de baixo para cima ao mesmo tempo.”  
> — Compreender o que a HAL faz *por dentro* e como o hardware realmente funciona, reduzindo dependências e aumentando o domínio sobre o microcontrolador.

---

## 📜 Licença

Este projeto é distribuído sob a licença MIT.

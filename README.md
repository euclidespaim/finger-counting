# 🖐️ Finger Counting & Libras Recognition

![GitHub repo size](https://img.shields.io/github/repo-size/euclidespaim/finger-counting?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/euclidespaim/finger-counting?style=for-the-badge)
![GitHub topics](https://img.shields.io/github/topics/euclidespaim/finger-counting?style=for-the-badge)

Este projeto une **Visão Computacional** e **Sistemas Embarcados** para criar uma interface de reconhecimento de sinais baseada na contagem de dedos, com foco em aplicações de acessibilidade e tradução básica de Libras.

---

## 🎯 Objetivo
O objetivo principal é utilizar a câmera para detectar a mão do usuário, contar os dedos estendidos através de algoritmos de processamento de imagem e enviar esses dados para um **Arduino**, que pode reagir fisicamente (ex: acender LEDs, mover servos ou exibir em um display).

## 🛠 Tecnologias e Ferramentas
- **Python**: Linguagem principal para o processamento de imagem.
- **OpenCV**: Biblioteca para visão computacional.
- **MediaPipe**: Framework do Google para detecção de mãos e pontos de articulação.
- **C++ / Arduino IDE**: Programação do microcontrolador.
- **Firmata / Serial Protocol**: Comunicação entre o computador e o hardware.

## ⚙️ Funcionamento
1. **Captura**: A webcam captura o vídeo em tempo real.
2. **Processamento**: O script Python identifica a mão e extrai os marcos (landmarks) dos dedos.
3. **Lógica de Contagem**: Com base na posição das pontas dos dedos em relação às articulações, o sistema determina quantos dedos estão abertos.
4. **Interação**: O valor é enviado via porta Serial para o Arduino, executando uma ação programada.

## 📂 Estrutura do Projeto
- `/python`: Scripts para detecção e contagem de dedos.
- `/arduino`: Código (`.ino`) para ser carregado no microcontrolador.
- `/assets`: Imagens e demonstrações do projeto.

## 🚀 Como Executar
1. Clone o repositório:
   ```bash
   git clone https://github.com/euclidespaim/finger-counting.git
   ```
2. Instale as dependências:
   ```bash
   pip install opencv-python mediapipe pyserial
   ```
3. Carregue o código do Arduino usando a Arduino IDE.
4. Execute o script principal:
   ```bash
   python main.py
   ```

## 🤝 Contribuições
Sinta-se à vontade para abrir **Issues** ou enviar **Pull Requests** com melhorias na precisão da detecção ou novos recursos de interação.

---
Desenvolvido por [Euclides Paim](https://euclidespaim.com).

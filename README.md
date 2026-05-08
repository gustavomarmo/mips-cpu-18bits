# Processador MIPS Simplificado — Logisim

Projeto acadêmico de implementação de um processador MIPS simplificado (8 bits, 8 registradores) desenvolvido no simulador de circuitos digitais **Logisim**.

---

## 📋 Descrição do Projeto

O circuito implementa uma arquitetura MIPS monociclo reduzida, composta pelos seguintes módulos:

- **Unidade de Controle** — decodifica o opcode e gera os sinais de controle (MemRead, MemWrite, RegWrite, ALUSrc, Branch, Jump, ALUOp, MemToReg).
- **Banco de Registradores** — 8 registradores de 8 bits (R0–R7) com leitura dupla e escrita controlada.
- **ULA (Unidade Lógico-Aritmética)** — suporta soma, subtração, multiplicação, divisão, negação, comparação e deslocamentos (shift esquerda/direita).
- **Controle da ULA** — seleciona a operação da ULA com base nos campos `ALUOp` e `Funct`.
- **Memória de Instruções (ROM)** — armazena o programa a ser executado.
- **Memória de Dados (RAM)** — utilizada nas instruções de load/store.
- **PC (Program Counter)** — registrador que controla o fluxo de execução, com suporte a desvios e saltos.

O programa de simulação inclui uma sequência de instruções que exercita as principais funcionalidades do processador.

---

## 👥 Integrantes

| Nome                      | Registro Acadêmico |
| ------------------------- | ------------------ |
| Diogo Santos Rodrigues    | 082230002          |
| Leonardo Rosário Teixeira | 082230012          |
| Bianca Ricci Lima         | 082230019          |
| Ryan Corazza Alvarenga    | 082230024          |
| Gustavo Sgrignoli Marmo   | 082230028          |

---

## ▶️ Instruções de Execução

### Pré-requisitos

- [Logisim 2.7.x](http://www.cburch.com/logisim/) instalado (requer Java).

### Passos

1. **Abrir o circuito**
   - Inicie o Logisim.
   - Vá em `File → Open` e selecione o arquivo `MIPS.circ`.

2. **Carregar o programa de simulação**
   - Na memória de instruções (ROM), clique com o botão direito e selecione **Edit Contents**.
   - Importe o arquivo `programa_simulacao` (formato raw `.hex`) ou cole o conteúdo manualmente.

3. **Configurar a simulação**
   - Certifique-se de que o clock está ativo. Vá em `Simulate → Tick Frequency` para ajustar a velocidade.
   - Para executar passo a passo, use `Simulate → Step Simulation` (`Ctrl+T`).
   - Para execução contínua, ative `Simulate → Ticks Enabled` (`Ctrl+K`).

4. **Resetar o circuito**
   - Use `Simulate → Reset Simulation` (`Ctrl+R`) para reiniciar o PC e os registradores antes de uma nova execução.

5. **Observar os resultados**
   - Acompanhe os valores dos registradores no módulo **Banco de Registradores**.
   - Verifique os sinais de controle na **Unidade de Controle**.
   - Observe as saídas da **ULA** e o estado da **RAM** durante operações de memória.

---

## 🎥 Vídeo Explicativo

> 🔗 **[https://youtu.be/4JYcedKk87A]**

---

## 📁 Arquivos do Projeto

| Arquivo              | Descrição                                    |
| -------------------- | -------------------------------------------- |
| `MIPS.circ`          | Circuito principal do processador no Logisim |
| `programa_simulacao` | Programa de teste em formato hexadecimal raw |
| `README.md`          | Este arquivo                                 |

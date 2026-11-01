## prjExemploGUI2
Primeira aplicação gráfica (**Java Swing**) da série: um formulário simples de **cálculo do valor de uma compra** a partir do preço unitário e da quantidade vendida.

## Conceitos abordados

- Criação de interface gráfica com `JFrame`, `JLabel`, `JTextField` e `JButton`
- Tratamento de eventos de clique (`ActionListener`)
- Conversão de texto em número (`Double.parseDouble`, `Integer.parseInt`)
- Exibição de resultado em um `JLabel`
- Manipulação de foco (`requestFocus`)

## Funcionalidades

A janela **"Exemplo Gui 02"** possui os campos e botões abaixo.

| Componente | Função |
|---|---|
| Código | Código do produto (informativo) |
| Descrição | Descrição do produto (informativo) |
| Preço Unitário | Valor unitário (número decimal) |
| Qtde. Vendida | Quantidade (número inteiro) |
| Valor da compra | Resultado exibido pelo programa |
| **Calcular** | Calcula `preço unitário × quantidade` e exibe o resultado |
| **Limpar** | Esvazia todos os campos e devolve o foco ao campo Código |
| **Sair** | Fecha a janela |

## Estrutura do projeto

```
prjExemploGui2/
├── src/
│   ├── GuiExemplo2.java      # Classe da janela (JFrame) e método main
│   └── GuiExemplo2.form      # Desenho da interface (editor visual do NetBeans)
├── build/ e dist/            # Arquivos gerados pela compilação (incluindo o .jar)
├── nbproject/                # Configuração do NetBeans
├── build.xml                 # Script Ant
└── manifest.mf
```

> O trecho `initComponents()` é **gerado automaticamente** pelo NetBeans a partir do `.form`. Edite a interface pelo editor visual, não direto nesse bloco.

## Observações

- O ponto decimal do preço deve ser digitado com **ponto** (ex.: `12.50`), e a quantidade deve ser um número inteiro.
- Não há validação de entrada: clicar em **Calcular** com campos vazios ou com texto inválido gera uma `NumberFormatException` no console e o resultado não é atualizado.

## Requisitos

- **JDK 8** ou superior (o projeto está configurado com `javac.source=1.8`)
- Ambiente com interface gráfica (a aplicação abre uma janela Swing)
- Opcional: **Apache NetBeans**, já que a interface foi desenhada no editor visual (arquivo `.form`)

## Como executar

### Pelo NetBeans

1. `File > Open Project…` e selecione a pasta `prjExemploGui2`.
2. Clique com o botão direito no projeto e escolha **Run** (ou pressione `F6`).

### Pela linha de comando

```bash
mkdir out
javac -encoding UTF-8 -d out src/GuiExemplo2.java
java -cp out GuiExemplo2
```

Também é possível usar o JAR já gerado na pasta `dist/`, que reflete a última compilação feita no NetBeans:

```bash
java -jar dist/prjExemploGui2.jar
```

## Autor

Vinícius Gonçalo

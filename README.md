# Gerador de Matriz Ybus

Este projeto gera automaticamente a matriz Ybus para qualquer circuito elétrico, a partir de informações fornecidas interativamente pelo usuário.

## 🚀 Objetivo

- Permitir que o usuário informe o número de nós (barras) do circuito.
- Informar as conexões entre os nós e os valores de admitância complexa.
- Informar as ligações dos nós com a Terra.
- Calcular e construir a matriz de admitâncias nodal \( Y_{\text{bus}} \).

## 📚 Como usar

1. **Executar o programa** (`CalculatedYbus.ipynb`) em um ambiente Python ou Google Colab.
2. **Responda às perguntas** que o programa faz:
   - Quantos nós (barras) o circuito tem.
   - Para cada nó:
     - Se ele está conectado a outro nó (e informar a qual).
     - Informar a admitância complexa entre os nós (por exemplo: `0.5+5j`).
   - Informar se há ligação com a Terra para cada nó, e o valor da admitância.

3. **Atenção**: 
   - Cada conexão entre dois nós deve ser informada apenas **uma vez**.
   - Se o nó 1 já está conectado ao nó 2, **não informe** depois que o nó 2 está conectado ao nó 1 novamente.  
   - Evitar repetir conexões mantém a matriz correta.

4. O programa irá calcular e exibir a matriz Ybus final, pronta para análise.

## ⚡ Exemplo rápido

Usuário responde:

- 4 nós
- Conexões:
  - Nó 1 conectado ao 2 (admitância 0.5+5j)
  - Nó 1 conectado ao 3 (admitância 0.8+8j)
  - Nó 2 conectado ao 3 (admitância 0.6+6j)
  - Nó 3 conectado ao 4 (admitância 1.6+16j)
- Conexões à Terra:
  - Nó 1 (0.1+1j)
  - Nó 2 (0.2+2j)
  - Nó 3 (0.3+3j)
  - Nó 4 (0.4+4j)

O programa monta automaticamente a matriz \( Y_{\text{bus}} \).

## 🛠️ Requisitos

- Python 3.7+
- Bibliotecas:
  - `numpy`

(Opcionalmente, `pandas` para organizar melhor a tabela.)

## 📄 Licença

Este projeto é livre para uso acadêmico e pessoal.

---

Criado por [Gabriel Teperino Percegoni Figueira] 🚀

# A Estrutura do Catecismo

O catecismo está dividido em **`quatro partes`**. São elas:

- A profissão da fé;
- Os sacramentos da fé;
- A vida da fé;
- A oração cristã;

Cada **`parte`** do Catecismo é formada por **`seções`** e cada seção é dividida por
**`capítulos`**.

```mermaid
graph TD
    Catecismo --> Parte1[Profissão da Fé]
    Catecismo --> Parte2[Sacramentos da Fé]
    Catecismo --> Parte3[Vida da Fé]
    Catecismo --> Parte4[Oração Cristã]

    Parte1 --> Secao1_1[Seções]

    Parte2 --> Secao2_1[Seções]

    Parte3 --> Secao3_1[Seções]

    Parte4 --> Secao4_1[Seções]

    Secao1_1 --> Capitulo1_1_1[Capítulos]

    Secao2_1 --> Capitulo2_1_1[Capítulos]

    Secao3_1 --> Capitulo3_1_1[Capítulos]

    Secao4_1 --> Capitulo4_1_1[Capítulos]
```

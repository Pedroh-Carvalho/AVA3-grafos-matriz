# Programa de Grafos (Matriz de Adjacência)

Descrição
---------

Programa em C que implementa um manipulador simples de grafos não direcionados usando matriz de adjacência. Permite limpar o grafo, inserir/remover arestas, mostrar a matriz de adjacência, calcular o grau dos vértices e listar adjacências.

Características
---------------
- **Representação:** Matriz de adjacência (`graph[][]`).
- **Tipo do grafo:** Não direcionado (arestas espelham-se em ambos os vértices).
- **Limite:** Número máximo de vértices definido por `MAX_VERTICES` (valor padrão 100).
- **Interação:** Menu interativo via terminal.

Requisitos
---------

- Compilador C (por exemplo `gcc`).

Arquivos
--------
- [main.c](main.c#L1-L400): Código fonte do programa.

Como compilar
--------------

No Windows (MinGW / MSYS) ou Linux com `gcc` instalado, execute:

```bash
gcc main.c -o grafo
```

No Windows com gerador de executável, o arquivo resultante será `grafo.exe`; em UNIX será `grafo`.

Como executar
--------------

Execute o binário gerado e siga o menu:

```bash
./grafo        # ou grafo.exe no Windows
```

Exemplo de uso rápido
---------------------
1. Ao iniciar, informe a quantidade de vértices (por exemplo `5`).
2. Use a opção `2` para inserir/remover arestas, informe os vértices de origem e destino e escolha `1` para adicionar ou `2` para remover.
3. Use a opção `3` para visualizar a matriz de adjacência.
4. Use a opção `4` para ver o grau de cada vértice.
5. Use a opção `5` para listar adjacências de cada vértice.
6. Use `6` para sair.

Observações e limitações
------------------------
- O programa não valida entradas não numéricas — entradas inválidas podem causar comportamento indesejado.
- Número máximo de vértices é fixo por `MAX_VERTICES`.
- A implementação usa `scanf`, portanto é sensível a formatos de entrada.

Possíveis melhorias
-------------------
- Substituir `scanf` por leitura de linha (`fgets`) e parsing seguro para lidar com entradas inválidas.
- Permitir grafos direcionados como opção.
- Salvar/carregar grafos de arquivos.
- Implementar busca (BFS/DFS) e detecção de componentes.

Licença
-------
Use livremente para fins educacionais. Sinta-se à vontade para adaptar e melhorar.

Exemplo de sessão (detalhado)
-----------------------------
Segue um exemplo completo de interação com o programa (entradas do usuário marcadas como "->"): 

```
Quantidade de vértices: -> 4

Grafo limpo com sucesso!

 MENU DO GRAFO 
1 - Limpar grafo
2 - Inserir/remover aresta
3 - Mostrar matriz
4 - Mostrar graus
5 - Mostrar adjacências
6 - Sair
Opção: -> 2

Vértice de origem: -> 0

Vértice de destino: -> 1
1 - Adicionar aresta
2 - Remover aresta
Opção: -> 1
Aresta atualizada com sucesso!!

 MENU DO GRAFO 
Opção: -> 2

Vértice de origem: -> 0

Vértice de destino: -> 2
1 - Adicionar aresta
2 - Remover aresta
Opção: -> 1
Aresta atualizada com sucesso!!

 MENU DO GRAFO 
Opção: -> 3

Matriz de adjacencia
	0 1 2 3
 0 |  0 1 1 0
 1 |  1 0 0 0
 2 |  1 0 0 0
 3 |  0 0 0 0

 MENU DO GRAFO 
Opção: -> 5

LISTA de ADJACÊNCIAS
0 ->  1 2
1 ->  0
2 ->  0
3 -> Nenhum

 MENU DO GRAFO 
Opção: -> 4

GRAU DOS VÉRTICES

Vértice 0 -> Grau 2
Vértice 1 -> Grau 1
Vértice 2 -> Grau 1
Vértice 3 -> Grau 0

 MENU DO GRAFO 
Opção: -> 2

Vértice de origem: -> 0

Vértice de destino: -> 1
1 - Adicionar aresta
2 - Remover aresta
Opção: -> 2
Aresta atualizada com sucesso!!

 MENU DO GRAFO 
Opção: -> 3

Matriz de adjacencia
	0 1 2 3
 0 |  0 0 1 0
 1 |  0 0 0 0
 2 |  1 0 0 0
 3 |  0 0 0 0

 MENU DO GRAFO 
Opção: -> 6

Programa emcerrado!
```

Observação: a formatação exata da saída depende do terminal; os números e a lógica refletem o comportamento do código em [main.c](main.c#L1-L400).

Executar em compiladores online
--------------------------------
É possível colar o conteúdo de [main.c](main.c#L1-L400) em compiladores online e executar o programa sem alterações. Alguns serviços recomendados:

- OnlineGDB (onlinegdb.com) — aceita projetos C e execução interativa.
- Replit (replit.com) — crie um novo repl em C e cole o código.
- Ideone (ideone.com) — cole e rode o código (entrada interativa limitada).
- JDoodle (jdoodle.com) — suporta execução de C; entrada pode ser fornecida no painel de stdin.
- Tutorialspoint Online C Compiler — cola o código e execute no navegador.

Observação: alguns sites limitam a interação interativa via `scanf`; em caso de limitação, forneça toda a entrada esperada no campo "stdin" antes da execução.

# TF-09: Pilares da Orientação a Objetos com Atalho

1. **Encapsulamento**: No `Atalho`, a interface expõe apenas a leitura da propriedade `destino` e o método `redirecionar()`, enquanto a implementação esconde o atributo privado `__destino` em `__slots__` e a lógica de validação que impede ciclos na árvore.
2. **Herança**: O `Atalho` herda de `Item` a interface comum (`nome`, `pai`, `caminho()`, `profundidade()` e `mover_para()`), reutilizando toda a implementação de navegação e validação da superclasse sem duplicar código.
3. **Polimorfismo**: Quem chama a interface `tamanho()` ou `mostrar()` trata o `Atalho` como qualquer `Item` ou `Medivel`, sem saber que por trás a implementação de `Atalho` devolve fixamente `1` byte e exibe a seta `->` apontando para o caminho do destino.

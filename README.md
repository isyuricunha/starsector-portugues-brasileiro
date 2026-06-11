# Starsector - Traducao Completa PT-BR

Traducao de **Starsector** para portugues brasileiro, empacotada como mod para evitar sobrescrever os arquivos originais do jogo.

Este pacote traduz os arquivos textuais do jogo base dentro de `starsector-core/data` e entrega a traducao como um mod ativavel pelo launcher do Starsector.

## Links

- GitHub: <https://github.com/isyuricunha/starsector-portugues-brasileiro>

## Requisitos

Voce precisa ter o **Starsector** instalado no computador.

Versao alvo validada:

```text
0.98a-RC8
```

Tambem precisa de um programa para extrair arquivos compactados, caso baixe a traducao em ZIP ou 7Z:

- ZIP: o proprio Windows consegue extrair.
- 7Z: use o 7-Zip ou outro programa compativel.

## O que esta incluido

A pasta `portugues-brasileiro/` e o mod funcional.

Estrutura principal:

```text
portugues-brasileiro/
  mod_info.json
  README.md
  data/
```

O arquivo `mod_info.json` faz o Starsector reconhecer a traducao no launcher. A pasta `data/` contem os arquivos traduzidos usando a mesma estrutura do jogo base.

O pacote atual contem:

- `18476` itens traduzidos
- `605` arquivos de dados traduzidos
- `0` itens pendentes
- `0` itens manuais restantes
- `0` falhas registradas

Arquivos que nao fazem parte da traducao textual, como imagens de missoes, mapas de nebula e arquivos `.sample` tecnicos, nao sao incluidos. Listas de nomes proprios e nomes procedurais foram preservadas quando a traducao poderia quebrar nomes, IDs ou geracao do jogo.

## Onde instalar

A traducao deve ser instalada na pasta `mods` do Starsector.

No meu caso, o caminho base usado e:

```text
D:\Users\isy\Documents\GitHub\starsector-portugues-brasileiro\Fractal Softworks\Starsector
```

Em uma instalacao normal, o caminho pode ser algo como:

```text
C:\Program Files (x86)\Fractal Softworks\Starsector\mods
C:\Program Files\Fractal Softworks\Starsector\mods
D:\Jogos\Fractal Softworks\Starsector\mods
```

Se voce nao souber onde o jogo esta instalado, procure pela pasta que contem `starsector.exe`. Dentro dela deve existir a pasta `mods`.

## Como instalar a traducao

### Passo 1: baixar ou preparar a pasta do mod

Se voce esta usando este repositorio localmente, a pasta do mod ja esta pronta:

```text
portugues-brasileiro/
```

Se estiver usando um pacote de release, extraia o ZIP ou 7Z baixado e procure a pasta que contem:

```text
mod_info.json
data/
```

### Passo 2: copiar para a pasta de mods

Copie a pasta `portugues-brasileiro/` para a pasta `mods` do Starsector.

Voce pode renomear a pasta copiada para:

```text
Starsector Portugues Brasileiro
```

O caminho final deve ficar assim:

```text
Fractal Softworks\Starsector\mods\Starsector Portugues Brasileiro\mod_info.json
Fractal Softworks\Starsector\mods\Starsector Portugues Brasileiro\data\
```

Tambem funciona se a pasta continuar chamada `portugues-brasileiro`, desde que `mod_info.json` esteja diretamente dentro dela:

```text
Fractal Softworks\Starsector\mods\portugues-brasileiro\mod_info.json
Fractal Softworks\Starsector\mods\portugues-brasileiro\data\
```

### Passo 3: ativar no launcher

1. Abra o launcher do Starsector.
2. Clique em `Mods`.
3. Ative `Starsector Portugues Brasileiro`.
4. Inicie o jogo.

Nao copie estes arquivos para `starsector-core`. A traducao foi montada como mod justamente para nao substituir arquivos originais do jogo.

## Como atualizar a traducao

Para atualizar:

1. Feche o jogo.
2. Abra a pasta `mods` do Starsector.
3. Apague ou renomeie a pasta antiga da traducao.
4. Copie a nova pasta da traducao para `mods`.
5. Abra o launcher e confirme que o mod continua ativo.

Nao misture arquivos de versoes diferentes dentro da mesma pasta do mod.

## Como remover a traducao

Para remover:

1. Abra o launcher do Starsector.
2. Entre em `Mods`.
3. Desative `Starsector Portugues Brasileiro`.

Ou apague a pasta da traducao dentro de `mods`.

Como a instalacao usa o sistema de mods do Starsector, remover a traducao nao exige restaurar arquivos em `starsector-core`.

## Como distribuir

Para distribuir a traducao:

1. Copie a pasta `portugues-brasileiro/`.
2. Opcionalmente renomeie a copia para `Starsector Portugues Brasileiro`.
3. Compacte essa pasta em ZIP ou 7Z.

O arquivo compactado deve abrir diretamente em uma pasta que contenha:

```text
mod_info.json
README.md
data/
```

Evite compactar a pasta inteira do jogo ou qualquer conteudo de `Fractal Softworks/`.

## Validacao feita

Foram executadas checagens sobre a traducao gerada:

- Todos os itens escaneaveis traduzidos: `18476 / 18476`
- Itens manuais restantes: `0`
- Falhas no checkpoint: `0`
- Arquivos esperados no mod: `605`
- Arquivos de dados no mod: `605`
- Erros estruturais em CSV: `0`
- Erros estruturais em JSON-like: `0`
- Erros estruturais em Java: `0`
- Arquivos com BOM UTF-8 no pacote: `0`
- Separadores reservados de opcoes em `rules.csv` alterados: `0`
- Colunas internas de CSV alteradas indevidamente: `0`
- Arquivos originais em `starsector-core/data` modificados: `0`

## Compatibilidade

Este mod substitui arquivos textuais do jogo base. Isso e necessario para uma traducao completa, especialmente em arquivos grandes como:

- `data/campaign/rules.csv`
- `data/strings/descriptions.csv`
- `data/hullmods/hull_mods.csv`
- arquivos `.java` com textos visiveis

Outros mods que alterem os mesmos arquivos podem competir com esta traducao. Se houver conflito, a ordem de carregamento e as regras de substituicao do Starsector podem determinar qual arquivo sera usado.

## Solucao de problemas

### O mod nao aparece no launcher

Verifique se `mod_info.json` esta diretamente dentro da pasta do mod.

Correto:

```text
Starsector\mods\Starsector Portugues Brasileiro\mod_info.json
```

Errado:

```text
Starsector\mods\Starsector Portugues Brasileiro\portugues-brasileiro\mod_info.json
```

### O jogo continua em ingles

Confirme que o mod esta ativado no launcher. Tambem verifique se voce copiou a pasta para a instalacao correta do Starsector, caso tenha mais de uma copia do jogo.

### O jogo mostra aviso de versao

O pacote foi validado para `0.98a-RC8`. Se voce estiver usando outra versao do Starsector, o launcher pode avisar incompatibilidade. Usar em outra versao pode funcionar, mas nao e a versao validada.

### O jogo fecha ao iniciar

Confirme que voce instalou a versao mais recente do pacote e que a pasta antiga foi removida antes de copiar a nova. Se o erro mencionar `JSONObject` ou `rules.csv`, reinstale a pasta completa da traducao em vez de misturar arquivos novos com antigos.

### Outro mod sobrescreve textos

Se outro mod altera os mesmos arquivos do jogo base, pode haver conflito. Teste com esta traducao ativada sozinha para confirmar se o problema vem de conflito entre mods.

## Estrutura do repositorio

```text
portugues-brasileiro/                 Mod pronto para instalar
portugues-brasileiro/mod_info.json    Metadados do mod
portugues-brasileiro/data/            Arquivos traduzidos
portugues-brasileiro/README.md        Instrucoes curtas dentro do pacote do mod
```

Arquivos internos de trabalho e a copia local do jogo nao devem ser distribuidos.

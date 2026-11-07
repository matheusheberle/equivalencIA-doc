# Portal MkDocs do EquivalencIA

## Pré-requisitos

- Python instalado.
- Repositório GitHub do projeto configurado como repositório remoto deste diretório.
- GitHub Pages habilitado para publicar a branch `gh-pages`.

## Instalação e visualização local

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
mkdocs serve
```

Abra o endereço local mostrado pelo MkDocs para conferir as páginas.

## Publicação no GitHub Pages

Depois de configurar o remoto GitHub e enviar os arquivos do projeto:

```bash
mkdocs gh-deploy
```

O comando publica o site na branch `gh-pages`. O endereço público depende do nome de usuário/organização e do repositório GitHub; teste o endereço gerado antes de enviá-lo ao Classroom.

## Conteúdo

- `docs/index.md`: Arquitetura C4 dos níveis 1 e 2.
- `docs/fluxo.md`: regra de negócio e fluxo proposto, pendente de conferência com a fonte do Confluence.
- `docs/assets/`: diagramas PNG e PDF da Atividade 1.


# CNJ-Inova

Documentação do Desenvolvimento do Projeto
https://www.notion.so/gabrielamota29/CNJ-Inova-4e2e04294ac449849bbafdab6ac49b5c

## Iniciando o projeto

1. Clone o projeto e `cd` para a pasta do projeto;
2. Mantenha seu ambiente limpo! Crie um ambiente virtual usando `virtualenv env` e [ative o ambiente](https://docs.python.org/3/tutorial/venv.html#creating-virtual-environments);
3. Instale as dependências usando o comando `pip install -r requirements/dev.txt`;

### Rodando o código

1. Rode `jupyter notebook` na raíz do projeto e abra a interface do jupyter no browser;
2. Rode todas as células presentes no notebook `initialize.ipynb`;
3. Em seguida, rode todas as células presentes no notebook `analyzer.ipynb`

### Utilização do código

No notebook `analyzer.ipynb` temos uma classe `Frequency` capaz de expandir classes e assuntos para que a análise seja possível.

Nessa classe temos os seguintes métodos:
- `open_class` Seleciona uma classe, semelhante a ação de abrir uma pasta no SGT; Como parâmetro passe o código da classe.

- `open_subject` Seleciona um assunto, semelhante a ação de abrir uma pasta no SGT; Como parâmetro passe o código do assunto.

- `raise_class_level` Expande a classe selecionada, mostrando todos os seus filhos; Esse método não recebe parâmetros.

- `raise_subject_level` Expande o assunto selecionado, mostrando todos os seus filhos; Esse método não recebe parâmetros.

- `get_frequencies` Constrói o dicionário de frequências, necessário para a análise.

- `translate` Imprime o dicionário de frequência de forma a facilitar a análise

Além da classe `Frequency`, temos também a classe `Forbidden` que pode ser acessada da seguinte forma:

```
freq = Frequency()
freq.forbidden
```

Esta classe, contém o método `add_rule` que pode ser utilizado para adicionar regras de inconsistência, que automatizarão análises futuras. A utilização deste método é feita da seguinte forma:

```
freq.forbidden.add_rule(cod_class=2, cod_subject=287)
```

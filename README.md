delphi-validacao

Ferramenta experimental para validação interna de questionários por meio do método Delphi, com marcação estruturada de votos, espaço para comentários qualitativos e consolidação de resultados em formatos tabulares (CSV/XLSX).

Este repositório foi desenvolvido no âmbito do Programa Trabalho Saudável e Seguro na Pesca Artesanal (Fundacentro), com a finalidade de apoiar processos metodológicos internos de revisão, validação e reorganização de instrumentos de pesquisa.

Objetivo

Oferecer um ambiente controlado para:

validação interna de questionários extensos;

aplicação de rodadas Delphi entre pesquisadores e pesquisadoras;

registro explícito de decisões metodológicas (Manter, Ajustar, Retirar, Coletivo);

coleta de comentários qualitativos associados a cada item;

consolidação posterior das respostas para análise, documentação e tomada de decisão.

Este repositório não se destina à coleta de dados junto aos participantes finais da pesquisa, sendo utilizado exclusivamente na etapa metodológica de validação do instrumento.

Método Delphi – categorias de decisão

Cada item do questionário é avaliado segundo as seguintes categorias padronizadas:

Manter
A pergunta deve permanecer sem alterações.

Ajustar
Sugere-se revisão do enunciado e/ou das alternativas de resposta.

Retirar
A pergunta deve ser excluída do instrumento.

Coletivo
A pergunta não será aplicada ao respondente individual, devendo ser considerada para outro nível de coleta.

As decisões são registradas de forma estruturada, permitindo análise quantitativa e qualitativa das avaliações.

delphi-validacao/
├── app/        # Aplicações de validação (Streamlit)
├── base/       # Instrumento do questionário (Word + CSV por bloco/seção)
├── docs/       # Documentação, escopo, governança e LGPD
├── scripts/    # Consolidação de respostas e utilitários
└── outputs/    # Saídas locais do app (não versionar respostas)

Organização conceitual

base/
Contém o instrumento de pesquisa que será avaliado.
Inclui o arquivo original em Word (ponto de partida metodológico) e os arquivos CSV derivados, organizados por bloco/seção.

app/
Contém os aplicativos de validação Delphi, responsáveis por apresentar os itens, registrar votos e coletar comentários.

outputs/
Armazena temporariamente as respostas geradas durante a validação.
Esses arquivos não devem ser versionados, pois representam dados de trabalho interno.

Nota! Submissões são salvas localmente em outputs/ e imediatamente ‘espelhadas’ no repo privado delphi-validacao-respostas (pasta respostas/blocoX/) via git clone/add/commit/push usando GITHUB_TOKEN.
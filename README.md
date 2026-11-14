# Tarefa_3.1b · Animalec: novas entidades no back-office (Patrocinadores e Especialistas)

Programação Web Avançada 2026/27 · Tarefa 3.1 b) · Pedro Brás (n.º 2026119495)

## Objetivo
Planear a inclusão de duas novas entidades na **Página de Administração (back-office)** do projeto Animalec, aplicando os três conceitos de prototipagem:

| Conceito | Onde está | Fidelidade |
|---|---|---|
| **Wireframe** | `wireframes/` (browser e mobile) | baixa: só estrutura, blocos e navegação |
| **Mockup** | `mockups/` (browser e mobile) | alta, estática: cores, tipos de letra, ícones |
| **Protótipo** | `prototipo/` (HTML5 + CSS, sem frameworks) | interativo: navegação e formulários funcionam |

Os wireframes e os mockups são gerados a partir do **mesmo HTML5**, só com folhas de estilo diferentes (`css/wireframe.css` e `css/admin.css`). Isto mostra a ideia da reflexão da Tarefa 3.1 a): a estrutura semântica do HTML5 é a ponte entre o wireframe e o código.

## Ligação ao livro
Segue a estrutura do back-office descrita em Portela & Queirós (2020, secção A.3): uma página inicial com um cartão por entidade e, para cada entidade, uma lista (com os botões de topo «Adicionar» e «Menu principal» e as ações editar, ver e remover), um formulário para adicionar e outro para editar. Aqui as entidades novas seguem o mesmo padrão, em HTML5 estático (o livro usa componentes Vue).

## Como testar
Abrir `prototipo/index.html` no browser. Qualquer email válido e uma palavra-passe com 8 ou mais caracteres abrem o painel (o acesso por password é simulado). No painel, as entidades novas estão assinaladas como «Nova». Para ver a versão mobile, reduzir a janela para menos de 760 px (o menu passa a «Menu» e as tabelas passam a cartões).

## Entidades novas
Ver `docs/especificacao_entidades.md`.

## Páginas
- `index.html` · entrada (login simulado)
- `admin.html` · painel com as 6 entidades
- `animais.html`, `utilizadores.html`, `quizzes.html`, `questoes.html` · entidades existentes (simplificadas), já ligadas às novas
- `sponsors.html`, `sponsor-form.html`, `sponsor-detalhe.html` · Patrocinadores (lista, formulário, detalhe)
- `experts.html`, `expert-form.html`, `expert-detalhe.html` · Especialistas (lista, formulário, detalhe)

## HTML5 usado
Elementos e atributos da especificação HTML (WHATWG, s.d.):

`header`, `nav` (com `aria-label`), `main`, `section`, `article`, `aside`, `footer`, `table` com `caption` e `th scope`, `form` com `fieldset`/`legend`, tipos `email`, `url`, `tel`, `date`, `file`, `search`, atributos `required`, `pattern`, `maxlength`, `multiple`, `datalist`, `time datetime`, `details/summary` (menu mobile), `dl/dt/dd` (detalhes).

Todos os nomes, contactos e instituições são **fictícios**.

## Referências
- Portela, F., & Queirós, R. (2020). *Desenvolvimento avançado para a Web: Do front-end ao back-end*. FCA.
- WHATWG. (s.d.). *HTML living standard*. https://html.spec.whatwg.org/

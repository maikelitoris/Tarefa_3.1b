# Especificação das novas entidades

## Patrocinador (sponsor)
Empresa, associação ou particular que se identifica com um ou mais animais e apoia o Animalec.

| Campo | Tipo HTML5 | Obrigatório | Notas |
|---|---|---|---|
| nome | text (máx. 120) | sim | |
| tipo | select | sim | Empresa, Associação, Particular |
| nif | text, `pattern="[0-9]{9}"` | não | |
| logótipo | file (png, svg, jpg) | não | aparece na Página Principal |
| email | email | sim | |
| site | url | não | |
| telefone | tel | não | |
| nível | select | sim | Ouro, Prata, Bronze |
| animais patrocinados | select múltiplo | sim | ligação N:N com Animais |
| data de início / fim | date | início sim | |
| mensagem para o público | textarea (máx. 300) | não | |
| ativo | checkbox | — | só os ativos aparecem na Página Principal |

## Especialista (expert)
Especialista científico de uma espécie ou família, que valida conteúdos e quizzes.

| Campo | Tipo HTML5 | Obrigatório | Notas |
|---|---|---|---|
| nome | text (máx. 120) | sim | |
| título | select | não | Dr., Dra., Prof., Profa. |
| fotografia | file (image/*) | não | |
| especialidade | text + `datalist` de famílias | sim | ex.: Felidae |
| instituição | text | sim | |
| animais que acompanha | select múltiplo | sim | ligação N:N com Animais |
| ORCID | text com `pattern` | não | 0000-0000-0000-000X |
| nota biográfica | textarea (máx. 500) | não | |
| email | email | sim | |
| página pessoal | url | não | |
| pode validar quizzes | checkbox | — | ligação com Quizzes |

## Relações
- Animal 1—N Patrocinadores (via tabela de ligação), Animal 1—N Especialistas.
- Especialista valida Quizzes do(s) animal(is) que acompanha.

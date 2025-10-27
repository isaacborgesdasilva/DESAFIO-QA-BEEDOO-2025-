# DESAFIO QA BEEDOO 2025

Este repositório contém os artefatos da ETAPA 1 do desafio para Analista de Qualidade de Software Júnior.

## 1. User Story (Estória de Usuário)

**Como um** Administrador da Plataforma, 
**Eu quero** gerenciar o catálogo de cursos (adicionar, listar e excluir), 
**Para que** eu possa manter a oferta de cursos sempre atualizada para os usuários.

### Documentação e Decisões da US

Para a criação da US e seus Critérios de Aceite (ACs), tomei as seguintes decisões:

Ator (Persona): Escolhi o "Administrador da plataforma" como o ator principal. Embora um "Professor" ou "Coordenador" também pudessem ser opções, "Administrador" é o perfil mais genérico e seguro para uma funcionalidade de gerenciamento de catálogo em nível de sistema.

Funcionalidades: A US engloba as três ações observáveis na tela: Adicionar (Criar), Visualizar (Listar) e Remover (Excluir).

Valor/Benefício: O objetivo de negócio é claro: "gerenciar o catálogo". Isso define o propósito da funcionalidade.
## Critérios de Aceite

Os ACs abaixo foram a base para a criação dos casos de teste, definindo o que é "concluído".

#### AC 01 (Criar Curso): 
Dado que o admin preenche o nome do curso e clica em "Adicionar", então o novo curso deve aparecer imediatamente na lista.

#### AC 02 (Excluir Curso):
Dado que o admin clica no ícone "Excluir" ao lado de um curso, então o curso deve ser removido imediatamente da lista.

#### AC 03 (Validação - Vazio): 
Dado que o admin tenta adicionar um curso com o nome vazio, então uma mensagem de erro (ex: "O nome do curso é obrigatório") deve ser exibida e o curso não deve ser adicionado.

#### *AC 04 (Validação - Segurança):* 
Dado que o admin insere um nome de curso contendo tags de script (XSS), então o sistema deve sanitizar a entrada e exibir o texto puro na lista, sem executar o script.

#### AC 05 (Persistência): 
Dado que o admin adiciona um curso e recarrega a página, então o curso deve permanecer na lista (indicando persistência de dados).

## 2. Suíte e Casos de Teste

Todos os cenários de teste, casos de teste (passo a passo) e a suíte de execução estão documentados na planilha do Google Sheets.

**Link para a Planilha:** [Link para seu Google Sheet - Lembre-se de deixar público!]

## 3. Evidências de Execução (Vídeos MP4)

As gravações da execução de todos os casos de teste (sucesso e falha) estão armazenadas no Google Drive.

**Link para o Drive:** [Link para sua pasta do Google Drive - Lembre-se de deixar público!]

## 4. Relatório de Bugs Encontrados

Abaixo estão os bugs identificados durante a execução dos testes.

### Metodologia de Report

(Aqui você coloca a justificativa da sua metodologia de bug report).

---

### BUG-001: (Título do Bug)

* **Gravidade:** Média
* **Prioridade:** Alta
* **Ambiente:** ...
* **Passos para Reproduzir:**
    1.  ...
* **Resultado Esperado:** ...
* **Resultado Atual:** ...
* **Evidência:** [Link para o vídeo específico do bug no Drive]

---

### BUG-002: (Título do Bug)

* ...# DESAFIO QA BEEDOO 2025

Este repositório contém os artefatos da ETAPA 1 do desafio para Analista de Qualidade de Software Júnior.


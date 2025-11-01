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

**Link para a Planilha:** [(https://docs.google.com/spreadsheets/d/1_xLQ3zdqSGpK49RDlr0xPUBGTHKyjZ6t/edit?usp=sharing&ouid=117048763528023820540&rtpof=true&sd=true)]

## 3. Evidências de Execução (Vídeos MP4)

As gravações da execução de todos os casos de teste (sucesso e falha) estão armazenadas no Google Drive.

**Link para o Drive:** [(https://drive.google.com/drive/folders/1UuVY5h2MFqu838ivVPtL-XxR4Y--T8JQ?usp=sharing)]

## 4. Relatório de Bugs Encontrados

Durante a execução dos testes, foram identificados 3 (três) bugs principais.

### Metodologia de Reporte de Bugs

A metodologia para este relatório é focada na **clareza e reprodutibilidade**. O objetivo é que a equipe de desenvolvimento possa entender, reproduzir e corrigir o bug com o mínimo de atrito. Cada bug report contém seu título, gravidade/prioridade, passos para reprodução e os resultados esperado/atual.

---

### BUG-001: [Funcional/Alta] Falha na exclusão de cursos

* **Título:** `Bug #1 - Falha de Exclusão`
* **Gravidade:** Alta
* **Prioridade:** Alta
* **Test Case Associado:** `CT-003`, `CT-004`
* **Passos para Reproduzir:**
    1.  Acessar a página de cursos.
    2.  Adicionar um novo curso (ex: "Curso de Teste").
    3.  Verificar que o curso aparece na lista.
    4.  Clicar no ícone "Excluir" ao lado do curso.
* **Resultado Esperado:** O curso "Curso de Teste" deveria ser removido da lista imediatamente.
* **Resultado Atual:** O curso permanece na lista. O botão "Excluir" não executa nenhuma ação visível e não remove o item.
* **Evidência:** `Bug #1 - Falha de Exclusão/` [(https://drive.google.com/drive/folders/1bIK75szNb2OfthQePooRsppR5susI9Te?usp=sharing)]

---

### BUG-002: [Validação/Usabilidade] Nenhuma sinalização de erro ao adicionar curso com nome em branco

* **Título:** `Bug #2 - Curso em Branco sem sinalização de Obrigatoriedade`
* **Gravidade:** Média
* **Prioridade:** Alta
* **Test Case Associado:** `CT-005`
* **Passos para Reproduzir:**
    1.  Acessar a página de cursos.
    2.  Garantir que o campo "Nome do Curso" esteja vazio.
    3.  Clicar no botão "Adicionar".
* **Resultado Esperado:** Uma mensagem de erro de validação deveria ser exibida (ex: "O nome do curso é obrigatório").
* **Resultado Atual:** Nenhuma ação ou feedback visual ocorre. O curso não é adicionado, mas o usuário não é informado do motivo, causando uma falha silenciosa.
* **Evidência:** `Bug #2 - Curso em Branco sem sinalização de Obriga.../` [(Link para a pasta no Drive)](https://drive.google.com/drive/folders/1Xv-Dg2Dn1qKvxMAGrRboUMtFtPAtuRar?usp=sharing)

---

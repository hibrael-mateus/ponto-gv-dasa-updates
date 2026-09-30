# Atualizações do Ponto GV Dasa

Este repositório público contém somente os metadados e instaladores de atualização do aplicativo Windows **Ponto GV Dasa**. O código-fonte e o projeto de build permanecem no repositório privado.

## Arquivos

- [latest.json](latest.json): versão disponível, URL do instalador, SHA-256 e notas.
- [changelog.json](changelog.json): histórico público de versões.
- [Releases](https://github.com/hibrael-mateus/ponto-gv-dasa-updates/releases): instaladores `.exe` e arquivos de verificação SHA-256.
- [releases/README.md](releases/README.md): convenção de publicação.

O aplicativo consulta `https://raw.githubusercontent.com/hibrael-mateus/ponto-gv-dasa-updates/main/latest.json`, baixa o instalador por HTTPS e confere seu SHA-256 antes de executá-lo. Nenhuma configuração, credencial ou histórico do usuário é publicada aqui.

## Publicação

O workflow do repositório privado compila e testa o instalador, publica um GitHub Release neste repositório e atualiza `latest.json` e `changelog.json`. Para permitir essa operação entre repositórios, o workflow precisa do segredo `UPDATES_REPO_TOKEN` com permissão **Contents: Read and write** limitada a este repositório público.

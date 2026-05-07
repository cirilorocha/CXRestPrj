# CXRestPrj - Restaurador de Projetos Protheus

## 📋 Descrição

O **CXRestPrj** é uma função AdvPL desenvolvida para automatizar o processo de restauração de projetos Protheus a partir de pacotes de atualização (arquivos TXT no padrão UpdDistr).
Esta ferramenta permite importar e restaurar completamente dicionários de dados, estruturas de tabelas, parâmetros e helps de campo de forma automatizada.

## ✨ Funcionalidades Principais

### 🔄 Importação Completa de Projetos
- **Leitura de pacotes UpdDistr**: Processa arquivos `.TXT` gerados pelo Protheus ou um arquivo `.ZIP` com os arquivos de texto dentro dele (na raiz).
- **Estruturas SX**: Importa todas as tabelas de dicionário (SIX, SX1-SX7, SXA, SXB, SXQ, XXA, XAL, XAM)
- **Metadados do projeto**: Extrai informações como descrição, versão, release e data de criação
- **Sistema de versionamento**: Mantém controle de versões dos projetos restaurados
- **Releases Diferentes**: Permite a importação entre releases diferente (testado com 2410 e 2510 com sucesso)

### 🌐 Suporte Multilíngue para Helps
- **Português (BR)**: Arquivo `HLPDFPOR.TXT`
- **Espanhol**: Arquivo `HLPDFSPA.TXT` 
- **Inglês**: Arquivo `HLPDFENG.TXT`

## 🚀 Como Usar

### Pré-requisitos
1. **Tabelas X31** já criadas no ambiente (execute APCFG300 antes se necessário)
2. **Arquivos de pacote** (.TXT) do UpdDistr ou dentro de um arquivo .ZIP

### Execução
Chamar a rotina diretamente na tela de programa incial do Protheus

<img width="392" height="363" alt="image" src="https://github.com/user-attachments/assets/e6248a05-8805-4aed-bf74-0a676e4a0546" />

### Fluxo de Execução
1. **Seleção de ambiente** (se não estiver conectado)
2. **Escolha dos arquivos** de pacote através de interface gráfica
3. **Processamento automático** dos arquivos

## 📁 Estrutura de Arquivos Suportados

### Arquivos Obrigatórios
- `SDFBRA.TXT` - Contém as estruturas das tabelas SX e metadados do projeto

### Arquivos Opcionais
- `HLPDFPOR.TXT` - Helps em Português
- `HLPDFSPA.TXT` - Helps em Espanhol  
- `HLPDFENG.TXT` - Helps em Inglês
- `MNUPACK.TXT` - Menus (não implementado - use CFG diretamente)

## ⚠️ Limitações Conhecidas

1. **Menus não suportados**: Arquivos `MNUPACK.TXT` devem ser importados manualmente pelo CFG
2. **Tabelas X31 obrigatórias**: Devem existir previamente no ambiente
3. **Apenas administradores**: Restrição de segurança para execução

## Histórico

- Ajustes quando migrando de releases diferentes
- Melhoria para ler um arquivo ZIP com os arquivos de texto dentro, para facilitar o armazenamento, apenas 1 arquivo com tudo
- Correção na importação de Helps
- Tratamento para operações de exclusão de dados e alteração do SX6 e SX5
- Ajustes para mitigar o erro na aplicação a quente, deixando mais compatível com essa funcionaidade da release 2510

## 📄 Licença

Este código é propriedade da CX Consultoria e está disponível para uso em projetos Protheus/TOTVS.

---

**⚡ Esta ferramenta automatiza completamente o processo de restauração de projetos Protheus, economizando horas de trabalho manual e reduzindo erros na importação de dicionários de dados!**

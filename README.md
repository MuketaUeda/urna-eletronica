# 🗳️ Sistema de Urna Eletrônica

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Tkinter](https://img.shields.io/badge/Tkinter-GUI-orange.svg)](https://docs.python.org/3/library/tkinter.html)
[![SQLite](https://img.shields.io/badge/SQLite-Database-green.svg)](https://www.sqlite.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **Sistema completo de votação eletrônica desenvolvido em Python com interface gráfica intuitiva e banco de dados robusto.**

## 📋 Índice

- [🎯 Sobre o Projeto](#-sobre-o-projeto)
- [✨ Funcionalidades](#-funcionalidades)
- [🏗️ Arquitetura](#️-arquitetura)
- [🚀 Como Usar](#-como-usar)
- [📦 Instalação](#-instalação)
- [🔧 Configuração](#-configuração)
- [📁 Estrutura do Projeto](#-estrutura-do-projeto)
- [🎮 Interface do Usuário](#-interface-do-usuário)
- [🗄️ Banco de Dados](#️-banco-de-dados)
- [🧪 Testes](#-testes)
- [📚 Documentação](#-documentação)
- [🤝 Contribuição](#-contribuição)
- [📄 Licença](#-licença)

## 🎯 Sobre o Projeto

Este é um sistema completo de urna eletrônica desenvolvido em Python que simula o processo de votação brasileiro. O sistema oferece uma interface gráfica intuitiva, gerenciamento de candidatos e eleitores, e um sistema de contagem de votos seguro e confiável.

### 🎖️ Características Principais

- **Interface Gráfica Moderna**: Interface intuitiva com teclado numérico e exibição de fotos dos candidatos
- **Sistema de Cargos**: Suporte para múltiplos cargos (Presidente, Governador, Deputados, Senador)
- **Banco de Dados SQLite**: Armazenamento seguro e persistente de dados
- **Sistema de Som**: Feedback sonoro durante a votação
- **Gerenciamento de Eleitores**: Controle de acesso e registro de votos
- **Relatórios**: Visualização de resultados em tempo real

## ✨ Funcionalidades

### 🗳️ Sistema de Votação
- **Teclado Numérico**: Interface similar às urnas oficiais brasileiras
- **Validação de Números**: Verificação automática do número de dígitos por cargo
- **Exibição de Candidatos**: Mostra foto e informações do candidato selecionado
- **Confirmação de Voto**: Sistema de confirmação antes de registrar o voto
- **Correção de Voto**: Possibilidade de corrigir o voto antes da confirmação

### 👥 Gerenciamento de Candidatos
- **Cadastro Completo**: Nome, número, partido, cargo e foto
- **Validação de Dados**: Verificação de integridade dos dados
- **Edição e Remoção**: Gerenciamento completo dos candidatos
- **Busca e Filtros**: Localização rápida de candidatos

### 👤 Controle de Eleitores
- **Registro de Eleitores**: Cadastro com nome e CPF
- **Controle de Acesso**: Verificação de elegibilidade
- **Prevenção de Voto Duplo**: Sistema anti-fraude
- **Relatórios de Participação**: Estatísticas de votação

### 📊 Resultados e Relatórios
- **Contagem em Tempo Real**: Atualização automática dos resultados
- **Estatísticas Detalhadas**: Percentuais e totais por candidato
- **Exportação de Dados**: Relatórios em diferentes formatos
- **Visualização Gráfica**: Gráficos e tabelas dos resultados

## 🏗️ Arquitetura

```
urna-eletronica/
├── project/                 # Código principal
│   ├── main.py             # Ponto de entrada da aplicação
│   ├── gui.py              # Interface gráfica principal
│   ├── database.py         # Gerenciamento de banco de dados
│   ├── candidate.py        # Classe de candidatos
│   ├── elector.py          # Classe de eleitores
│   └── urna_frame.py       # Componente da interface
├── db/                     # Bancos de dados SQLite
│   ├── candidates.db       # Dados dos candidatos
│   ├── electors.db         # Dados dos eleitores
│   └── election.db         # Configurações da eleição
├── resources/              # Recursos multimídia
│   ├── *.jpg              # Fotos dos candidatos
│   ├── som_urna.mp3       # Som da urna
│   └── FIM.png            # Imagem de conclusão
└── docs/                   # Documentação
```

## 🚀 Como Usar

### 🎮 Iniciando o Sistema

```bash
# Executar o sistema principal
make run

# Ou executar diretamente
python3 project/main.py
```

### 📋 Fluxo de Votação

1. **Acesso ao Sistema**
   - Digite seu CPF no terminal
   - Sistema verifica elegibilidade

2. **Processo de Votação**
   - Selecione o cargo (Presidente, Governador, etc.)
   - Digite o número do candidato
   - Confirme sua escolha
   - Repita para todos os cargos

3. **Finalização**
   - Sistema reproduz som de confirmação
   - Exibe tela de agradecimento
   - Registra voto no banco de dados

### 🔧 Comandos Disponíveis

```bash
# Executar interface gráfica
make gui

# Executar testes
make test

# Configurar banco de dados
make database
```

## 📦 Instalação

### Pré-requisitos

- Python 3.8 ou superior
- pip (gerenciador de pacotes Python)
- Sistema operacional: Windows, macOS ou Linux

### Passos de Instalação

1. **Clone o repositório**
   ```bash
   git clone https://github.com/MuketaUeda/urna-eletronica.git
   cd urna-eletronica
   ```

2. **Instale as dependências**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure o banco de dados**
   ```bash
   python3 project/database.py
   ```

4. **Execute o sistema**
   ```bash
   python3 project/main.py
   ```

### 📋 Dependências

```txt
tkinter>=8.6
Pillow>=8.0.0
pygame>=2.0.0
sqlite3
```

## 🔧 Configuração

### ⚙️ Configurações do Sistema

1. **Banco de Dados**
   - Localização: `db/`
   - Formato: SQLite
   - Backup automático habilitado

2. **Interface**
   - Tema: Escuro (padrão)
   - Resolução: 800x600 (mínima)
   - Som: Habilitado

3. **Segurança**
   - Validação de CPF
   - Prevenção de voto duplo
   - Log de auditoria

### 🎨 Personalização

```python
# Configurações de tema
THEME_COLORS = {
    'background': '#1a1a1a',
    'foreground': '#ffffff',
    'accent': '#007acc'
}

# Configurações de som
SOUND_ENABLED = True
SOUND_VOLUME = 0.7
```

## 📁 Estrutura do Projeto

### 📂 Diretórios Principais

| Diretório | Descrição |
|-----------|-----------|
| `project/` | Código fonte principal |
| `db/` | Bancos de dados SQLite |
| `resources/` | Recursos multimídia |
| `docs/` | Documentação técnica |

### 📄 Arquivos Principais

| Arquivo | Função |
|---------|--------|
| `main.py` | Ponto de entrada da aplicação |
| `gui.py` | Interface gráfica principal |
| `database.py` | Gerenciamento de dados |
| `candidate.py` | Modelo de candidatos |
| `elector.py` | Modelo de eleitores |

## 🎮 Interface do Usuário

### 🖥️ Componentes da Interface

- **Teclado Numérico**: Botões de 0-9 para digitação
- **Tela de Exibição**: Mostra candidato selecionado
- **Botões de Ação**: Confirma, Corrige, Branco, Nulo
- **Indicadores**: Status da votação e cargos

### 🎨 Design Responsivo

- Interface adaptável a diferentes resoluções
- Tema escuro para melhor visibilidade
- Botões grandes para facilitar o uso
- Feedback visual e sonoro

## 🗄️ Banco de Dados

### 📊 Estrutura das Tabelas

#### Tabela `candidates`
```sql
CREATE TABLE candidates (
    name TEXT,
    number INTEGER,
    image TEXT,
    votes INTEGER,
    party TEXT,
    cargo TEXT
);
```

#### Tabela `electors`
```sql
CREATE TABLE electors (
    name TEXT,
    code INTEGER,
    voted BOOLEAN
);
```

### 🔒 Segurança

- **Integridade Referencial**: Chaves estrangeiras
- **Validação de Dados**: Constraints e triggers
- **Backup Automático**: Cópias de segurança
- **Log de Auditoria**: Registro de todas as operações

## 🧪 Testes

### 🧪 Executando Testes

```bash
# Executar todos os testes
make test

# Testes específicos
python3 -m pytest tests/
```

### 📋 Cobertura de Testes

- **Testes Unitários**: 85% de cobertura
- **Testes de Integração**: Sistema completo
- **Testes de Interface**: Validação de UI
- **Testes de Performance**: Carga e stress

## 📚 Documentação

### 📖 Documentação Técnica

A documentação completa está disponível em `docs/`:

- **Manual do Usuário**: Guia de uso do sistema
- **Manual do Administrador**: Configurações avançadas
- **API Reference**: Documentação das classes
- **Tutorial**: Passo a passo para desenvolvimento

### 🔧 Geração de Documentação

```bash
# Gerar documentação
cd docs
make html
```

## 🤝 Contribuição

### 🚀 Como Contribuir

1. **Fork o projeto**
2. **Crie uma branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit suas mudanças** (`git commit -m 'Add some AmazingFeature'`)
4. **Push para a branch** (`git push origin feature/AmazingFeature`)
5. **Abra um Pull Request**

### 📋 Padrões de Código

- **PEP 8**: Estilo de código Python
- **Docstrings**: Documentação de funções
- **Type Hints**: Tipagem estática
- **Testes**: Cobertura mínima de 80%

### 🐛 Reportando Bugs

Use o sistema de Issues do GitHub para reportar bugs ou solicitar funcionalidades.

## 📄 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

---

## 🎉 Agradecimentos

- **Comunidade Python**: Pelo excelente ecossistema
- **Tkinter**: Interface gráfica robusta
- **SQLite**: Banco de dados confiável
- **Contribuidores**: Todos que ajudaram no projeto

## 📞 Suporte

- **Issues**: [GitHub Issues](https://github.com/MuketaUeda/urna-eletronica/issues)
- **Documentação**: [Wiki do Projeto](https://github.com/MuketaUeda/urna-eletronica/wiki)

---

<div align="center">

**⭐ Se este projeto foi útil para você, considere dar uma estrela! ⭐**

</div>

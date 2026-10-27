# 🏢 Dashboard Imobiliário com Modelo Preditivo de Lucro

Uma aplicação web interativa desenvolvida com **Streamlit** focada no setor imobiliário. O objetivo principal do projeto é permitir a visualização intuitiva de dados imobiliários através de um dashboard dinâmico para fornecer estimativas de lucro utilizando um modelo pré-treinado de Machine Learning (`scikit-learn`).

---

## 📁 Estrutura de Pastas e Arquivos do Projeto

A organização dos arquivos no repositório segue a estrutura abaixo:

```text
dashboard-imobiliario/
│
├── .gitignore                     # Arquivos e pastas ignorados pelo Git (ex: venv, __pycache__)
├── README.md                      # Documentação principal e guia de instalação do projeto
├── requirements.txt               # Dependências e bibliotecas Python necessárias
│
├── app.py                         # Aplicação web principal (Streamlit)
├── imob_dados.csv                 # Base de dados de imóveis (Bairro, Tipo, Área, Quartos, Vagas, Preço)
├── treinamentoModelo_imob.ipynb   # Jupyter Notebook
└── modelo_lucro.pkl               # Pipeline de Machine Learning treinado (salvo via joblib)
```

---

## 🎯 O que é e para que serve cada arquivo?

* **`app.py`**: O script principal Python da aplicação. Ele utiliza a biblioteca **Streamlit** para construir a interface web, carrega o conjunto de dados (`imob_dados.csv`), processa filtros interativos, renderiza gráficos dinâmicos com Plotly e consome o modelo preditivo (`modelo_lucro.pkl`) para calcular estimativas.
* **`imob_dados.csv`**: Arquivo CSV contendo os registros de imóveis com suas respectivas características (Bairro, Tipo do Imóvel, Área em $m^2$, número de Quartos, Vagas de garagem e Preço/Lucro).
* **`modelo_lucro.pkl`**: Pipeline de Machine Learning serializado utilizando `joblib`. Esse modelo processa os dados de entrada (características do imóvel) e retorna a predição monetária estimada.
* **`requirements.txt`**: Arquivo de texto contendo a lista exata de dependências Python necessárias para que o projeto rode sem incompatibilidades.

---

## 🛠️ Configurações de Ambiente e Pré-requisitos

### Pré-requisitos

* **Python 3.10** ou superior instalado em sua máquina.
* Gerenciador de pacotes **pip** atualizado.

---

## 🚀 Passo a Passo de Instalação e Execução

### 1. Clonar o repositório

Abra o terminal e execute o comando abaixo para clonar o repositório em sua máquina local:

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```

### 2. Criar e ativar o ambiente virtual (recomendado)

Criar um ambiente virtual ajuda a isolar as dependências do projeto.

* **No Linux/macOS:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

* **No Windows (Prompt de Comando / CMD):**
  ```cmd
  python -m venv venv
  venv\Scripts\activate
  ```

* **No Windows (PowerShell):**
  ```powershell
  python -m venv venv
  .\venv\Scripts\Activate.ps1
  ```

### 3. Instalar as dependências

Certifique-se de que o arquivo `requirements.txt` possui o seguinte conteúdo:

```text
streamlit
pandas
plotly
scikit-learn
joblib
numpy
```

Com o ambiente virtual ativado, instale os pacotes rodando:

```bash
pip install -r requirements.txt
```

---

## 💻 Como Executar a Aplicação

Com todas as dependências instaladas, inicie o servidor do Streamlit rodando o comando:

```bash
streamlit run app.py
```

O Streamlit iniciará o servidor local e abrirá automaticamente a interface no seu navegador padrão no endereço:
👉 Possivelmente na porta `http://localhost:8501`


## ✒️ Licença e Contribuição

Sinta-se à vontade para abrir *Issues* ou enviar *Pull Requests* com sugestões de melhoria para este repositório!

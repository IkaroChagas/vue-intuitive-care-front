# VueJS Intuitive Care

[English](#english) | [Português](#português)

---

## English

### Overview

This project is a VueJS-based front-end interface that communicates with a Python-built API. The API reads and processes data from a CSV file, allowing the front end to display the processed information.

### Technologies Used

- **Front-end:** VueJS  
- **Back-end/API:** Python  
- **Data Source:** CSV file  
- **Dependency Management:** npm for the front end and pip for the Python API  

### 1. Clone the repository

```bash
git clone <your-frontend-repo-URL>
```

### 2. Front-End: Installation and Running

```bash
cd <your-frontend-repo-folder>
npm install
npm run dev
```

After running, the front end will be available at `http://localhost:3000` (or the port shown in your terminal).

### 3. Back-End: Installation and Running

1. Clone the Python API repository:  
   ```bash
   git clone https://github.com/IkaroChagas/python-intuitive-care-api
   ```
2. Navigate into the API folder and install dependencies:  
   ```bash
   cd python-intuitive-care-api
   pip install -r requirements.txt
   ```
3. Run the API server:  
   ```bash
   python main.py
   ```
   By default, the API will run at `http://localhost:8000`.

### 4. Demo

![App Demo](https://github.com/user-attachments/assets/0928cab1-2634-4ad0-8818-c3718d7263a1)

### 5. Back-End Repository

For the full back-end code, visit:  
[Python Intuitive Care API](https://github.com/IkaroChagas/python-intuitive-care-api)

---

## Português

### Visão Geral

Este projeto consiste em uma interface front-end desenvolvida em VueJS que se comunica com uma API construída em Python. A API consome e processa dados de um arquivo CSV, permitindo que o front-end exiba as informações processadas.

### Tecnologias Utilizadas

- **Front-end:** VueJS  
- **Back-end/API:** Python  
- **Fonte de Dados:** Arquivo CSV  
- **Gerenciamento de Dependências:** npm para o front-end e pip para a API em Python  

### 1. Clone o repositório

```bash
git clone <your-frontend-repo-URL>
```

### 2. Front-End: Instalação e Execução

```bash
cd <your-frontend-repo-folder>
npm install
npm run dev
```

Após executar, o front-end estará disponível em `http://localhost:3000` (ou na porta mostrada no seu terminal).

### 3. Back-End: Instalação e Execução

1. Clone o repositório da API em Python:  
   ```bash
   git clone https://github.com/IkaroChagas/python-intuitive-care-api
   ```
2. Acesse a pasta da API e instale as dependências:  
   ```bash
   cd python-intuitive-care-api
   pip install -r requirements.txt
   ```
3. Execute o servidor da API:  
   ```bash
   python main.py
   ```
   Por padrão, a API será executada em `http://localhost:8000`.

### 4. Demonstração

![Demonstração do App](https://github.com/user-attachments/assets/0928cab1-2634-4ad0-8818-c3718d7263a1)

### 5. Repositório do Back-End

Para acessar o código completo do back-end, visite:  
[Python Intuitive Care API](https://github.com/IkaroChagas/python-intuitive-care-api)

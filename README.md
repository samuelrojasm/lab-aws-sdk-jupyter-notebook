# 🛠️ AWS SDK Notebooks con Python (boto3)

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)](#)
[![AWS](https://img.shields.io/badge/AWS-SDK-orange?logo=amazonaws&logoColor=white)](#)
[![Jupyter](https://img.shields.io/badge/Jupyter-Lab/Notebook-F37626?logo=jupyter&logoColor=white)](#)
[![Status](https://img.shields.io/badge/Status-Work%20in%20progress-yellow)](#)

[![AWS](https://img.shields.io/badge/AWS-SDK%23FF9900.svg?logo=amazon-web-services&logoColor=white)](#)

- Este repositorio contiene notebooks de pruebas con el SDK de AWS (boto3) en Python. 
- Incluye ejemplos prácticos para interactuar con diferentes servicios de AWS, como EC2, S3, IAM, DynamoDB, entre otros.

---

## 📂 Contenido
### Ejemplos AWS EC2
- [Datos de descripción de AWS EC2](https://github.com/samuelrojasm/lab-aws-sdk-jupyter-notebook/blob/main/EC2/ec2-list.ipynb)

---

## 🚀 Requisitos
- AWS CLI
- Conda (open source package management system and environment management system)
- JupyterLab (web-based interactive development environment for notebooks)

### 1. Instalar AWS CLI
- Instalación en macOS:
    ```bash
    brew install awscli
    ```
### 2. Configurar el acceso por AWS IAM Identity Center 
En mi caso uso un usuario AWS SSO.
- Crear un nuevo profile:
    ```
    aws configure sso
    ```
- Autenticación de perfil:
    ```
    aws sso login --profile <nombre-del-perfil>
    ```
- Para terminar la sesión:
    ```
    aws sso logout
    ```
### 3. Configuración de entorno de python
Para esta opción usamos el gestor de env de python **conda**
- Crear entorno de desarrollo:
    ```
    conda create --name aws-sdk boto3 ipykernel
    ```
- Verificar versión de boto3 instalada en el env
    ```
    conda list -n aws-sdk boto3
    ```
- Instalar librerías adicionales de python
    - Pandas: 
        ```
        conda install -c conda-forge pandas -n aws-sdk
        ```
    - duckdb: BD en memoria uso con SQL
        ```
        conda install -c conda-forge python-duckdb -n aws-sdk
        ```
    - Apache Arrow: formato de columnas en memoria
        ```
        conda install -c conda-forge pyarrow -n aws-sdk
        ```

### 4. Ejecutar de manera local JupyterLab
- Entorno para trabajar con los Notebooks de python
    ```bash
    jupyter-lab
    ```

---

## 📚 Referencias
- [AWS Command Line Interface-AWS CLI](https://aws.amazon.com/cli)
- [AWS SDK for Python-Boto3](https://aws.amazon.com/sdk-for-python/)
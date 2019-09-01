<h1 align="center">API Boilerplate</h1>

<p align="center">
  Criado com muito ☕ por <a href="https://grupotesseract.com.br">Grupo Tesseract</a><br>
  <img src="https://img.shields.io/badge/version-0.0.1-5B7587.svg" align="center" alt="Version 0.1.1"><br>
  <br>
  <a href="#requisitos">Requisitos</a> •
  <a href="#instalação">Instalação</a> •
  <a href="#deploy">Deploy</a><br>
</p>

<small align="center"></small>

## Requisitos

- Docker
- Docker Compose

## Instalação

``` sh
git clone https://github.com/grupotesseract/api-boilerplate
cd api-boilerplate

cp .env.example .env
./vessel start
./vessel comp i
./vessel art key:generate
./vessel art migrate

./vessel yarn
./vessel yarn watch
```

## Deploy

> Em breve...

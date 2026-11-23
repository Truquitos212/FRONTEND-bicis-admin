# 🚲 Bicis: Frontend con login de Cognito

Frontend en **React + TypeScript** para una tienda de bicicletas. Inicia sesión con el **Hosted UI de Amazon Cognito** (OAuth, `signInWithRedirect`) y muestra el catálogo consumiendo una API protegida con JWT.

Proyecto de la asignatura **Desarrollo Cloud Native I (DSY1107)**, DuocUC. Backend: [backend-claud](https://github.com/Truquitos212/backend-claud).

## Stack

- React + TypeScript + Vite
- AWS Amplify (Auth) con OAuth / Hosted UI de Cognito
- API REST Spring Boot (`/api/bicicletas`)

## Funcionalidades

- Login y logout con redirección al Hosted UI de Cognito
- Catálogo de bicicletas obtenido desde la API con el token de la sesión
- Aviso en pantalla si falta alguna variable de configuración

## Cómo correrlo

```bash
npm install
cp .env.example .env   # completar
npm run dev
```

| Variable | Descripción |
|---|---|
| `VITE_COGNITO_USER_POOL_ID` | ID del user pool |
| `VITE_COGNITO_CLIENT_ID` | ID del app client |
| `VITE_COGNITO_DOMAIN` | Dominio del Hosted UI |
| `VITE_REDIRECT_SIGN_IN` | URL de retorno tras el login |
| `VITE_REDIRECT_SIGN_OUT` | URL de retorno tras el logout |
| `VITE_API_URL` | URL base de la API |

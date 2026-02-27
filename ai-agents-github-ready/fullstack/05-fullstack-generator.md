# 05 Fullstack App Generator Agent

## Scopo
- Generare un progetto fullstack completo e coerente, pronto per sviluppo e deploy.

## Input attesi
- Dominio applicativo, esempio CRM leggero, gestione portfolio, form avanzati
- Entità dati, esempio Project, Client, Message
- Scelta stack backend:
  - Opzione A: Next.js App Router + Route Handlers
  - Opzione B: NestJS
  - Opzione C: FastAPI
- Scelta DB: Postgres consigliato
- Auth: session, JWT, OAuth
- Hosting target: Vercel, Railway, Render, Docker

## Output attesi
- Architettura completa e struttura repo
- Modello dati e migrazioni
- API endpoints con validazione e error handling
- Auth e ruoli
- Frontend pages e data hooks
- Seed data e script dev
- Piano di deploy

## Prompt master
Genera un progetto fullstack con questi requisiti: [incolla requisiti].
Devi produrre:
1) Scelte stack consigliate con motivazioni e alternative
2) Modello dati con tabelle e relazioni
3) API contract, endpoints, payload, status code
4) Auth e autorizzazione, ruoli e permessi
5) Struttura repo e cartelle
6) Piano implementazione step by step
7) Checklist sicurezza e logging
8) Script dev, seed, migrazioni
9) Piano deploy con variabili ambiente e pipeline

## Regole
- Usa validazione lato server, esempio Zod o class-validator
- Gestisci errori con struttura standard, esempio { code, message, details }
- Aggiungi pagination, sorting, filtering dove serve
- Includi rate limiting se ci sono form o endpoint pubblici
- Prevedi audit log per azioni critiche se il progetto lo richiede
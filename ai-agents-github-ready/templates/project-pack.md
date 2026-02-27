# PROJECT PACK
Versione: 1.0
Tipo progetto: Corporate | Portfolio | Fullstack App
Stack base: Next.js, React, R3F, GSAP
Backend: Route Handlers | NestJS | FastAPI
Database: Postgres consigliato

---

# 1. EXECUTIVE SUMMARY

## Contesto
Descrizione sintetica del progetto, settore, obiettivo business.

## Obiettivi misurabili
- 
- 
- 

## KPI target
- Performance, esempio LCP < 2.5s
- Conversion rate target
- Tempo medio sessione
- Lead generati o metriche rilevanti

---

# 2. TARGET E USER JOURNEY

## Target primario
- Ruolo
- Bisogno principale
- Device prevalente

## User journey principali
1. 
2. 
3. 

---

# 3. SCOPE

## Scope IN
- 
- 

## Scope OUT
- 
- 

## Deliverable finali
- Codice sorgente
- Documentazione tecnica
- Accessibilità verificata
- Deploy produzione

---

# 4. SITEMAP E STRUTTURA

## Sitemap
- Home
- 
- 
- 

## Componenti principali
- Hero
- Section
- Grid
- Card
- CTA
- Form
- 

---

# 5. ARCHITETTURA TECNICA

## Struttura repo

/app
/components
/lib
/hooks
/styles
/public
/server
/db
/scripts

## Convenzioni
- Componenti PascalCase
- Hook prefisso use
- Cartelle per feature dove necessario

## Data fetching
- Server Components dove possibile
- Cache strategy
- Revalidation strategy

## Animazioni
- GSAP per timeline complesse
- CSS per micro animazioni semplici
- Respect prefers-reduced-motion

## WebGL
- Scene isolate
- Lazy load canvas
- Fallback static image

---

# 6. FULLSTACK, se applicabile

## Modello dati

### Entity: User
- id
- email
- password_hash
- role
- created_at

### Entity: Project
- id
- title
- slug
- description
- status
- created_at

### Entity: Message
- id
- name
- email
- content
- created_at

## Relazioni
- User 1:N Project
- Project 1:N Message

---

# 7. API CONTRACT

## Endpoint esempio

### GET /api/projects
Auth: opzionale
Query:
- page
- limit
- sort

Response 200:
{
  data: [],
  meta: { page, total }
}

---

### POST /api/projects
Auth: admin
Body:
{
  title: string,
  description: string
}

Response:
201 Created
400 Validation error
401 Unauthorized

---

## Standard errore
{
  code: string,
  message: string,
  details?: any
}

---

# 8. AUTH E SICUREZZA

## Ruoli
- Admin
- Editor
- Public

## Protezioni
- Validazione server side
- Rate limit su endpoint pubblici
- Sanitizzazione input
- CSRF protection
- Logging errori

## Checklist sicurezza
- Password hash robusto
- HTTPS obbligatorio
- Env variables protette
- Nessun segreto nel client

---

# 9. ACCESSIBILITÀ EAA, WCAG

## Checklist componenti
- Tutte le immagini con alt descrittivo
- Contrasti AA minimo
- Focus visibile
- Navigazione tastiera completa
- Form con label associate
- Errori form annunciati

## Test manuali
- Navigazione solo tastiera
- Screen reader test base
- Zoom 200 percento
- Riduzione movimento attiva

---

# 10. PERFORMANCE BUDGET

## Target
- LCP < 2.5s
- CLS < 0.1
- INP < 200ms
- JS iniziale < 180kb gzip

## Strategie
- Image optimization
- Code splitting
- Lazy load componenti pesanti
- Compressione font

---

# 11. QA E REGRESSION

## Smoke test
- Home carica correttamente
- Menu funziona
- Form invia correttamente
- API rispondono 200

## Regression
- CRUD entità principali
- Auth login logout
- Animazioni non bloccano scroll
- Mobile layout corretto

## Edge case
- API timeout
- Input vuoti
- Input molto lunghi
- Utente non autenticato

---

# 12. DEPLOY

## Ambiente
- Hosting
- Database provider
- CDN

## Variabili ambiente
- DATABASE_URL
- AUTH_SECRET
- API_BASE_URL

## Pipeline
- Lint
- Build
- Test
- Deploy

---

# 13. BACKLOG OPERATIVO

## Fase 1
- Setup repo
- Setup DB
- Setup auth

## Fase 2
- Implementazione API core
- Implementazione UI base

## Fase 3
- Animazioni
- Ottimizzazioni

## Fase 4
- Accessibilità
- QA completo

---

# 14. CASE STUDY TEMPLATE

## Problema
Descrizione sintetica del bisogno cliente.

## Soluzione
Tecnologie e scelte tecniche.

## Sfide tecniche
- 
- 

## Risultati
- 
- 

## Stack
- Next.js
- React
- R3F
- GSAP
- Postgres

---

# 15. DEFINIZIONE DI DONE

- Tutte le feature implementate
- Tutti i test smoke superati
- Checklist accessibilità completata
- Performance budget rispettato
- Deploy stabile
- Documentazione aggiornata

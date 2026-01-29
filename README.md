# TicketMaster - Gestionnaire de Tickets

Projet de gestion de tickets avec API Python FastAPI et frontend React.

## Installation

### Backend
```bash
cd backend
pip install fastapi uvicorn
```

### Frontend
```bash
cd frontend
npm install
```

## Lancement

### Méthode 1 : Les deux en même temps
```bash
npm run dev
```

### Méthode 2 : Séparément
**Backend :**
```bash
python -m uvicorn Backend.main:app --host 0.0.0.0 --port 8000 --reload
```

**Frontend :**
```bash
cd frontend
npm start
```

## Endpoints API

- **GET** `/tickets` - Récupérer tous les tickets
  - Paramètres optionnels : `status`, `priority`, `tag`, `sort_by`, `descending`
  
- **POST** `/tickets` - Créer un nouveau ticket
  - Body : `{"title": "...", "description": "...", "status": "...", "priority": "...", "tags": [...]}`
  
- **PATCH** `/tickets/{id}` - Modifier un ticket
  - Body : `{"status": "...", ...}`
  
- **DELETE** `/tickets/{id}` - Supprimer un ticket

## Structure du projet

```
TicketMaster/
├── Backend/
│   ├── tickets.json      
│   ├── script.py         
│   └── main.py           
├── frontend/
│   └── src/
│       ├── App.js        
│       └── components/
│           ├── TicketForm.js
│           └── TicketService.js
└── package.json          
```

## URLs

- Frontend : http://localhost:3000
- Backend : http://localhost:8000
- Documentation API : http://localhost:8000/docs


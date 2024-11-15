# Aplicație de Gestionare a Sarcinilor în Laravel

## Descrierea Proiectului
Acest proiect reprezintă o aplicație web dezvoltată în Laravel pentru gestionarea sarcinilor într-o echipă. Aplicația permite crearea, vizualizarea, actualizarea și ștergerea sarcinilor, cu funcționalități de prioritizare și atribuire către membrii echipei.

## Structura Proiectului
- Controller-e implementate:
  - HomeController: Gestionează paginile principale
  - TaskController: Managementul sarcinilor (CRUD)
- View-uri și Componente:
  - Layout principal (app.blade.php)
  - Componente reutilizabile (task-card, task-priority)
  - Pagini pentru listare și detalii sarcini

## Răspunsuri la Întrebări Tehnice

### 1. Controller de Resurse în Laravel
Un controller de resurse în Laravel este o clasă care gestionează toate operațiunile CRUD pentru o anumită resursă. În proiectul nostru, folosim:
```php
Route::resource('tasks', TaskController::class);
```
Această singură linie creează automat următoarele rute:
- GET /tasks (index)
- GET /tasks/create (create)
- POST /tasks (store)
- GET /tasks/{id} (show)
- GET /tasks/{id}/edit (edit)
- PUT/PATCH /tasks/{id} (update)
- DELETE /tasks/{id} (destroy)

**Diferența față de rutarea manuală:**
- Rutare manuală necesită definirea individuală a fiecărei rute
- Controller-ul de resurse oferă o convenție standardizată și reduce codul necesar
- Urmează principiile REST automat

### 2. Avantaje Componente Anonime Blade
În proiect am folosit componente precum task-card și task-priority care oferă:
- Implementare rapidă fără clase PHP separate
- Logică simplificată în template
- Reutilizare ușoară a codului
- Întreținere simplificată

### 3. Metode HTTP pentru CRUD
- CREATE: POST (/tasks)
- READ: GET (/tasks și /tasks/{id})
- UPDATE: PUT/PATCH (/tasks/{id})
- DELETE: DELETE (/tasks/{id})

## Funcționalități Implementate
- Listare sarcini cu detalii
- Afișare prioritate vizuală
- Sistem de layout consistent
- Componente reutilizabile
- Rutare resource

## Funcționalități de Implementat
- Formulare pentru creare/editare
- Validare date
- Autentificare utilizatori
- Sistem de notificări
- Filtrare și căutare sarcini

## Tehnologii Utilizate
- Laravel Framework
- Blade Template Engine
- Tailwind CSS
- Componente Blade

## Concluzie
Proiectul demonstrează implementarea unui sistem de gestionare a sarcinilor folosind Laravel, cu focus pe scalabilitate și mentenabilitate prin utilizarea controller-elor de resurse și componentelor Blade. Structura modulară permite extinderea ușoară cu funcționalități adiționale.

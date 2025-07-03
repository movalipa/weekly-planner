# 🗓️ Weekly Task Planner

A **frontend-only** project built with **Next.js** and **TypeScript**, designed to help developers learn and practice **Clean Architecture** in a realistic client-side application.

---

## 📌 Project Description

The **Weekly Task Planner** is a simple task management app that allows users to plan and manage tasks for each day of the week (Monday to Sunday). It includes features such as creating, editing, deleting, and filtering tasks.

This is a **client-only** project — all data is stored in the browser using **LocalStorage**. No backend is required.

The focus is on implementing **Clean Architecture**, emphasizing **separation of concerns**, **modular design**, and **scalability**.

---

## 🔧 Tech Stack

- Next.js
- TypeScript
- LocalStorage (for persistence)
- (Optional) Zustand or Jotai for state management
- Tailwind CSS (optional, for styling)

---

## 🧩 Core Features

- [x] View tasks by day (Monday to Sunday)
- [x] Add a task (title, description, priority, optional tags)
- [x] Edit a task
- [x] Delete a task
- [x] Persist tasks using LocalStorage
- [x] Filter tasks by tag or priority
- [ ] (Bonus) Drag-and-drop tasks between days

---

## 🧱 Clean Architecture Layers

### 1. Domain Layer
- Business models: `Task`, `Priority`, `Tag`, etc.
- Pure logic, no dependencies
- Use cases: `createTask()`, `updateTask()`, `deleteTask()`, `getTasksByDay()`

### 2. Application Layer
- Coordinates use cases and state
- Exposes services or hooks to the UI

### 3. Infrastructure Layer
- Handles LocalStorage interactions
- Implements interfaces from domain layer

### 4. Presentation Layer
- React components and pages
- Handles UI only (no business logic)

---

## 📁 Folder Structure (Optional)
```bash
/src
  /pages
    index.tsx
  /components
    WeeklyBoard.tsx
    TaskForm.tsx
    TaskCard.tsx
  /domain
    /models
      Task.ts
    /usecases
      createTask.ts
      updateTask.ts
      deleteTask.ts
      getTasksByDay.ts
  /application
    /services
      TaskService.ts
    /state
      useTaskStore.ts
  /infrastructure
    /repositories
      LocalTaskRepository.ts

```

---

## ✅ Definition of Done (DoD)

### 📦 Functional Requirements

- [ ] Tasks can be created, edited, and deleted.
- [ ] Tasks are displayed per day.
- [ ] Tasks persist using LocalStorage.
- [ ] Tasks can be filtered by tag and priority.
- [ ] UI is responsive and user-friendly.
- [ ] React components contain no business logic.

### 🧱 Architecture Requirements

- [ ] Code is separated by domain, application, infrastructure, and presentation layers.
- [ ] Domain models are framework-agnostic.
- [ ] Use cases are placed in domain and are unit-testable.
- [ ] Repositories are abstracted as interfaces.
- [ ] Infrastructure implements repository interfaces (e.g., LocalStorageRepo).
- [ ] Components interact with the app layer via services/hooks.

### 🧪 Quality Requirements

- [ ] TypeScript used across all files.
- [ ] Code is modular, readable, and maintainable.
- [ ] No circular dependencies between layers.
- [ ] No logic is duplicated across layers.

### ✅ Optional Bonus (Advanced)

- [ ] Implement drag-and-drop between days.
- [ ] Use Zustand or Jotai for state management.
- [ ] Write unit tests for use cases in the domain layer.

---

## 🚀 Getting Started

> To be filled in by the team after project setup.

---

## 👥 Purpose

This project is intended as a **learning tool** for frontend developers to practice **Clean Architecture principles** in a real-world, frontend-only application.

---

# Portfolio Platform - API Specification

## Overview

This document defines the REST API endpoints used by the Portfolio Platform.

The API will be consumed by:

* React Web Application
* Admin Dashboard
* Future Flutter Mobile Application

Base URL:

```text
/api
```

---

## HTTP Methods

* GET → Retrieve data
* POST → Create new data
* PUT → Update existing data
* DELETE → Remove data

---

## Authentication API

### Admin Login

```http
POST /api/auth/login
```

Used to authenticate the admin and return a JWT token.

---

## Projects API

### Get All Projects

```http
GET /api/projects
```

Returns all portfolio projects.

### Get Project Details

```http
GET /api/projects/:id
```

Returns detailed information about a specific project.

### Create Project

```http
POST /api/projects
```

Protected route.

Used by the admin to create a new project.

### Update Project

```http
PUT /api/projects/:id
```

Protected route.

Used by the admin to update an existing project.

### Delete Project

```http
DELETE /api/projects/:id
```

Protected route.

Used by the admin to delete a project.

---

## Skills API

### Get All Skills

```http
GET /api/skills
```

Returns all skills displayed in the portfolio.

### Create Skill

```http
POST /api/skills
```

Protected route.

Used by the admin to add a new skill.

### Update Skill

```http
PUT /api/skills/:id
```

Protected route.

Used by the admin to update an existing skill.

### Delete Skill

```http
DELETE /api/skills/:id
```

Protected route.

Used by the admin to delete a skill.

---

## Messages API

### Send Message

```http
POST /api/messages
```

Allows visitors to send contact messages.

### Get All Messages

```http
GET /api/messages
```

Protected route.

Returns all contact messages for the admin dashboard.

### Delete Message

```http
DELETE /api/messages/:id
```

Protected route.

Used by the admin to delete a message.

---

## Upload API

### Upload Project Image

```http
POST /api/upload/project-image
```

Protected route.

Uploads project images to Cloudinary.

### Upload CV

```http
POST /api/upload/cv
```

Protected route.

Uploads or updates the portfolio CV.

---

## Future AI Features

### Skill Matching API

```http
POST /api/ai/skill-match
```

Future feature.

Compares job requirements with portfolio skills and returns matching results.

---

## API Security

Protected routes require JWT authentication.

Only authenticated admin users can access dashboard management endpoints.

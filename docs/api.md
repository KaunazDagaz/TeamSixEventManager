# API Specification — EventManager

## Base URL
/api

## Authentication
All protected endpoints require:

Authorization: Bearer

---

# Authentication

## POST /auth/register
Register a new user

### Request
{
  "email": "user@mail.com",
  "password": "string"
}

### Response
{
  "message": "User registered successfully"
}

---

## POST /auth/login
Authenticate user and return JWT token

### Request
{
  "email": "user@mail.com",
  "password": "string"
}

### Response
{
  "token": "jwt_token_here"
}

---

## POST /auth/verify-email
Verify user email

### Request
{
  "token": "verification_token"
}

### Response
{
  "message": "Email verified"
}

---

# Events

## GET /events
Get list of events

### Query Parameters
| Name | Type | Description |
|------|------|------------|
| page | int | Page number |
| pageSize | int | Items per page |
| tag | string | Filter by tag |

### Response
[
  {
    "id": 1,
    "title": "Concert",
    "date": "2026-05-01",
    "location": "City",
    "likes": 10,
    "attendees": 5
  }
]

---

## GET /events/{id}
Get event details

### Response
{
  "id": 1,
  "title": "Concert",
  "description": "Event description",
  "date": "2026-05-01",
  "location": "City",
  "price": 20,
  "likes": 10,
  "attendees": 5
}

---

## POST /events
Create event (Organizer only)

### Request
{
  "title": "Concert",
  "description": "Description",
  "date": "2026-05-01",
  "location": "City",
  "price": 20
}

### Response
{
  "message": "Event created"
}

---

## PUT /events/{id}
Update event

### Request
{
  "title": "Updated title",
  "description": "Updated description"
}

### Response
{
  "message": "Event updated"
}

---

## DELETE /events/{id}
Delete event

### Response
{
  "message": "Event deleted"
}

---

# User Interactions

## POST /events/{id}/like
Like event

### Response
{
  "message": "Event liked"
}

---

## DELETE /events/{id}/like
Remove like

### Response
{
  "message": "Like removed"
}

---

## POST /events/{id}/attend
Mark "Want to Attend"

### Response
{
  "message": "Marked as attending"
}

---

## DELETE /events/{id}/attend
Remove attendance

### Response
{
  "message": "Attendance removed"
}

---

# Comments

## GET /events/{id}/comments
Get event comments

### Response
[
  {
    "id": 1,
    "user": "user@mail.com",
    "content": "Nice event!",
    "createdAt": "2026-05-01"
  }
]

---

## POST /events/{id}/comments
Add comment (Verified users only)

### Request
{
  "content": "Nice event!"
}

### Response
{
  "message": "Comment added"
}

---

# User Profile

## GET /users/me
Get current user profile

### Response
{
  "email": "user@mail.com",
  "likedEvents": [],
  "attendingEvents": []
}

---

# Moderator

## GET /admin/users
Get list of users

---

## POST /admin/block/{userId}
Block user

---

## POST /admin/unblock/{userId}
Unblock user

---

## POST /admin/approve-organizer/{userId}
Approve organizer role

---

# Error Format

All errors return:

{
  "message": "Error description"
}
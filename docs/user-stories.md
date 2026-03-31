# 📘 Event Manager — User Stories

---

## US-001: User Registration
**As a** guest  
**I want to** register an account  
**So that** I can access application features  

### Acceptance Criteria
- [ ] Registration form includes email and password
- [ ] Email must be validated
- [ ] Password must be at least 8 characters
- [ ] Email must be unique
- [ ] User is successfully created

---

## US-002: User Login
**As a** registered user  
**I want to** log into the system  
**So that** I can access my account  

### Acceptance Criteria
- [ ] User can enter email and password
- [ ] Valid credentials allow login
- [ ] Invalid credentials show error message
- [ ] JWT token is returned after login

---

## US-003: View Events List
**As a** guest  
**I want to** browse events  
**So that** I can discover interesting activities  

### Acceptance Criteria
- [ ] Events are displayed on the homepage
- [ ] Each event shows title, date, and location
- [ ] Events are loaded from backend
- [ ] Clicking event opens details page

---

## US-004: Filter Events
**As a** guest  
**I want to** filter events  
**So that** I only see relevant ones  

### Acceptance Criteria
- [ ] User can filter by category/tag
- [ ] User can filter by date
- [ ] Filter updates results dynamically

---

## US-005: View Event Details
**As a** guest  
**I want to** view detailed information about an event  
**So that** I can decide if I’m interested  

### Acceptance Criteria
- [ ] Event page shows description
- [ ] Displays date and time
- [ ] Displays price
- [ ] Displays likes count
- [ ] Displays comments (read-only)

---

## US-006: Like Event
**As a** user  
**I want to** like or unlike an event  
**So that** I can express my interest  

### Acceptance Criteria
- [ ] User can like an event
- [ ] User can remove like
- [ ] Like count updates correctly

---

## US-007: Mark Event as "Want to Attend"
**As a** user  
**I want to** mark events I want to attend  
**So that** I can track them  

### Acceptance Criteria
- [ ] User can mark event as attending
- [ ] Event appears in user profile
- [ ] User can remove event from list

---

## US-008: View User Profile
**As a** user  
**I want to** view my profile  
**So that** I can manage my activity  

### Acceptance Criteria
- [ ] Profile displays user information
- [ ] Shows liked events
- [ ] Shows planned events

---

## US-009: Email Verification
**As a** user  
**I want to** verify my email  
**So that** I can unlock full functionality  

### Acceptance Criteria
- [ ] Verification email is sent
- [ ] Email contains confirmation link/token
- [ ] User becomes verified after confirmation

---

## US-010: Comment on Event
**As a** verified user  
**I want to** comment on events  
**So that** I can share my opinion  

### Acceptance Criteria
- [ ] Only verified users can comment
- [ ] Comment is saved in database
- [ ] Comment appears in event page

---

## US-011: Create Event
**As an** organizer  
**I want to** create events  
**So that** users can discover them  

### Acceptance Criteria
- [ ] Event creation form exists
- [ ] Includes title, description, date, price
- [ ] Event is saved in database
- [ ] Only organizers can create events

---

## US-012: Edit Event
**As an** organizer  
**I want to** edit my events  
**So that** I can update information  

### Acceptance Criteria
- [ ] Organizer can edit own events only
- [ ] Changes are saved successfully

---

## US-013: View Event Analytics
**As an** organizer  
**I want to** view analytics  
**So that** I understand user engagement  

### Acceptance Criteria
- [ ] Shows number of likes
- [ ] Shows number of attendees
- [ ] Displays activity graph

---

## US-014: Manage Users
**As a** moderator  
**I want to** manage users  
**So that** I can enforce platform rules  

### Acceptance Criteria
- [ ] Moderator can view users list
- [ ] Can search users
- [ ] Can block/unblock users

---

## US-015: Remove Content
**As a** moderator  
**I want to** remove inappropriate content  
**So that** the platform remains safe  

### Acceptance Criteria
- [ ] Moderator can delete comments
- [ ] Moderator can delete events if necessary

---

## US-016: Approve Organizer Requests
**As a** moderator  
**I want to** approve organizer requests  
**So that** trusted users can create events  

### Acceptance Criteria
- [ ] Moderator sees pending requests
- [ ] Can approve or reject requests
- [ ] User role updates after approval

---

## US-017: Assign Moderator Role
**As a** moderator  
**I want to** promote users to moderators  
**So that** admin workload is shared  

### Acceptance Criteria
- [ ] Moderator can assign moderator role
- [ ] Cannot demote other moderators

---

## US-018: Role-Based Authorization
**As a** system  
**I want to** restrict access based on roles  
**So that** users only access allowed features  

### Acceptance Criteria
- [ ] Unauthorized access is blocked
- [ ] Role checks are enforced in backend

---

## US-019: Error Handling
**As a** user  
**I want to** see clear error messages  
**So that** I understand what went wrong  

### Acceptance Criteria
- [ ] Errors return meaningful messages
- [ ] UI displays error feedback

---

## US-020: Performance
**As a** user  
**I want to** experience fast loading  
**So that** I have a smooth experience  

### Acceptance Criteria
- [ ] Pages load within acceptable time
- [ ] API responses are optimized
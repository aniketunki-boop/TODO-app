# User Stories: Todo API

## Create
- **US-01** As a user, I want to create a todo with a name, so that I can track a task.
  - AC: valid name returns 201 and the new todo with status `pending`.
- **US-02** As a user, I want an empty name rejected, so that bad data isn't saved.
  - AC: empty name returns 400 with an error message.

## Read
- **US-03** As a user, I want to get a todo by ID, so that I can see its details.
  - AC: existing ID returns 200.
- **US-04** As a user, I want a clear error for a missing todo.
  - AC: unknown ID returns 404.

## List
- **US-05** As a user, I want todos in pages, so that the list loads fast.
  - AC: `limit=20` returns at most 20 items plus `next_cursor`.
- **US-06** As a user, I want invalid cursors rejected.
  - AC: bad cursor returns 400.

## Update
- **US-07** As a user, I want to change a todo's status, so that I can track progress.
  - AC: valid status returns 200 with the updated todo.

## Delete
- **US-08** As a user, I want to delete a todo.
  - AC: returns 204; a later GET returns 404.
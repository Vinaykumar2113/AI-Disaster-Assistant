# Database Design
The project uses PostgreSQL as the primary database.
## Table: Users
| Column        | Type      |
| ------------- | --------- |
| id            | UUID      |
| full_name     | VARCHAR   |
| email         | VARCHAR   |
| password_hash | VARCHAR   |
| role          | VARCHAR   |
| phone_number  | VARCHAR   |
| created_at    | TIMESTAMP |

---

## Table: Disaster Reports

| Column        | Type      |
| ------------- | --------- |
| id            | UUID      |
| user_id       | UUID      |
| disaster_type | VARCHAR   |
| description   | TEXT      |
| latitude      | FLOAT     |
| longitude     | FLOAT     |
| image_url     | TEXT      |
| severity      | VARCHAR   |
| status        | VARCHAR   |
| created_at    | TIMESTAMP |

---

## Table: Shelters

| Column             | Type    |
| ------------------ | ------- |
| id                 | UUID    |
| shelter_name       | VARCHAR |
| address            | TEXT    |
| latitude           | FLOAT   |
| longitude          | FLOAT   |
| capacity           | INTEGER |
| available_capacity | INTEGER |

---

## Table: Emergency Officers

| Column       | Type    |
| ------------ | ------- |
| id           | UUID    |
| user_id      | UUID    |
| department   | VARCHAR |
| phone_number | VARCHAR |

---

## Table: Notifications

| Column     | Type      |
| ---------- | --------- |
| id         | UUID      |
| user_id    | UUID      |
| title      | VARCHAR   |
| message    | TEXT      |
| is_read    | BOOLEAN   |
| created_at | TIMESTAMP |

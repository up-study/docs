# User
| field               | type              |
|---------------------|-------------------|
| id                  | uuid              |
| first_name          | char              |
| last_name           | char              |
| username            | char              |
| email               | email             |
| phone               | phone number field |
| telegram_id         | int               |
| cources             | m2m Cources       |
| followers           | m2m Users         |
| profile_photo       | image             |
| posts               | m2o Posts         |
| email_notifications | bool              |
| wa_notifications    | bool              |
| tg_notifications    | bool              |
| organizations       | m2m Organization  |

# Organization
| field   | type                                 |
|---------|--------------------------------------|
| id      | uuid                                 |
| owner   | o2o User                             |
| members | m2m User through  OrganizationMember |

# OrganizationMember
| field           | type                                           |
|-----------------|------------------------------------------------|
| id              | int                                            |
| user_id         | uuid                                           |
| organization_id | uuid                                           |
| private         | true                                           |
| role            | int(OrganizationRoles.choices, default=member) |

# Profile
- user o2o User | None
- organization o2o Organization | None

```python
from enum import IntEnum

class OrganizationRoles(IntEnum):
    MEMBER = 1
    CO_OWNER = 3
    OWNER = 3
```
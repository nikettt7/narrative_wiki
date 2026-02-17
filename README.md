# Bhaarat Wiki
### Official Character Compendium for *The Age of Bhaarat* by Tara Gaming

---

## Stack

| Layer    | Technology       |
|----------|-----------------|
| Frontend | Next.js 14      |
| Database | Supabase (PostgreSQL) |
| Auth     | Supabase Auth   |
| Hosting  | Vercel          |

---

## 👥 User Roles

| Role   | Can Do                                              |
|--------|-----------------------------------------------------|
| Reader | Browse all characters and read all wiki content     |
| Editor | Create characters, edit all sections and infoboxes  |
| Admin  | Everything above + elevated permissions             |

To promote someone to Editor, run in Supabase SQL Editor:
```sql
update public.profiles set role = 'editor'
where id = (select id from auth.users where email = 'their@email.com');
```

## Each Character Has

- **Infobox** with 5 categories: Biographical · Physical · Relationships · Magical Characteristics · Affiliation
- **Introduction paragraph**
- **Table of Contents** (auto-generated)
- **7 Sections**: Biography · Physical Description · Personality · Abilities & Skills · Relationships · Etymology · Appearances

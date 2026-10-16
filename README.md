# DocTrade Starter

This starter covers the first implementation phase:

- Next.js App Router
- TypeScript
- Supabase SSR authentication
- Patient and healthcare-professional registration
- Server-side session handling
- Initial Supabase schema
- Patient / healthcare-professional / administrator role model
- RLS foundation
- Professional verification foundation
- Practice-location foundation

## 1. Install

```powershell
npm install
```

## 2. Configure Supabase

Copy:

```text
.env.example
```

to:

```text
.env.local
```

Fill in:

```text
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=
```

Use the current Supabase Project URL and Publishable Key from the Supabase dashboard.

Never put a Supabase secret/service-role key in a `NEXT_PUBLIC_*` variable.

## 3. Apply the database schema

Run:

```text
supabase/migrations/001_initial_schema.sql
```

in the Supabase SQL Editor, or use the Supabase CLI migration workflow.

The schema intentionally starts with a secure RLS foundation. More tables will be added as the DocTrade features are implemented.

## 4. Start

```powershell
npm run dev
```

Open:

```text
http://localhost:3000
```

## Important

The registration form accepts a requested professional role in Auth metadata, but the database trigger deliberately creates every new account as `patient`.

Do not use editable `user_metadata` as authorization.

The professional role must be granted by the application/database workflow later, after the professional profile and verification process are implemented.

## Next implementation phase

1. Complete role onboarding.
2. Build professional profile creation.
3. Build specialty/service management.
4. Build practice-location management.
5. Add PostGIS and Find Doctors Near Me.
6. Build availability and appointment booking.
7. Add patient and professional dashboards.
8. Add administrator verification.

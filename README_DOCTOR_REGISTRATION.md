# DocTrade Doctor Registration Patch

This patch adds the first production feature after authentication:
- `/register/doctor`
- doctor account creation
- professional profile fields
- specialty selection
- practice location
- consultation type selection
- secure Supabase RPC to create a pending doctor profile
- `/doctor/dashboard`
- homepage and registration links

## Apply

Copy the files in `DocTrade/` over the matching paths in your local project.

Run the SQL migration in Supabase SQL Editor:
`DocTrade/supabase/migrations/002_doctor_registration.sql`

Then restart:
`npm run dev`

If email confirmation is enabled, the doctor will need to confirm their email and then log in before the professional profile can be completed.

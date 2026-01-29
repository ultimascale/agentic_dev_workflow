# Tech stack

Summary: "Solito/Superbase/React(Native) -> Vercel"

- General setup
    - Typescript wherever possible
    - Linters (e.g. ESLint)
- Repo
    - git (Monorepo)
        - Branches:
            - main (production)
            - dev (for development - no deployment)
            - staging (for staging - deployment to Vercel for manual testing)
    - hosted on Github
        - CI / CD with Github Actions
- Frontend
    - React (Typescript)
    - Next.js
    - ReactNative / Expo
    - Solito
    - Tailwind CSS / NativeWind
- Database
    - Supabase (based on PostgreSQL)
- Auth: Supabase Auth
- Deployment
    - Vercel
        - for frontend and early stage backend
        - later maybe AWS Lambda or containerize w/ Docker & Kubernetes
    - EAS
- Analytics
    - Google Analytics 4
    - Firebase analytics on Mobile
    - Prometheus + Grafana
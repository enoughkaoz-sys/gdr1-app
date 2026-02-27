# GDR App (Expo + Supabase) — MVP

MVP do app do clan **GDR** (Expo Router + Supabase):
- Login/Cadastro (Supabase Auth)
- Perfis com roles: Admin / Analista / Competitivo / Casual
- Aprovação de novos usuários (Admin)
- Táticos por Mapa/Modo (com link de vídeo)
- Fórum (posts, com link de vídeo)
- Chat (mensagens) + Status manual: offline/online/in-game
- Android + Web (Expo)

## 1) Supabase
1) Crie um projeto no Supabase
2) SQL Editor:
- Rode `supabase/schema.sql`
- Rode `supabase/policies.sql`
3) Settings → API:
- Project URL
- anon public key

## 2) Variáveis de ambiente
Crie `.env` na raiz baseado em `.env.example`:
EXPO_PUBLIC_SUPABASE_URL=...
EXPO_PUBLIC_SUPABASE_ANON_KEY=...

## 3) Rodar
npm i
npx expo start

## 4) Build APK via EAS
npm i -g eas-cli
eas login
eas build -p android --profile preview

## 5) Primeiro Admin
No Supabase → Table Editor → `profiles`:
- seu usuário: `approved=true` e `role=admin`

# FriendConnect Luxe

Luxury dark-plum and champagne-gold starter for a dating PWA, including the user's supplied UPI QR image.

## Android / GitHub Codespaces
1. Upload all extracted project files into a GitHub repository.
2. Open Codespaces for that repository.
3. Run `npm install`.
4. Copy `.env.example` to `.env.local` and fill in your own Supabase URL and publishable key.
5. Run `npm run dev -- --host 0.0.0.0`, then open port 5173 in the Ports panel.

## Deploy
Import the repository into Vercel and set `VITE_SUPABASE_URL` and `VITE_SUPABASE_PUBLISHABLE_KEY` environment variables.

## Important
This is a polished starter, not a finished production dating app. Real profile management, mutual-match creation, secure chat policies, block/report actions, admin authorization, age verification, account deletion, and server-side payment verification still need implementation and testing.

The QR image is displayed as supplied. The current payment submission uses a placeholder `amount_paise: 1` and must not be used for real paid subscriptions until plan prices and a secure server-side admin approval function are implemented. QR scan does not itself prove payment. Verify the transaction in the recipient account/UPI records. Never store UPI PINs, OTPs, or bank passwords in this app. Never expose Supabase service-role keys in frontend code.

Before public launch, configure database RLS policies for every table, prevent self-assigned admin privileges, ensure only mutually matched and unblocked users can message, restrict profile access, and implement a real 18+ age gate. A checkbox alone is not age verification.

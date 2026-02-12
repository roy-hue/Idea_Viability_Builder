# IdeaCatalyst
A business idea validation platform that transforms raw concepts into investor-ready business plans using AI-powered analysis.






Technical Architecture

Frontend (React)
A. Pages: Home, IdeaCreator, Pricing, SubscriptionSuccess
B. Components: Form inputs, results display, stakeholder cards, pricing models
C. State Management: React Query for data fetching
D. Styling: Tailwind CSS + Framer Motion animations

Backend (Deno Functions)
A. createCheckout - Stripe checkout session creation
B. stripeWebhook - Payment event processing
C. getSubscriptionStatus - User subscription limits
D. createSubscriptionRecord - Auto-create free tier on signup

Database (Base44 Entities)
A. BusinessIdea - Stores analyzed ideas with RLS (users see only their own)
B. Subscription - User subscription data, plan type, Stripe IDs
C. AppPhase - Global phase tracking based on customer count
D. User - Built-in authentication

Integrations
A. Stripe - Payment processing
B. Base44 Core.InvokeLLM - AI analysis with structured JSON output




User Flow

A. Landing (Home) → View features, CTA to get started
B. Sign Up/Login → Auto-creates free subscription
C. Create Idea (IdeaCreator) → Submit business concept
D. AI Analysis → Generates comprehensive breakdown
E. View Results → Incentive stack, stakeholders, pricing, operations
F. Upgrade (Pricing) → Hit limit or want more features
G. Checkout → Stripe payment flow
H. Success → Redirected with confirmation




Security Features

A. Row-level security (RLS) on BusinessIdea entity
B. Server-side Stripe key handling only
C. User authentication required for all operations
D. Webhook signature verification

Current State

✅ Fully functional subscription system
✅ AI-powered idea analysis
✅ Stripe integration (test mode ready)
✅ Phase tracking enabled
✅ Responsive design
⚠️ Using test Stripe keys (needs production keys for launch)


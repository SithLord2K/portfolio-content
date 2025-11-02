### Pool League Hub - A Multi-Tenant League Management Platform

Pool League Hub is a comprehensive, multi-tenant SaaS (Software as a Service) application designed to modernize and streamline the management of pool leagues. Built with Blazor Server and .NET 9, it provides a centralized, interactive, and full-featured platform for players, captains, and administrators, moving beyond simple spreadsheets and static websites.

Each league operates on its own dedicated subdomain, offering a dynamic environment with support for multiple subscription tiers (Free and Premium), managed via Stripe.

**Note:** This is a proprietary, closed-source commercial project. The source code is not public.

---

#### Tech Stack

* **Framework:** **.NET 9 / ASP.NET Core**
* **Front-end:** **Blazor Server**
* **Component Library:** **MudBlazor**
* **Database:** **SQL Server** with **Entity Framework Core 9**
* **Authentication:** **Auth0** (for user management and roles)
* **Payments:** **Stripe** (for subscriptions and payment processing)
* **Real-time:** **SignalR**
* **Skill Rating:** **OpenSkillSharp**
* **Reporting:** **QuestPDF**
* **Logging:** **Serilog**

---

#### Key Features

#### Core Platform & Super Admin
* **Multi-Tenant Architecture:** The app serves unique league data based on the request's subdomain.
* **Subscription Tiers (Free & Premium):** Dynamically shows or hides features based on a league's Stripe subscription status.
* **Stripe Payment Integration:** Full integration with Stripe Checkout and webhooks to handle payment events.
* **Super Admin Dashboard:** A separate dashboard for the platform owner to manage all leagues, users, and subscription plans.
* **User & Role Management:** Integrates with the Auth0 Management API to allow a Super Admin to view all users and assign roles.

#### League Admin & Team Captain Features
* **League Setup Wizard:** A step-by-step wizard for new league admins to create their first venue, team, and player.
* **Automatic Schedule Generator:** A complex service that creates balanced round-robin schedules, respecting home/away constraints and venue availability.
* **Live Scoring:** A real-time, mobile-friendly scoresheet powered by SignalR that allows captains to submit scores live.
* **OpenSkill Player Skill Rating:** Automatically recalculates and updates player skill ratings after every match.
* **Player Pool ("Free Agents"):** A dedicated page for team captains to view and recruit unassigned players to their team.
* **Tournament Management (Work in progress):** An admin-facing feature to create and manage single-elimination tournaments.
* **Automated Weekly Recaps:** A premium feature that analyzes the week's games to find the "Top Performer" and "Upset of the Week".
* **PDF Report Generation:** Admins can download printable PDF reports for team standings, player standings, and weekly results.

#### Player & User Features
* **Personalized Player Hub:** A dashboard for logged-in players showing their next match, recent performance, and achievements.
* **Real-Time Standings:** Public-facing pages for team and player standings that are automatically updated.
* **Player Profiles:** Individual profiles showing personal stats, season-by-season performance, and rating history.
* **Head-to-Head Comparison:** An analytics page allowing players to compare their stats and match history against any other player.
* **League Message Board:** A premium, forum-like feature for players to create posts and replies.
* **PWA (Progressive Web App):** The application is fully installable as a PWA for an app-like experience on mobile devices.

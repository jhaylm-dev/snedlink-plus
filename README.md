<div align="center">

# SNED-LINK+

**A school–home behavior monitoring platform for special-needs education.**
Teachers record observations, SNED coordinators give recommendations, and parents follow their child's day, all in one connected system.

![Platform](https://img.shields.io/badge/Parent_App-Mobile-7B1E32)
![Platform](https://img.shields.io/badge/Admin_&_Teacher-Web_+_Desktop-7B1E32)
![Desktop](https://img.shields.io/badge/Desktop-Wails-C9A24A)

</div>

---

## Overview

SNED-LINK+ connects the three groups involved in a child's learning support:

| Portal | Who uses it | Platform |
|---|---|---|
| **Parent Portal** | Parents / guardians | Mobile app (this README's screenshots) |
| **Teacher Portal** | Teachers | Web app, also packaged as a desktop app |
| **Admin Portal** | SNED coordinators / school admins | Web app, also packaged as a desktop app |

The admin and teacher portals are built as a web app and wrapped into a native desktop application using **[Wails](https://wails.io/)**, so schools can use them either in the browser or as an installed app.

---

## Parent Mobile App

<div align="center">

| Sign in | Home | Behavior |
|:---:|:---:|:---:|
| <img src="images/mobile/01-login.png" width="220" /> | <img src="images/mobile/02-home.png" width="220" /> | <img src="images/mobile/05-behavior.png" width="220" /> |

| Recommendations | More |
|:---:|:---:|
| <img src="images/mobile/03-recommendations.png" width="220" /> | <img src="images/mobile/04-more.png" width="220" /> |

</div>

### Features

**Secure, invitation-based onboarding**
- Parent accounts are created by the child's teacher; parents activate via an emailed invitation link
- Email/password sign-in with show/hide password, "Remember me", and password recovery

**Home dashboard**
- Child switcher card showing name, grade, and section
- Today's summary: counts of *Positive*, *Needs Support*, and *Alert* observations
- Weekly behavior trend (Mon–Fri) with a trend label (e.g. *Steady*)
- Latest teacher update and an active alert banner when teacher action is needed
- Notification bell with unread badge and one-tap refresh

**Behavior updates**
- Tabbed views: **Summary**, **Observations**, **Activity**, **Photos**
- Totals for positive vs. needs-support observations
- Most frequent behaviors with percentage breakdowns (e.g. *Off Task*, *Communicated Appropriately*, *Followed Instructions*)
- Color-coded observation levels: **Low** (Normal Monitoring), **Moderate** (Needs Monitoring), **High** (Immediate Attention)
- Plain-language explanation of what each level means

**Recommendations & concerns**
- **Overview** and **Concerns** tabs
- Concern timeline (latest and earlier concerns, with *Resolved* status)
- Observation results scored out of 20 points with a parent-friendly explanation
- Recommendations from the SNED Coordinator, with status tracking (e.g. *Recommendation Provided*)
- **Verified** badges marking teacher-confirmed records

**More**
- Manage children, attendance, and school activities
- Account settings, change password, and a Security Center
- Help & support, Rating Scale Guide, and About

---

## Admin & Teacher Portals (Web + Desktop)

<!-- Add screenshots from images/web and images/desktop, e.g.
<img src="images/web/dashboard.png" width="700" />
<img src="images/desktop/dashboard.png" width="700" />
-->

> Screenshots coming soon.

- **Teachers:** log behavior observations, manage students and parent invitations, post updates and photos, take attendance
- **SNED Coordinators / Admins:** review concerns, provide recommendations, manage users and school activities
- **Desktop build:** the same web app packaged with Wails for Windows/macOS/Linux

---

## Tech Stack

<!-- Fill in with what you actually used -->

| Layer | Technology |
|---|---|
| Parent mobile app | _e.g. Flutter / React Native_ |
| Admin & teacher web app | _e.g. React / Vue + TypeScript_ |
| Desktop wrapper | [Wails](https://wails.io/) (Go) |
| Backend / API | _e.g. Node.js / Go / Laravel_ |
| Database | _e.g. PostgreSQL / MySQL_ |
| Auth | _e.g. JWT, email invitation activation_ |

---

## Architecture

```
┌──────────────────┐      ┌─────────────────────────────┐
│ Parent Mobile App│      │ Admin & Teacher Web App     │
│                  │      │  └─ Wails desktop wrapper   │
└────────┬─────────┘      └──────────────┬──────────────┘
         │                               │
         └──────────────┬────────────────┘
                        ▼
               ┌─────────────────┐
               │    Backend API  │
               └────────┬────────┘
                        ▼
               ┌─────────────────┐
               │     Database    │
               └─────────────────┘
```

---

## Source Code

This is a **client project**, so the source code is private and not publicly available. This repository is a showcase of the system only.

If you'd like to know more about how it was built, feel free to reach out.

<!-- Add your contact links here, e.g. email / LinkedIn / portfolio -->

---

## My Role

Full stack development of the platform: design and implementation of the mobile app, web portals, desktop packaging, and backend.

---

## Notes

Screenshots use sample/demo data. This repository is a portfolio showcase of a client project; the source code is not included.

© 2026 SNED-LINK+. All rights reserved.

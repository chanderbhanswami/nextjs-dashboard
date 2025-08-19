# Next.js Dashboard Application

> A full-featured, modern dashboard web application built with Next.js 15 App Router, TypeScript, Tailwind CSS, NextAuth, and PostgreSQL. This project demonstrates best practices for authentication, data fetching, UI/UX, and scalable architecture.

---

## � Full File Structure

```
nextjs-dashboard/
├── app/
│   ├── layout.tsx                # Root layout for the app
│   ├── page.tsx                  # Root landing page
│   ├── dashboard/
│   │   ├── layout.tsx            # Dashboard layout
│   │   ├── (overview)/           # Overview section
│   │   │   ├── loading.tsx       # Loading skeleton for overview
│   │   │   └── page.tsx          # Overview page
│   │   ├── customers/
│   │   │   └── page.tsx          # Customers list page
│   │   └── invoices/
│   │       ├── error.tsx         # Error boundary for invoices
│   │       ├── page.tsx          # Invoices list page
│   │       ├── [id]/
│   │       │   └── edit/
│   │       │       ├── not-found.tsx # Not found page for invoice edit
│   │       │       └── page.tsx      # Edit invoice page
│   │       └── create/
│   │           └── page.tsx      # Create invoice page
│   ├── lib/
│   │   ├── actions.ts            # Server actions (CRUD, auth)
│   │   ├── data.ts               # Data fetching (Postgres queries)
│   │   ├── definitions.ts        # TypeScript types
│   │   ├── placeholder-data.ts   # Example/mock data
│   │   └── utils.ts              # Utility functions
│   ├── login/
│   │   └── page.tsx              # Login form page
│   ├── query/
│   │   └── route.ts              # API route for queries
│   ├── seed/
│   │   └── route.ts              # API route for seeding data
│   └── ui/
│       ├── acme-logo.tsx         # Logo component
│       ├── button.tsx            # Button component
│       ├── fonts.ts              # Font loading
│       ├── global.css            # Global styles
│       ├── home.module.css       # Home page styles
│       ├── login-form.tsx        # Login form UI
│       ├── search.tsx            # Search bar UI
│       ├── skeletons.tsx         # Skeleton loaders
│       ├── customers/            # Customer UI components
│       ├── dashboard/            # Dashboard UI components
│       └── invoices/             # Invoice UI components
├── public/
│   ├── favicon.ico
│   ├── hero-desktop.png
│   ├── hero-mobile.png
│   ├── opengraph-image.png
│   └── customers/
│       ├── amy-burns.png
│       ├── balazs-orban.png
│       ├── delba-de-oliveira.png
│       ├── evil-rabbit.png
│       ├── lee-robinson.png
│       └── michael-novotny.png
├── .env                         # Environment variables
├── .eslintrc.json               # ESLint config
├── .gitignore                   # Git ignore rules
├── auth.config.ts               # NextAuth config
├── auth.ts                      # NextAuth provider logic
├── middleware.ts                # Middleware for auth/redirects
├── next-env.d.ts                # Next.js type declarations
├── next.config.ts               # Next.js config
├── package.json                 # Project metadata & dependencies
├── pnpm-lock.yaml               # pnpm lockfile
├── postcss.config.js            # PostCSS config
├── README.md                    # Project documentation
├── tailwind.config.ts           # Tailwind CSS config
├── tsconfig.json                # TypeScript config
└── LICENSE                      # MIT License
```

---
## 📝 MIT License

This project is licensed under the MIT License:


> Copyright (c) 2025 Chanderbhan Swami

> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in all
> copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
> SOFTWARE.

---
## 🧩 Advanced Features & Extensibility

- **API Routes**: Easily add new API endpoints in `app/query/` or `app/seed/`.
- **Custom Middleware**: Use `middleware.ts` for authentication, redirects, or logging.
- **Theming**: Easily extend Tailwind config for custom themes.
- **Component-Driven**: All UI is modular and reusable.
- **Type Safety**: All data and props are fully typed with TypeScript.
- **Production Ready**: Easily deploy to Vercel, Netlify, or your own server.

---

## 🏗️ Database Schema (Example)

**users**
| id (UUID) | name (string) | email (string) | password (string, bcrypt hash) |

**customers**
| id (UUID) | name (string) | email (string) | image_url (string) |

**invoices**
| id (UUID) | customer_id (UUID) | amount (int, cents) | date (date) | status ('pending'|'paid') |

**revenue**
| month (string) | revenue (int) |

---

## 🏆 Best Practices Followed

- Environment variables for all secrets and DB connections
- Secure password hashing (bcrypt)
- Server actions for all mutations
- TypeScript for all code
- Modular, reusable UI components
- Linting and formatting enforced
- Error boundaries and user feedback

---

## 🛡️ Security Notes

- All sensitive data is stored securely in the database
- Passwords are never stored in plain text
- Authentication tokens are managed by NextAuth
- Environment variables are not committed to version control

---

## 🏢 Deployment

- **Vercel**: Zero-config deployment for Next.js
- **Netlify**: Supported with minor config
- **Custom Server**: Deploy anywhere Node.js is supported

---

## 🧪 Testing & Quality

- Linting: `npm run lint`
- Type checking: `tsc --noEmit`
- Manual and visual testing for all UI components

---

## 📈 Analytics & Monitoring

- Easily integrate Vercel Analytics, Sentry, or other monitoring tools

---

## 🗃️ Data Seeding & Migrations

- Use `app/seed/route.ts` for initial data population
- Database migrations can be managed with external tools (e.g., Prisma, Drizzle, or raw SQL)

---

## 🏷️ Versioning

- Follows semantic versioning for releases

---

## 🏁 Getting Help

- For issues, open a GitHub issue or contact the developer

---
# Next.js Dashboard Application

> A full-featured, modern dashboard web application built with Next.js 15 App Router, TypeScript, Tailwind CSS, NextAuth, and PostgreSQL. This project demonstrates best practices for authentication, data fetching, UI/UX, and scalable architecture.

---

## �🚀 Features

- **Next.js 15 App Router**: File-based routing, layouts, server components, and API routes.
- **Authentication**: Secure login with NextAuth.js and credentials provider (email/password, bcrypt hashed).
- **PostgreSQL Database**: All data (users, customers, invoices, revenue) is stored and queried from a Postgres database.
- **Tailwind CSS**: Utility-first CSS framework for rapid, responsive UI development.
- **TypeScript**: Full type safety across the codebase.
- **Zod Validation**: Robust form and data validation.
- **Modern UI**: Responsive dashboard, cards, tables, charts, skeleton loaders, and more.
- **Server Actions**: Secure server-side mutations for create, update, delete operations.
- **Error Handling**: Graceful error boundaries and user feedback.
- **Loading States**: Skeletons and spinners for async data fetching.
- **Custom Components**: Modular, reusable UI components for forms, tables, navigation, and more.
- **Environment Variables**: Secure configuration for database and secrets.
- **MIT License**: Open source and free to use.

---

## 🛠️ Tech Stack & Tools

- **Framework**: [Next.js 15 (App Router)](https://nextjs.org/)
- **Language**: [TypeScript](https://www.typescriptlang.org/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/), [PostCSS](https://postcss.org/)
- **Authentication**: [NextAuth.js](https://next-auth.js.org/)
- **Database**: [PostgreSQL](https://www.postgresql.org/) (with [postgres.js](https://github.com/porsager/postgres))
- **Validation**: [Zod](https://zod.dev/)
- **Icons**: [Heroicons](https://heroicons.com/)
- **UI Utilities**: [clsx](https://github.com/lukeed/clsx), [use-debounce](https://github.com/xnimorz/use-debounce)
- **Password Hashing**: [bcrypt](https://github.com/kelektiv/node.bcrypt.js)
- **Linting**: [ESLint](https://eslint.org/)
- **Other**: [pnpm](https://pnpm.io/) for package management

---

## 📦 Main Dependencies

```
@heroicons/react, @tailwindcss/forms, autoprefixer, bcrypt, clsx, next, next-auth, postcss, postgres, react, react-dom, tailwindcss, typescript, use-debounce, zod
```

**Dev Dependencies:**
```
@types/bcrypt, @types/node, @types/react, @types/react-dom, eslint, eslint-config-next
```

---

## 📋 Functionality Overview

- **Authentication**: Secure login with email and password (bcrypt hashed, checked against Postgres users table).
- **Dashboard**: Overview cards, revenue chart, latest invoices, and navigation.
- **Customers**: List, search, and view customer details.
- **Invoices**: List, search, create, edit, and delete invoices. Pagination and status tracking.
- **Server Actions**: All mutations (create, update, delete) are performed securely on the server.
- **Data Validation**: All forms use Zod for validation.
- **Error Handling**: User-friendly error messages and boundaries.
- **Loading States**: Skeleton loaders and spinners for async operations.
- **Responsive Design**: Works on all screen sizes.

---

## 📁 Key Files & Folders

- `app/lib/definitions.ts` – TypeScript types for all data models.
- `app/lib/data.ts` – All data fetching functions (Postgres queries).
- `app/lib/actions.ts` – Server actions for create, update, delete, and authentication.
- `app/lib/placeholder-data.ts` – Example data for development/testing.
- `app/ui/` – All UI components (buttons, forms, tables, skeletons, etc).
- `auth.ts` & `auth.config.ts` – NextAuth configuration and credentials provider logic.
- `.env` – Environment variables (DB connection, secrets, etc).

---

## ⚙️ Setup & Installation

1. **Clone the repository:**
	```sh
	git clone <your-github-repo-url>
	cd nextjs-dashboard
	```
2. **Install dependencies:**
	```sh
	pnpm install
	# or
	npm install
	```
3. **Configure environment variables:**
	- Copy `.env.example` to `.env` and fill in your Postgres connection string and secrets.
4. **Run the development server:**
	```sh
	pnpm dev
	# or
	npm run dev
	```
5. **Open in browser:**
	- Visit [http://localhost:3000](http://localhost:3000)

---

## 🧑‍💻 Developer Details

- **Author:** Chanderbhan Swami
- **GitHub:** [chanderbhanswami](https://github.com/chanderbhanswami)
- **Contact:** chanderbhanswami29@gmail.com

---

## 🌐 GitHub Repository

This project is open source and available on GitHub:

**Repo:** [https://github.com/chanderbhanswami/nextjs-dashboard](https://github.com/chanderbhanswami/nextjs-dashboard)

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---

## 📚 Additional Sections

### Environment Variables
- `POSTGRES_URL` – PostgreSQL connection string
- `NEXTAUTH_SECRET` – Secret for NextAuth
- `NEXTAUTH_URL` – App URL for NextAuth

### Project Structure Notes
- All business logic is in `app/lib/`
- All UI is in `app/ui/`
- All routing is file-based in `app/`

### How to Add Features
- Add new pages in `app/`
- Add new components in `app/ui/`
- Add new data models/types in `app/lib/definitions.ts`

### How to Contribute
- Fork the repo, create a branch, submit a pull request.

---

## 🙏 Acknowledgements

- [Next.js](https://nextjs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [NextAuth.js](https://next-auth.js.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [Zod](https://zod.dev/)
- [Heroicons](https://heroicons.com/)

---

## 📞 Support

For questions, issues, or feature requests, please open an issue on GitHub or contact the developer directly.

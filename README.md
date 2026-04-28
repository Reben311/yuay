# MSU-MCEST Campus Equipment Management System (Front-End)

Static front-end shell built with HTML + Tailwind CSS (CDN) + vanilla JavaScript.
Designed to be wired to a PHP + MySQL backend.

## Folder structure

```
/                           -> index.html (redirects to login)
/pages/                     -> all application pages (HTML)
/js/shared.js               -> shared logic (sidebar, modal, tabs, fade)
/js/<page>.js               -> optional page-specific JS
/assets/images/             -> logo / icons (placeholder)
/partials/                  -> suggested PHP includes location
                              (sidebar-admin.php, sidebar-student.php,
                               topbar.php, head.php, footer.php)
```

## How to use locally
Just open `index.html` in a browser. No build step required.
Tailwind is loaded via CDN.

## PHP integration notes
- Every page has `<!-- PHP: ... -->` comments where dynamic data should be injected.
- Forms use `method`, `action="REPLACE_WITH_PHP_ENDPOINT"`, and proper `name` attributes.
- Tables/cards have `<!-- PHP LOOP: ... -->` markers showing where to render rows.
- Auth/role-gating is marked with `<!-- PHP: session check (admin/student only) -->`.
- No real data is hardcoded; tables show empty states until the backend fills them.

## Pages
- Public: `login.html`, `register.html`
- Admin: `admin-dashboard.html`, `equipment.html`, `materials.html`, `students.html`,
         `users.html`, `requests.html`, `transactions.html`, `admin-settings.html`,
         `change-password.html`
- Student: `student-dashboard.html`, `student-browse.html`, `student-requests.html`,
           `student-change-password.html`

## Color tokens (Tailwind config inline)
- Primary navy:   #0B2545
- Navy dark:      #061A33
- Accent gold:    #D4A017
- Accent gold-2:  #B8860B
- Surface:        #F7F8FB
- Border:         #E5E7EB

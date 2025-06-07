
# Babynama Intern Assignment - Webinars Page

This project implements the "Upcoming Live Webinars" feature as part of the Babynama Frontend Intern Assignment.

## Live URL

[PASTE YOUR VERCEL DEPLOYMENT URL HERE]
*Example: `https://your-project-name.vercel.app/webinars`*

## Choices Made

I made the technical choice to separate the display of each webinar into its own `WebinarCard` component. This decision was driven by the principles of modularity and reusability. By creating a dedicated component, the main `/webinars` page component (`page.tsx`) remains cleaner and more focused on fetching and mapping the data. It also makes the individual webinar cards easier to style and maintain independently, improving the overall organization and readability of the codebase.

## Roadblock & Learning

One small thing I got stuck on was understanding the behavior of Server Components versus Client Components in Next.js 13+ App Router. Initially, my "View Details" button, which uses an `onClick` event handler, was causing a runtime error: `"Error: Event handlers cannot be passed to Client Component props."` because the component was being treated as a Server Component by default.

I solved this by adding the `'use client';` directive at the very top of my `app/webinars/page.tsx` file. This explicit directive signals to Next.js that the component (and its children) should be rendered on the client side, allowing for interactive features like event handlers to function correctly. This helped me deepen my understanding of Next.js's rendering environments.

## Screenshot

![Screenshot of Webinars Page UI](PASTE_PATH_TO_YOUR_SCREENSHOT_HERE)
*Example: `public/screenshot-webinars-page.png` or an external URL if hosted.*

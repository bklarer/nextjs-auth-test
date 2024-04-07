This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## initiate prisma with

```bash
npx prisma init --datasource-provider sqlite
```

## run migration

```bash
npx prisma migrate dev
```

## When Making Nextjs applications

- Recommends to Identify all the different routes you want your app to have and the data that each shows

- Make path helper functions

```javaScript
const paths = {
    homePage() {
        return '/'
    },
    topicShowPath(slug: string) {
        return `/content/topics/${slug}`
    },
    postCreatePath(slug: string) {
        return `/content/topics/${slug}/posts/new`
    },
    postShowPath(slug: string, postId: string) {
        return `/content/topics/${slug}/posts/${postId}`
    }
}
```

- Create your routing folders + pagetsx files based on step 1

- Identify the places where data changes in your app

- Make empty server actions for each of those

- Add in comments on what paths you'll need to revalidate for each server action

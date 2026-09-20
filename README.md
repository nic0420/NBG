# NBG — Plataforma de rifas

Aplicación para organizar y vender rifas online: el organizador crea el sorteo, los participantes compran números y pagan con Mercado Pago, y el sistema confirma el pago, envía el comprobante por mail y realiza el sorteo.

**Demo:** https://nbg-six.vercel.app

## Qué hace

- **Alta de rifas**: título, premio, cantidad de números y precio.
- **Venta de números** con reserva y control de disponibilidad.
- **Pago con Mercado Pago** y webhook que confirma la compra del lado del servidor.
- **Sorteo automático** entre los números vendidos.
- **Panel de administración** con estadísticas y listado de compras.
- **Emails** de confirmación al comprador.

## Modelo de datos

`Raffle` · `Ticket` · `Purchase` · `Admin`

## Stack

| Capa | Tecnología |
|---|---|
| Framework | Next.js 16 (App Router) + React 19 |
| ORM / base | Prisma 6 + PostgreSQL |
| Pagos | SDK de Mercado Pago + webhook |
| Emails | nodemailer y resend |
| Deploy | Vercel |

## Cómo correrlo

```bash
git clone https://github.com/nic0420/NBG.git
cd NBG
npm install
cp .env.example .env    # DATABASE_URL, credenciales de Mercado Pago y de mail
npx prisma migrate dev
npm run dev
```

## Historial

Continuación de [giorgio-raffle](https://github.com/nic0420/giorgio-raffle), la primera versión del proyecto.
This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

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

You can start editing the page by modifying `app/page.js`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

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

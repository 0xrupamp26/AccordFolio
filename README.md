# AccordFolio
# AccordFolio Web

Frontend for AccordFolio - A tokenized basket protocol on Aptos.

## Features

- Connect with Aptos wallets (Petra, Martian, Pontem, Rise)
- Browse and invest in pre-defined token baskets
- Create custom token baskets with custom allocations
- View portfolio performance and history
- Automatic rebalancing of baskets
- Price feeds integration with Pyth Network
- Transaction history and receipts

## Prerequisites

- Node.js 16.14 or later
- pnpm 7.x or later
- Aptos wallet browser extension (Petra, Martian, or Pontem)

## Getting Started

1. **Install Dependencies**

   ```bash
   pnpm install
   ```

2. **Set Up Environment Variables**

   Copy `.env.example` to `.env.local` and update the variables:

   ```bash
   cp .env.example .env.local
   ```

3. **Run the Development Server**

   ```bash
   pnpm dev
   ```

   Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

4. **Build for Production**

   ```bash
   pnpm build
   pnpm start
   ```

## Environment Variables

| Variable | Description | Required | Default |
|----------|-------------|----------|---------|
| `NEXT_PUBLIC_APTOS_NETWORK` | Aptos network to connect to (devnet, testnet, mainnet) | Yes | `devnet` |
| `NEXT_PUBLIC_BASKET_CORE_ADDRESS` | Address of the deployed BasketCore contract | Yes | `` |
| `NEXT_PUBLIC_BASKET_SHARE_ADDRESS` | Address of the BasketShare contract | Yes | `` |
| `NEXT_PUBLIC_INDEXER_URL` | URL of the AccordFolio indexer | No | `http://localhost:3001` |
| `NEXT_PUBLIC_PYTH_APT_USD_FEED_ID` | Pyth price feed ID for APT/USD | Yes | `` |
| `NEXT_PUBLIC_PYTH_USDC_USD_FEED_ID` | Pyth price feed ID for USDC/USD | Yes | `` |
| `NEXT_PUBLIC_PYTH_BTC_USD_FEED_ID` | Pyth price feed ID for BTC/USD | Yes | `` |

## Project Structure

```
src/
├── app/                    # App Router pages and layouts
│   ├── api/               # API routes
│   ├── components/        # Reusable UI components
│   ├── config/            # App configuration
│   ├── contexts/          # React contexts
│   ├── hooks/             # Custom React hooks
│   ├── lib/               # Utility functions
│   ├── styles/            # Global styles
│   └── types/             # TypeScript type definitions
├── public/                # Static files
│   ├── images/            # Image assets
│   └── tokens/            # Token icons
└── tests/                 # Test files
```

## Tech Stack

- **Framework**: [Next.js](https://nextjs.org/) 14 with App Router
- **UI**: [Tailwind CSS](https://tailwindcss.com/)
- **Wallet**: [@aptos-labs/wallet-adapter-react](https://github.com/aptos-labs/aptos-wallet-adapter)
- **State Management**: [Zustand](https://github.com/pmndrs/zustand)
- **Form Handling**: [React Hook Form](https://react-hook-form.com/)
- **Data Fetching**: [TanStack Query](https://tanstack.com/query/latest)
- **Type Safety**: TypeScript
- **Testing**: Jest + React Testing Library

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support, please open an issue or join our [Discord](https://discord.gg/aptos).


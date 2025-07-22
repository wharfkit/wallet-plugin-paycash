# @wharfkit/wallet-plugin-paycash

> **⚠️ Important Notice:**
> 
> Due to current limitations in the PayCash wallet, this plugin only supports authentication (login) via QR code. Transaction signing via QR code (ESR) is **not supported** by PayCash at this time. As a result, this plugin cannot be used for signing or broadcasting transactions through PayCash QR/ESR. If PayCash adds support for transaction ESR in the future, this plugin can be updated to enable full cold wallet functionality.

A Session Kit wallet plugin for the PayCash wallet.

## Overview

The PayCash wallet plugin enables users to authenticate and sign transactions using the PayCash wallet through QR code authentication. 

## Features

- 🔐 **QR Code Authentication** - Secure login through QR code scanning
- ☁️ **Cloud-Only Solution** - No mobile app installation required
- 🎨 **Embedded Logo** - Optimized PayCash logo included
- ⚡ **TypeScript Support** - Full TypeScript implementation
- 🌓 **Theme Support** - Light and dark theme compatibility
- 📱 **Cross-Platform** - Works on desktop and mobile browsers

## Installation

```bash
yarn add @wharfkit/wallet-plugin-paycash
```

## Usage

### Basic Setup

```typescript
import { WalletPluginPayCash } from '@wharfkit/wallet-plugin-paycash'
import { SessionKit } from '@wharfkit/session'

const kit = new SessionKit({
  appName: 'My App',
  chains: [
    {
      id: 'aca376f206b8fc25a6ed44dbdc66547c36c6c33e3a119ffbeaef943642f0e906',
      name: 'EOS Mainnet',
    },
  ],
  walletPlugins: [new WalletPluginPayCash()],
})
```

### Authentication Flow

1. User clicks "Login with PayCash"
2. QR code is displayed for scanning
3. User scans QR code with PayCash wallet
4. Authentication is completed securely

## Configuration

The plugin supports the following configuration options:

```typescript
const plugin = new WalletPluginPayCash({
  // Custom configuration options can be added here
})
```

## Development

### Prerequisites

- Node.js 16+
- yarn

### Setup

```bash
# Clone the repository
git clone https://github.com/zhenek73/wallet-plugin-paycash.git
cd wallet-plugin-paycash

# Install dependencies
yarn install

# Start development server
yarn start
```

### Building

```bash
# Build the plugin
yarn build

# Build with watch mode
yarn dev
```

## Testing

The plugin includes a test application for development and testing:

```bash
# Start test application
yarn start
```

Then visit `http://localhost:3000` to test the plugin functionality.

## Architecture

The plugin implements the WharfKit Session Kit wallet plugin interface:

- **Authentication**: QR code-based authentication flow
- **Transaction Signing**: Secure transaction signing through PayCash wallet
- **Session Management**: Proper session handling and cleanup

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support and questions:

- Create an issue on GitHub
- Check the [WharfKit documentation](https://wharfkit.com)
- Visit [PayCash documentation](https://paycash.app)

## Related

- [WharfKit Session Kit](https://github.com/wharfkit/session)
- [PayCash Wallet](https://paycash.app)
- [Antelope Blockchain](https://antelope.io)

---

Made with ❤️ for the Antelope ecosystem and Paycash

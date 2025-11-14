# CopyPasta

A simple, client-side text compression and sharing tool. Compress any text into a shareable URL using Gzip compression and Base64 encoding.

## Features

- **100% Client-Side**: All compression and decompression happens in your browser. No data is sent to any server.
- **Simple & Fast**: Paste text, get a link, share it.
- **URL-Based Sharing**: The compressed text is encoded directly in the URL hash.
- **Dark/Light Theme**: Toggle between themes with automatic detection based on system preferences.
- **Retro UI**: Minimal, monospace font-based interface inspired by classic web pages.
- **No Dependencies**: Pure HTML, CSS, and JavaScript. No build process required.

## How It Works

1. **Compression**: Enter your text in the textarea and click "Generate Link"
2. **Encoding**: The text is compressed using the browser's native Gzip compression API and encoded to Base64
3. **Sharing**: Copy the generated URL and share it with anyone
4. **Decompression**: When someone opens the link, the text is automatically decompressed and displayed

## Usage

### Option 1: Open Directly

Simply open `index.html` in any modern web browser. No server required!

### Option 2: Local Development Server

If you want to run a local server:

```bash
# Install dependencies (optional, uses npx if not installed)
npm install

# Start the server (opens browser automatically)
npm start

# Or just serve without opening browser
npm run serve
```

The app will be available at `http://localhost:8080`

### Option 3: Deploy to Static Hosting

Deploy the `index.html` file to any static hosting service:

- **GitHub Pages**: Push to a repository and enable GitHub Pages
- **Netlify**: Drag and drop the `index.html` file
- **Vercel**: Deploy with a single command
- **Cloudflare Pages**: Connect your repository
- **Any web server**: Just upload `index.html`

## Browser Compatibility

Requires a modern browser with Compression Streams API support:

- Chrome 80+
- Firefox 113+
- Safari 16.4+
- Edge 80+

## Technical Details

- **Compression Algorithm**: Gzip (using browser's native CompressionStream API)
- **Encoding**: URL-safe Base64 encoding
- **Storage**: URL hash fragment (no server-side storage)
- **Privacy**: All processing happens in the browser - your text never leaves your device

## Limitations

- Maximum URL length depends on the browser (typically ~2MB for most browsers)
- Very large texts may not work due to URL length limitations
- Requires JavaScript enabled in the browser

## License

MIT

## Contributing

Feel free to submit issues and pull requests!

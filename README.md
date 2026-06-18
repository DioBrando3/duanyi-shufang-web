# Duanyi Shufang

Duanyi Shufang is a browser-based reading app for EPUB books, comic archives, and common document formats. It is optimized for Safari usage so browser translation extensions, such as Immersive Translate, can work directly on the original text paragraphs.

Live site: https://diobrando3.github.io/duanyi-shufang-web/

## Features

- Import and read EPUB books.
- Open comic-style EPUB, CBZ, and ZIP image archives.
- Open document files: DOCX, ODT, RTF, TXT, Markdown, HTML, and HTM.
- Display original text as standard web paragraphs for translation extensions.
- Keep table of contents, chapter navigation, bookmarks, and reading position.
- Process imported files locally in the browser. Files are not uploaded to the server.

## Supported Files

| Type | Status | Notes |
| --- | --- | --- |
| `.epub` | Supported | Text EPUB and image/comic EPUB are supported. |
| `.cbz`, `.zip` | Supported | Used for comic/image archives. |
| `.docx` | Supported | Modern Word files. |
| `.odt` | Supported | OpenDocument text files. |
| `.rtf` | Supported | Basic RTF text extraction. |
| `.txt`, `.text` | Supported | Plain text files. |
| `.md`, `.markdown` | Supported | Markdown is converted to readable text. |
| `.html`, `.htm` | Supported | Common text elements are parsed as paragraphs. |
| `.doc` | Not supported | Convert old Word documents to `.docx` first. |

## Local Development

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Open:

```text
http://localhost:5174/
```

To test from an iPhone on the same Wi-Fi, open the Mac's local network address instead of `localhost`, for example:

```text
http://10.10.72.33:5174/
```

## Production Build

Build the static website:

```bash
npm run build
```

Preview the production build:

```bash
npm run preview
```

The generated static site is placed in:

```text
dist/
```

## GitHub Pages Deployment

This app is currently published at:

```text
https://diobrando3.github.io/duanyi-shufang-web/
```

For GitHub Pages under the `duanyi-shufang-web` repository path, build with:

```bash
VITE_BASE_PATH=/duanyi-shufang-web/ npm run build
```

Then publish the contents of `dist/` to the `main` branch of the GitHub Pages repository.

## iOS App Build

The project also includes a Capacitor iOS wrapper, but Safari is recommended when browser translation plugins are required.

Sync the latest web build into the iOS project:

```bash
npm run ios:sync
```

Open the Xcode project:

```bash
npm run ios:open
```

## Privacy

Imported books and documents are parsed in the browser. The published static website does not include a backend upload service, so selected files remain on the user's device/browser storage.

Translation extensions or external translation APIs may process visible text depending on the user's own extension or translation settings.

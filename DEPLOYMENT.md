# Deployment

## GitHub Pages

This project is a static website, so GitHub Pages is the simplest deployment option.

1. Create a GitHub repository.
2. Upload all project files.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, select:
   - Source: Deploy from a branch
   - Branch: `main`
   - Folder: `/ (root)`
5. Save.
6. GitHub will provide the Pages URL.

The URL will normally look like:

```text
https://YOUR-USERNAME.github.io/SmartTaskManagementSystem/
```

## Important

Do not put private API keys in `index.html`. If an external AI API is added later, call it through a backend server.

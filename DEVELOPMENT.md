# The Dropout Theme - Development Workflow

## 🚀 Quick Start

### Prerequisites
- Node.js 16+ installed
- Shopify CLI installed: `npm install -g @shopify/cli`
- Access to your Shopify store

### Initial Setup
1. **Authenticate with Shopify:**
   ```bash
   shopify auth login
   ```

2. **Connect to your store:**
   ```bash
   shopify theme dev --store=your-store.myshopify.com
   ```

## 📝 Development Workflow

### 1. Development Mode
```bash
npm run dev
# or
shopify theme dev
```
This starts a development server with live reloading.

### 2. Deploy Changes
```bash
npm run deploy
# or
shopify theme push
```
Deploy your local changes to the live theme.

### 3. Pull Remote Changes
```bash
npm run pull
# or
shopify theme pull
```
Download changes made in Shopify admin.

### 4. Theme Validation
```bash
npm run check
# or
shopify theme check
```
Validate your theme for errors and best practices.

## 🎯 Development Best Practices

### File Structure
- `sections/` - Reusable page sections
- `snippets/` - Reusable code snippets
- `templates/` - Page templates
- `assets/` - CSS, JS, images
- `config/` - Theme settings
- `locales/` - Translation files

### Git Workflow
1. Make changes locally
2. Test with `shopify theme dev`
3. Commit changes: `git add . && git commit -m "Description"`
4. Push to GitHub: `git push origin main`
5. Deploy to Shopify: `shopify theme push`

### Theme Settings
- Edit `config/settings_schema.json` for new settings
- Update `config/settings_data.json` for default values
- Use translation keys in `locales/` files

## 🔧 Common Commands

```bash
# Start development server
shopify theme dev

# Deploy to live theme
shopify theme push

# Pull from live theme
shopify theme pull

# Check theme for issues
shopify theme check

# List themes
shopify theme list

# Create new theme
shopify theme init

# Serve theme locally
shopify theme serve
```

## 📁 Key Files to Edit

### Theme Customization
- `templates/index.json` - Homepage layout
- `sections/header.liquid` - Header section
- `sections/footer.liquid` - Footer section
- `assets/base.css` - Main stylesheet

### Settings
- `config/settings_schema.json` - Theme settings structure
- `config/settings_data.json` - Default settings values
- `locales/en.default.json` - English translations

## 🚨 Important Notes

1. **Always test locally** before deploying
2. **Use Git** for version control
3. **Backup your theme** before major changes
4. **Follow Shopify's best practices** for performance
5. **Test on multiple devices** and browsers

## 🆘 Troubleshooting

### Common Issues
- **Authentication errors**: Run `shopify auth login` again
- **Deployment failures**: Check your store URL and permissions
- **Live reload not working**: Restart the dev server

### Getting Help
- [Shopify Theme Documentation](https://shopify.dev/themes)
- [Shopify CLI Documentation](https://shopify.dev/themes/tools/cli)
- [Dawn Theme Documentation](https://shopify.dev/themes/tools/dawn) 
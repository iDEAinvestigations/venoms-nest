# Venom's Nest Website

Static website for hosting the Venom's Nest app suite.

## Folder Structure

```
VenomsNest-Website/
├── index.html          # Main landing page
├── css/
│   └── style.css       # Styling
├── apps/               # Place APK files here
│   ├── macvenom-pro.apk
│   ├── socialpede.apk
│   ├── rfscorpion.apk
│   ├── iplizard.apk
│   ├── pcmdlive.apk
│   ├── toadcam.apk
│   ├── linkup.apk
│   └── linkup-elite.apk
└── images/             # Optional app icons/screenshots
```

## Deployment Option 1: GitHub Pages (Free)

1. Create a new GitHub repository (e.g., `venoms-nest`)
2. Upload all files from this folder to the repository
3. Go to Settings > Pages
4. Set Source to "Deploy from a branch" and select `main` branch
5. Your site will be live at: `https://yourusername.github.io/venoms-nest`

## Deployment Option 2: Subdomain on ideatech.us

1. In Namecheap, go to Domain List > ideatech.us > Advanced DNS
2. Add a CNAME record:
   - Host: `apps` (or `venomsnest`)
   - Value: `yourusername.github.io`
3. In your GitHub repo settings > Pages > Custom domain:
   - Enter: `apps.ideatech.us` (or `venomsnest.ideatech.us`)
4. Enable "Enforce HTTPS"

## Adding APK Files

1. Build your release APKs:
   ```bash
   ./gradlew assembleRelease
   ```

2. Copy APKs to the `apps/` folder with these names:
   - `macvenom-pro.apk`
   - `socialpede.apk`
   - `rfscorpion.apk`
   - `iplizard.apk`
   - `pcmdlive.apk`
   - `toadcam.apk`
   - `linkup.apk`
   - `linkup-elite.apk`

## Testing Locally

Open `index.html` in a browser, or use Python's simple server:

```bash
cd VenomsNest-Website
python3 -m http.server 8000
# Then open http://localhost:8000
```

## Customization

- Edit `index.html` to update app descriptions
- Edit `css/style.css` to change colors (look for CSS variables at top)
- Replace emoji icons with actual images in `images/` folder if desired

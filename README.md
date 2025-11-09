# CaninCasa.it - WordPress Rebuild

🐾 **La Guida Completa per Vivere con il Tuo Migliore Amico a Quattro Zampe!**

## 📋 Descrizione Progetto

Ricreazione completa del sito www.caniincasa.it su WordPress, eliminando WPBakery Page Builder e riducendo drasticamente i plugin utilizzati, mantenendo il 100% delle URL esistenti per preservare la SEO.

## 🎯 Obiettivi Principali

- ✅ **Preservazione SEO**: Mantenere tutte le URL esistenti identiche
- ⚡ **Performance**: Sito veloce, sotto 2 secondi di caricamento
- 🎯 **Snellezza**: Massimo 5-7 plugin essenziali
- 🔄 **Automazione futura**: Struttura pronta per integrazione n8n
- 📱 **Responsive**: Design mobile-first
- ♿ **Accessibilità**: WCAG 2.1 AA compliant

## 🛠️ Stack Tecnologico

- **CMS**: WordPress (ultima versione stabile)
- **Theme**: Custom theme leggero basato su best practices
- **PHP**: 8.1+
- **Database**: MySQL 8.0+
- **Editor**: Gutenberg nativo con custom blocks
- **Custom Fields**: Advanced Custom Fields (ACF) PRO

## 📁 Struttura Progetto

```
cani-in-casa/
├── wp-admin/                  # WordPress Core (gitignored)
├── wp-includes/               # WordPress Core (gitignored)
├── wp-content/
│   ├── plugins/              # Solo plugin essenziali
│   │   └── .gitkeep
│   ├── themes/
│   │   └── theme-caniincasa/ # Theme custom (tracked in git)
│   └── uploads/              # Media files
├── .gitignore
├── README.md
└── wp-config.php             # WordPress config (gitignored)
```

## 🏗️ Custom Post Types

Il sito utilizza 11 Custom Post Types:

1. **razze_di_cani** - `/razze_di_cani/{slug}/`
2. **allevamenti** - `/allevamenti/{slug}/`
3. **struttureveterinarie** - `/struttureveterinarie/{slug}/`
4. **patologie_canine** - `/patologie_canine/{slug}/`
5. **faq** - `/faq/{slug}/`
6. **annunci_dogsitter** - `/annunci_dogsitter/{slug}/`
7. **annunci_cucciolate** - `/annunci_cucciolate/{slug}/`
8. **canili** - `/canili/{slug}/`
9. **centri_cinofili** - `/centri_cinofili/{slug}/`
10. **pensioni_per_cani** - `/pensioni_per_cani/{slug}/`
11. **colore** - `/colore/{slug}/`

## 🔌 Plugin Essenziali (Max 7)

1. **Advanced Custom Fields PRO** - Gestione custom fields
2. **Yoast SEO / Rank Math** - SEO optimization
3. **WP Rocket / LiteSpeed Cache** - Caching e performance
4. **Wordfence / iThemes Security** - Security
5. **WP Mail SMTP** - Email delivery
6. **Contact Form 7 / Fluent Forms** - Forms management
7. **Redirection** (opzionale) - Gestione redirect se necessario

## 🚀 Installazione

### Requisiti

- PHP 8.1 o superiore
- MySQL 8.0 o superiore
- Apache/Nginx con mod_rewrite
- WordPress 6.4+

### Setup Locale

1. **Clona il repository**
   ```bash
   git clone <repository-url> cani-in-casa
   cd cani-in-casa
   ```

2. **Scarica WordPress Core**
   ```bash
   # Opzione 1: Download manuale
   wget https://wordpress.org/latest.zip
   unzip latest.zip
   mv wordpress/* .
   rm -rf wordpress latest.zip

   # Opzione 2: Usa WP-CLI
   wp core download --locale=it_IT
   ```

3. **Crea database**
   ```sql
   CREATE DATABASE caniincasa CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
   ```

4. **Configura WordPress**
   ```bash
   # Opzione 1: Via browser
   # Vai su http://localhost/cani-in-casa e segui il wizard

   # Opzione 2: Usa WP-CLI
   wp config create --dbname=caniincasa --dbuser=root --dbpass=password --locale=it_IT
   wp core install --url=http://localhost/cani-in-casa --title="CaninCasa.it" --admin_user=admin --admin_email=info@caniincasa.it
   ```

5. **Attiva il theme**
   ```bash
   wp theme activate theme-caniincasa
   ```

6. **Installa plugin essenziali**
   ```bash
   wp plugin install advanced-custom-fields-pro --activate
   wp plugin install wordpress-seo --activate
   # ... altri plugin
   ```

## 🎨 Theme Custom

Il theme `theme-caniincasa` è un theme custom leggero che include:

- Template personalizzati per ogni CPT
- Sistema di componenti UI riutilizzabili
- Design System con variabili CSS
- Ricerca avanzata e filtri
- Sistema recensioni
- Form di contatto e annunci
- Ottimizzazioni performance integrate

### Struttura Theme

```
theme-caniincasa/
├── functions.php
├── style.css
├── inc/
│   ├── custom-post-types.php
│   ├── taxonomies.php
│   ├── custom-fields.php
│   ├── ajax-handlers.php
│   └── template-functions.php
├── template-parts/
├── js/
└── css/
```

## 🔐 Sicurezza

- Tutti gli input sono sanitizzati
- Output escaped correttamente
- Prepared statements per database queries
- CSRF protection su tutti i form
- Rate limiting su API endpoints

## ⚡ Performance

Target metrics:
- Google PageSpeed Score: 90+
- First Contentful Paint: < 1.5s
- Time to Interactive: < 3s
- Cumulative Layout Shift: < 0.1

## 🔗 Integrazione n8n

Il sito è predisposto per automazioni via n8n con:
- REST API endpoints custom
- Webhook handlers
- Authentication via API Key
- Documentazione API completa

## 📝 SEO

- URL structure preservata al 100%
- Schema.org markup per tutti i CPT
- Sitemap XML automatica
- Meta tags ottimizzati
- Open Graph e Twitter Cards

## 🧪 Testing

```bash
# Test PHP
composer test

# Test JavaScript
npm test

# Linting
npm run lint
```

## 📚 Documentazione

- [Documentazione Tecnica](docs/technical.md)
- [Guida Utente Admin](docs/user-guide.md)
- [API Documentation](docs/api.md)

## 🤝 Contribuire

Questo è un progetto privato. Per modifiche contattare il team di sviluppo.

## 📧 Contatti

- **Email**: info@caniincasa.it
- **Progetto**: Max - Creattivo Communication

## 📄 License

Proprietario - Tutti i diritti riservati

---

**Versione**: 1.0
**Data Creazione**: 08 Novembre 2025
**Ultimo Aggiornamento**: 09 Novembre 2025

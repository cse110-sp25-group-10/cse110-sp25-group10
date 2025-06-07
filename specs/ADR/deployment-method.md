# ADR  
**Deployment Platform: Netlify vs GitHub Pages**  
**Date: 6/5/2025**

## Context / Problem  
We need to choose a deployment platform for our flashcard web application that supports fast updates, continuous deployment, and integration with our development workflow. The decision needs to balance ease of use, performance, custom domain support, and CI/CD capabilities.

## Options Considered  
- GitHub Pages  
- Netlify  

## Decision & Outcome  
We will **deploy the application using Netlify** as the primary hosting platform.

## Pros & Cons  

### Netlify

#### Pros  
- Simple drag-and-drop or Git-based continuous deployment  
- Built-in CI/CD pipeline with preview builds for pull requests  
- Free HTTPS, custom domain support, and form handling  
- Faster deployment times with atomic builds and smart caching  
- Better suited for SPAs (supports history fallback out-of-the-box)

#### Cons  
- Slightly more complexity than GitHub Pages for beginners  
- Free tier includes monthly bandwidth limits

### GitHub Pages

#### Pros  
- Built directly into GitHub, minimal setup required  
- Completely free with generous usage limits  
- Great for static sites with no custom server needs

#### Cons  
- Limited build configuration and lacks first-party CI/CD  
- No native support for SPA routing (requires manual workaround)  
- Slower update propagation and fewer deployment customization options  

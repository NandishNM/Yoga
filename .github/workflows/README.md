# Darpana Yoga — Static Website

A responsive, one-page website for Darpana Yoga, created from the supplied flyer.

## Local preview

Open `index.html` in Chrome or Edge; everything works without a server. For an optional local server, run `python -m http.server 8000` in this folder and visit http://localhost:8000/.

## Deploy to Azure Static Web Apps

1. Create a new GitHub repository (e.g. `darpana-yoga`) and upload these files to the repository root. Ensure `index.html` is at the repository root, NOT inside an extra folder.
2. In the Azure portal, search for **Static Web Apps** and select **Create**.
3. Choose an appropriate eligible Azure subscription, a resource group, and name `darpana-yoga` (or similar). Select the **Free** plan if suitable for evaluation/personal use; see production note below.
4. Source = **GitHub**. Authorize GitHub and select your repository and `main` branch.
5. Build preset = **Custom**. App location = `/` . API location = leave blank. Output location = leave blank.
6. Create the Static Web App, monitor GitHub **Actions** for the deployment, and open the URL shown in Azure's **Overview** page.
7. To update prices/classes, edit `index.html`, commit and push to `main`; the site redeploys automatically.
8. Optionally purchase a domain from a registrar. In Azure Static Web Apps choose **Custom domains > Add** and follow the DNS verification instructions. The SSL certificate is managed automatically.

### Important use/licensing notes
- Azure Static Web Apps **Free** is designated by Microsoft for hobby/personal projects and does not include an SLA. Standard is marketed for general-purpose production use. Check suitability for the business website before publishing.
- Azure Visual Studio/MSDN subscriber credits are for **dev/test only**, not production use. Deploy a live business website on a suitable eligible subscription, rather than the MSDN credit subscription.
- This website publishes the exact studio street address given in the flyer. Confirm that you intend to share the address publicly.

### Editing
- Brand colours are CSS variables at the top of `index.html`.
- Phone: search for `0422 284 121` or `+61422284121` in the HTML.
- Email: search for `darpana.yoga26@gmail.com`.
- Timetable: search for `id="timetable"`; Fees: `id="fees"`.
- Footer flyer image: `assets/class-flyer.webp`.
- No paid libraries, JavaScript frameworks, cookies, tracking, server, database or payment integration.

Microsoft documentation:
https://learn.microsoft.com/en-us/azure/static-web-apps/get-started-portal
https://azure.microsoft.com/en-au/pricing/details/app-service/static/
https://learn.microsoft.com/en-us/visualstudio/subscriptions/faq/subscriber/azure

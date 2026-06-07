# Git Integration
https://github.com/LTCharlton/linser22-digital-space/tree/master
- All live website files must reside within the **public/** folder
	- This isolates your content from system files
		- prevents "Bad Request" errors
- `.github/workflows/deploy.yml` script tells GitHub to look specifically at the public/ directory
- Secure **GitHub Secret** named `NEOCITIES_API_TOKEN`
	- key acts as the password between GitHub and Neocities
- `cleanup: true` - means your live Neocities site is an exact mirror of your local public/ folder
- lg2 engine in a-Shell does not support the -A (all) flag, use this exact sequence to publish updates:
   1. `cd public`
   2. `git add .` - This stages every new image, post, or edit inside the folder
   3. `cd ..` - back to the root directory
   4. `git commit -m "Write a brief description of your changes here"`
   5. `git push origin refs/heads/master`
> If your site doesn't update, the first thing to check is the **Actions** tab in your GitHub repository


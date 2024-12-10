# DITA-OT publishing with GitHub Actions

Template site for publishing Bootstrap-themed HTML and PDF using the DITA Open Toolkit with GitHub Actions.

## Instructions for ENGL 4814 students

1. Click on the "Use this template" green button on the top of this page
2. You need to create a repository based on the template. **Be sure to select the "Include all branches" option. We need all branches of the repository.**
3. Create your new repository based on the template.

### Next steps and requirements
- Now, the Actions will automatically publish a Bootstrap-themed HTML and a PDF using the DITA Open Toolkit
- You must have a file named `index.dita` inside the `dita` folder
- You must name your main DITA map `document.ditamap`
  - Of course, you can rename them, but that also requires renaming them inside the workflow file (and you don't want to do that... do you?)
- Customize your header file to replace banner title and icon
- Change your theme for PDF and HTML styles.

###  Ensure GITHUB_TOKEN Has Sufficient Permissions
- Navigate to Settings → Actions → General in your repository
- Under Workflow permissions, ensure that Read and write permissions is selected. This gives the GITHUB_TOKEN the necessary permission to push to the gh-pages branch.

---
## A bit more how-to information

### Create Your Content in the "dita" Folder

All of your DITA files (topics, maps, images, and other resources) should be placed inside the `dita` folder located within the repository.

### Trigger the GitHub Action for Publishing

Once you have committed your changes (via GitHub or via Oxygen Content Fusion), the GitHub Action for publishing will automatically trigger and will run in the background.

The GitHub Action workflow is pre-configured to start every time you commit changes to the repository.
It is defined in the `.github/workflows/ci.yml` file (CI stands for continuous integration), which runs the DITA Open Toolkit to process your DITA content and generate the output files (e.g., HTML, PDF).

### View the Workflow Progress

To check if the publishing process is successful, you can go to the "Actions" tab at the top of your repository page.

You’ll see a list of workflows. Look for the most recent one triggered by your commit.

A green checkmark indicates success, while a red X means the workflow failed. If it fails, click on the job to see the logs and investigate any potential issues (such as broken links in your DITA map or syntax errors).

### Access the Published Output

If the workflow completes successfully, the output files (such as HTML or PDF) will be placed in the designated out directory or another specified folder, depending on your workflow configuration.

You can find and download these files from the repository directly or view them through the GitHub Pages side of your repository.


## Credits

Thanks to the following DITA-OT experts:
- Jason Fox
- Roger Sheen.

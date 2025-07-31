# Procedure Checklist - Content Management System

This project includes a GitHub-integrated content management system that allows authorized users to edit procedure content directly from the web interface.

## Features

- 📝 **Web-based Editor**: Edit HTML content directly in the browser
- 🔐 **GitHub Authentication**: Secure access using GitHub Personal Access Tokens
- 🔄 **Auto-deployment**: Changes automatically deploy via Netlify
- 👁️ **Live Preview**: See changes before saving
- 📱 **Responsive Design**: Works on desktop and mobile devices

## Setup Instructions

### 1. GitHub Personal Access Token

1. Go to [GitHub Settings > Tokens](https://github.com/settings/tokens)
2. Click "Generate new token (classic)"
3. Give it a descriptive name (e.g., "Procedure Checklist Editor")
4. Select the following scopes:
   - `repo` (Full control of private repositories)
   - `workflow` (Update GitHub Action workflows)
5. Click "Generate token"
6. **Copy the token** - you won't be able to see it again!

### 2. Repository Setup

Make sure your repository is connected to Netlify for auto-deployment:

1. Push your code to GitHub
2. Connect your repository to Netlify
3. Configure build settings:
   - Build command: (leave empty for static sites)
   - Publish directory: `/` (or your site root)
4. Enable auto-deployment

### 3. Using the Editor

1. **Access the Editor**:
   - Click the "📝 Editor" button in the top-right corner
   - Enter your GitHub credentials:
     - **GitHub Username**: Your GitHub username
     - **Personal Access Token**: The token you created in step 1
     - **Repository Name**: `username/repository-name` (e.g., `yourname/procedure-checklist`)

2. **Edit Content**:
   - Select a file from the dropdown menu
   - Make changes in the editor panel
   - Use the "👁️ Preview" button to see changes
   - Click "💾 Save Changes" to commit to GitHub

3. **Auto-deployment**:
   - Changes are automatically committed to your GitHub repository
   - Netlify detects the changes and deploys the updated site
   - All users will see the updated content within a few minutes

## Security Notes

- **Keep your token secure**: Never share your Personal Access Token
- **Repository permissions**: Only users with repository access can edit content
- **Token expiration**: Consider setting an expiration date for your token
- **Scope limitation**: The token only has access to the specific repository

## Troubleshooting

### Authentication Issues
- Verify your GitHub username is correct
- Ensure your Personal Access Token is valid and has the correct permissions
- Check that the repository name format is correct (`username/repo-name`)

### File Loading Issues
- Make sure the file exists in your repository
- Verify the file has a `.html` extension
- Check that your token has read access to the repository

### Save Issues
- Ensure your token has write access to the repository
- Check that the file hasn't been modified by someone else (conflict)
- Verify your internet connection

### Netlify Deployment Issues
- Check your Netlify build logs
- Ensure your repository is properly connected to Netlify
- Verify build settings are correct

## File Structure

```
procedure-checklist/
├── index.html              # Main page with editor
├── talking-points.html     # Procedure content
├── bankruptcy.html         # Procedure content
├── cease-and-desist.html   # Procedure content
├── style.css              # Styles
├── script.js              # Search functionality
└── README.md              # This file
```

## Browser Compatibility

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Support

If you encounter issues:
1. Check the browser console for error messages
2. Verify your GitHub token permissions
3. Ensure your repository is properly connected to Netlify
4. Check that all files are committed to your repository

## Future Enhancements

Potential improvements for the CMS:
- Rich text editor (WYSIWYG)
- Image upload functionality
- Version history and rollback
- User management and permissions
- Content templates
- Bulk editing capabilities 
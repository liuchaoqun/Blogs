# My Blog

A simple, elegant blog powered by Jekyll and hosted on GitHub Pages.

## Features

- Clean, responsive design
- Markdown-based blog posts
- Syntax highlighting for code blocks
- Tag support
- SEO optimized
- RSS feed support

## Directory Structure

```
.
├── _config.yml          # Jekyll configuration
├── _layouts/            # Page layouts
│   ├── default.html     # Base layout
│   ├── home.html        # Homepage layout (lists posts)
│   └── post.html        # Blog post layout
├── _posts/              # Blog posts go here
│   └── YYYY-MM-DD-title.md
├── _includes/           # Reusable components (empty for now)
├── assets/              # Static assets
│   ├── css/
│   │   └── style.css    # Main stylesheet
│   └── images/          # Images for blog posts
├── index.md             # Homepage
├── about.md             # About page
└── Gemfile              # Ruby dependencies
```

## Getting Started

### Prerequisites

- Ruby (version 2.5.0 or higher)
- Bundler gem

### Local Development

1. **Install dependencies:**
   ```bash
   bundle install
   ```

2. **Run the local server:**
   ```bash
   bundle exec jekyll serve
   ```

3. **View your site:**
   Open your browser and navigate to `http://localhost:4000`

### Writing a New Blog Post

1. Create a new file in the `_posts` directory following this naming convention:
   ```
   YYYY-MM-DD-title-of-your-post.md
   ```

2. Add front matter at the top of your file:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: 2026-01-21 12:00:00 +0000
   author: Your Name
   tags: [tag1, tag2, tag3]
   ---
   ```

3. Write your content below the front matter using Markdown.

4. Save the file and it will automatically appear on your blog!

### Example Blog Post

See the example posts in `_posts/` for reference:
- `2026-01-21-welcome-to-my-blog.md`
- `2026-01-15-getting-started-with-markdown.md`

## Publishing to GitHub Pages

1. **Update `_config.yml`** with your repository information:
   ```yaml
   title: Your Blog Title
   author: Your Name
   email: your.email@example.com
   url: "https://yourusername.github.io"
   baseurl: "/repository-name"
   ```

2. **Push your changes to GitHub:**
   ```bash
   git add .
   git commit -m "Set up Jekyll blog"
   git push origin main
   ```

3. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click on "Settings"
   - Navigate to "Pages" in the left sidebar
   - Under "Source", select the branch you want to deploy (usually `main`)
   - Click "Save"

4. **Access your blog:**
   Your site will be available at `https://yourusername.github.io/repository-name`

## Customization

### Changing the Theme

Edit `_config.yml` and update the `theme` setting or add a custom theme.

### Modifying Styles

Edit `assets/css/style.css` to customize the appearance of your blog.

### Adding New Pages

Create new `.md` files in the root directory with the appropriate front matter.

### Adding Images

1. Place images in `assets/images/`
2. Reference them in your posts:
   ```markdown
   ![Alt text]({{ '/assets/images/your-image.jpg' | relative_url }})
   ```

## Tips for Writing

- Use descriptive titles
- Add relevant tags to help organize your content
- Break up long posts with headings (## and ###)
- Include code blocks with syntax highlighting
- Add images to make posts more engaging
- Keep paragraphs concise and readable

## Troubleshooting

### Site not updating?
- Clear your browser cache
- Wait a few minutes for GitHub Pages to rebuild
- Check the Actions tab in your GitHub repository for build errors

### Local server issues?
- Make sure all dependencies are installed: `bundle install`
- Try running: `bundle exec jekyll clean` then `bundle exec jekyll serve`

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)
- [Liquid Template Language](https://shopify.github.io/liquid/)

## License

This project is open source and available under the MIT License.
# Searchable Cookbook Interface

This directory contains a searchable interface for the Amazon Bedrock Cookbook.

## Files

- **`cookbook-search.html`** - Interactive search interface (open directly in browser)
- **`cookbook-recipes.json`** - Recipe database in JSON format (for programmatic access)
- **`COOKBOOK.md`** - Markdown version with all recipes organized by category

## Usage

### Option 1: Local HTML File (Recommended)

Simply open `cookbook-search.html` in your web browser:

```bash
# macOS
open cookbook-search.html

# Linux
xdg-open cookbook-search.html

# Windows
start cookbook-search.html
```

No server required! The search works entirely client-side.

### Option 2: GitHub Pages

If this repository is hosted on GitHub, you can enable GitHub Pages to make the search interface available online:

1. Go to repository Settings → Pages
2. Select source: Deploy from a branch
3. Select branch: `main` and folder: `/ (root)`
4. Access at: `https://[username].github.io/[repo-name]/cookbook-search.html`

### Option 3: Local Web Server

For development or testing:

```bash
# Python 3
python -m http.server 8000

# Node.js (with http-server)
npx http-server

# Then open: http://localhost:8000/cookbook-search.html
```

## Features

### 🔍 Free Text Search
- Search across recipe titles, descriptions, categories, and tags
- Real-time filtering as you type
- Case-insensitive matching

### 🏷️ Category Filters
- Quickstarts
- Agents
- RAG
- Multimodal
- Custom Models
- Use Cases
- Evaluation
- Observability
- Responsible AI
- Production
- Advanced

### 📊 Difficulty Filters
- 🟢 Beginner - Getting started recipes
- 🟡 Intermediate - Standard implementations
- 🔴 Advanced - Complex patterns and optimizations

### 📈 Live Stats
- Shows count of filtered recipes
- Total recipe count

### 🎨 Responsive Design
- Works on desktop, tablet, and mobile
- Clean, modern interface
- AWS-themed colors

## Search Examples

Try these search queries:

- **"RAG"** - Find all RAG-related recipes
- **"Claude"** - Recipes using Claude models
- **"agents"** - All agent-related content
- **"fine-tuning"** - Model customization recipes
- **"cost"** - Cost optimization techniques
- **"security"** - Security and compliance recipes
- **"langchain"** - LangChain integration examples
- **"sql"** - Database query recipes
- **"vision"** - Image and video processing

## Adding New Recipes

### Method 1: Edit HTML File

Open `cookbook-search.html` and add to the `recipes` array:

```javascript
{
    title: "Your Recipe Title",
    description: "Brief description of what this recipe does",
    category: "Category Name",
    tags: ["tag1", "tag2", "tag3"],
    difficulty: "beginner|intermediate|advanced",
    link: "./path/to/recipe/"
}
```

### Method 2: Edit JSON File

Add to `cookbook-recipes.json`:

```json
{
    "id": "unique-recipe-id",
    "title": "Your Recipe Title",
    "description": "Brief description",
    "category": "Category Name",
    "tags": ["tag1", "tag2"],
    "difficulty": "beginner",
    "link": "./path/to/recipe/",
    "keywords": ["additional", "search", "terms"]
}
```

## Customization

### Change Colors

Edit the CSS in `cookbook-search.html`:

```css
.header {
    background: linear-gradient(135deg, #232F3E 0%, #FF9900 100%);
}

.filter-btn.active {
    background: #FF9900; /* AWS Orange */
}
```

### Add More Filters

Add new filter types in the `renderFilters()` function:

```javascript
// Example: Add model filter
const modelHTML = ['claude', 'titan', 'llama'].map(model => 
    `<button class="filter-btn" data-type="model" data-value="${model}">
        ${model}
    </button>`
).join('');
```

### Modify Card Layout

Edit the `renderRecipes()` function to change card appearance:

```javascript
grid.innerHTML = recipesToRender.map(recipe => `
    <div class="recipe-card">
        <!-- Your custom card HTML -->
    </div>
`).join('');
```

## Browser Compatibility

Works in all modern browsers:
- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Opera 76+

No external dependencies required!

## Performance

- **Load Time:** < 100ms (all client-side)
- **Search Speed:** Instant (< 10ms for 100+ recipes)
- **File Size:** ~15KB HTML + CSS + JS

## Accessibility

- Keyboard navigation supported
- ARIA labels for screen readers
- High contrast colors
- Responsive text sizing

## Future Enhancements

Potential improvements:

- [ ] Add sorting (alphabetical, newest, most popular)
- [ ] Bookmark/favorite recipes
- [ ] Export filtered results
- [ ] Dark mode toggle
- [ ] Recipe ratings/feedback
- [ ] Related recipes suggestions
- [ ] Advanced search operators (AND, OR, NOT)
- [ ] Search history
- [ ] URL-based filtering (shareable links)

## Troubleshooting

### Search not working
- Ensure JavaScript is enabled in your browser
- Check browser console for errors (F12)

### Recipes not displaying
- Verify the `recipes` array in the HTML file
- Check that all recipe objects have required fields

### Links not working
- Ensure relative paths are correct
- Check that target folders exist in repository

## Contributing

To add recipes or improve the search interface:

1. Fork the repository
2. Add your recipes to `cookbook-search.html`
3. Test locally
4. Submit a pull request

## License

MIT-0 License - See [LICENSE](./LICENSE) file.

---

**Questions?** Open an issue on GitHub or check the main [COOKBOOK.md](./COOKBOOK.md) for more information.

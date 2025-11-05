# Markdown Tips and Tricks

## Can I have a textbox with rounded corners in Markdown?

**Short answer:** Yes, but it depends on your markdown renderer.

### 🔍 How to View This Guide

**Important:** To see the textboxes with rounded corners in this document:

1. **On GitHub:** Make sure you're viewing the **rendered** markdown (the default view when you click on the file)
   - ✅ Correct: Click on `markdown-tips.md` in the file list
   - ❌ Wrong: Don't click "Raw" or "Code" view
   
2. **The examples below will show:**
   - Code blocks (for you to copy)
   - Live rendered examples (showing how they look)

If boxes aren't rendering, you're likely viewing the raw markdown source instead of the rendered HTML.

### ✅ Quick Test - Can You See These Boxes?

If you're viewing this correctly, you should see colored boxes below:

> [!NOTE]
> **Test Box 1:** If you can see this in a blue box with rounded corners, GitHub alerts are working! ✅

<div style="border: 2px solid #4CAF50; border-radius: 10px; padding: 15px; background-color: #f0f0f0; margin: 10px 0;">
  <strong>Test Box 2:</strong> If you can see this in a green box with rounded corners, HTML+CSS is working! ✅
</div>

**What you should see:**
- Test Box 1: Blue box with a lightbulb icon
- Test Box 2: Green box with a light gray background

**If you DON'T see styled boxes above**, you're viewing the raw markdown. Go back and click on the filename to view the rendered version.

---

Standard markdown doesn't support styled textboxes with rounded corners directly, but there are several approaches you can use:

### Method 1: HTML with Inline CSS (Most Control)

If your markdown renderer supports HTML (like GitHub, GitLab, most static site generators), you can use HTML with inline CSS:

```html
<div style="border: 2px solid #4CAF50; border-radius: 10px; padding: 15px; background-color: #f0f0f0;">
  <strong>Important Note:</strong> This is a textbox with rounded corners!
  You can include <em>any HTML content</em> here.
</div>
```

**Rendered example:**

<div style="border: 2px solid #4CAF50; border-radius: 10px; padding: 15px; background-color: #f0f0f0;">
  <strong>Important Note:</strong> This is a textbox with rounded corners!
  You can include <em>any HTML content</em> here.
</div>

### Method 2: GitHub-Flavored Markdown Alerts (GitHub Only)

GitHub supports special alert syntax that creates styled boxes:

```markdown
> [!NOTE]
> This creates a blue info box with rounded corners.

> [!TIP]
> This creates a green tip box with rounded corners.

> [!IMPORTANT]
> This creates a purple important box with rounded corners.

> [!WARNING]
> This creates a yellow warning box with rounded corners.

> [!CAUTION]
> This creates a red caution box with rounded corners.
```

**Rendered examples:**

> [!NOTE]
> This creates a blue info box with rounded corners.

> [!TIP]
> This creates a green tip box with rounded corners.

> [!IMPORTANT]
> This creates a purple important box with rounded corners.

> [!WARNING]
> This creates a yellow warning box with rounded corners.

> [!CAUTION]
> This creates a red caution box with rounded corners.

### Method 3: Simple Blockquotes (Basic Styling)

For a simpler approach that works everywhere, use blockquotes:

```markdown
> **Note:** This is a simple blockquote that looks like a box.
> It doesn't have rounded corners by default, but some renderers style it nicely.
```

**Rendered example:**

> **Note:** This is a simple blockquote that looks like a box.
> It doesn't have rounded corners by default, but some renderers style it nicely.

### Method 4: Code Blocks (No Rounded Corners, but Box-like)

For a box-like appearance without styling, use code blocks with ASCII art:

````markdown
```text
┌─────────────────────────────┐
│ This is a text box using    │
│ ASCII art box-drawing       │
│ characters                  │
└─────────────────────────────┘
```
````

**Rendered example:**

```text
┌─────────────────────────────┐
│ This is a text box using    │
│ ASCII art box-drawing       │
│ characters                  │
└─────────────────────────────┘
```

### Method 5: Custom CSS (For Your Own Site)

If you control the website/rendering, add custom CSS:

```css
.rounded-box {
  border: 2px solid #2196F3;
  border-radius: 15px;
  padding: 20px;
  margin: 10px 0;
  background-color: #E3F2FD;
}
```

Then in your markdown:

```html
<div class="rounded-box">
  This uses a custom CSS class for consistent styling across your site.
</div>
```

## Which Method Should You Use?

- **GitHub/GitLab README**: Use Method 1 (HTML+CSS) or Method 2 (GitHub Alerts)
- **Documentation site (MkDocs, Jekyll, etc.)**: Use Method 1 or Method 5
- **Maximum compatibility**: Use Method 3 (Blockquotes)
- **Plain text appearance**: Use Method 4 (Code blocks with ASCII)

## Examples for This Repository

Since this is a GitHub repository, here are some practical examples. Each example uses inline CSS for easy copy-pasting - customize the colors and styling to suit your needs:

### Example 1: Key Concept Box

<div style="border: 2px solid #2196F3; border-radius: 10px; padding: 15px; background-color: #E3F2FD; margin: 10px 0;">
  <strong>🔑 Key Concept:</strong> Serial transmission sends data one bit at a time over a single channel, while parallel transmission sends multiple bits simultaneously over multiple channels.
</div>

### Example 2: Warning Box

> [!WARNING]
> Make sure you understand the difference between baud rate and bit rate before the exam!

### Example 3: Tip Box

> [!TIP]
> Use mnemonics to remember the OSI model layers: "Please Do Not Throw Sausage Pizza Away"

### Example 4: Important Note Box

<div style="border: 2px solid #FF9800; border-radius: 10px; padding: 15px; background-color: #FFF3E0; margin: 10px 0;">
  <strong>⚠️ Important:</strong> CSMA/CA is used in WiFi networks to avoid collisions, unlike CSMA/CD used in wired Ethernet.
</div>

## Summary

Yes, you can create textboxes with rounded corners in markdown! The best method depends on where your markdown will be rendered. For GitHub repositories, use HTML with inline CSS or GitHub alert syntax for the best results.

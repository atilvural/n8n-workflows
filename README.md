## Micro SaaS Idea Generator (n8n Workflow)
Simple n8n workflow to fetch Reddit posts, generate or improve micro-SaaS ideas using AI, and store them in MySQL.

### Database Setup
```
CREATE TABLE reddit_post (
  url VARCHAR(1000) CHARSET utf8mb3 NOT NULL PRIMARY KEY,
  author VARCHAR(150) CHARSET utf8mb3 NULL,
  title TEXT NULL,
  post TEXT NULL,
  ups INT NULL,
  downs INT NULL,
  processed BIT DEFAULT b'0' NULL
);

CREATE TABLE saas_ideas (
  id INT AUTO_INCREMENT PRIMARY KEY,
  category VARCHAR(255) CHARSET utf8mb3 NULL,
  description TEXT NULL,
  leads VARCHAR(2000) CHARSET utf8mb3 NULL COMMENT 'Comma separated usernames',
  posts TEXT NULL COMMENT 'Comma separated post urls'
);
```
### How It Works
- Fetches top posts from /r/SaaS, /r/startups, /r/sidehustle, /r/SideProject.
- Saves posts into reddit_post table if not already inserted.
- Selects unprocessed posts and loads existing SaaS ideas.
- AI analyzes posts and generates or updates micro-SaaS ideas.
- Ideas are saved into saas_ideas table.
- Marks processed posts.

### Requirements
- MySQL database access.
- Google Gemini API key (for AI analysis).


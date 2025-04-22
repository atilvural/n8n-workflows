# Micro SaaS Idea Generator Repository

This repository contains workflows and tools built with [n8n](https://n8n.io/) to automate the process of generating, managing, and sharing micro-SaaS ideas. It integrates with Reddit, AI tools, MySQL, Discord, and Gmail to streamline the entire workflow from idea collection to approval and distribution.

## Repository Structure

### 1. [saas-ideas](./saas-ideas)
This folder contains workflows and resources for collecting, generating, and managing micro-SaaS ideas.

- **Workflows**:
  - **Idea Collector**: Fetches Reddit posts and generates SaaS ideas using AI.
  - **Idea Report Generator**: Groups and merges related ideas into comprehensive reports.
  - **Idea Approver**: Sends Discord messages for idea approval or removal.

- **Database Setup**:
  - Includes SQL scripts to create the `reddit_post` and `saas_ideas` tables.

- **Key Features**:
  - Fetches posts from subreddits like `/r/SaaS`, `/r/startups`, `/r/sidehustle`, and `/r/SideProject`.
  - Uses AI to analyze posts and generate or improve SaaS ideas.
  - Sends Discord notifications for idea approval.

For more details, see the [saas-ideas README](./saas-ideas/README.md).

---

### 2. [newsletter](./newsletter)
This folder contains workflows for sending email newsletters with the latest SaaS ideas to subscribed users.

- **Workflows**:
  - **Newsletter Send Email**: Sends newsletters to subscribers with approved SaaS ideas.

- **Database Setup**:
  - Includes SQL scripts to create the `newsletter` table.

- **Key Features**:
  - Sends HTML-based newsletters to subscribers.
  - Integrates with Gmail for email delivery.

For more details, see the [newsletter README](./newsletter/README.md).

---

## Summary of What This Repository Does

This repository automates the process of discovering, refining, and sharing micro-SaaS ideas. It works as follows:
1. **Idea Collection**: Fetches posts from Reddit and stores them in a MySQL database.
2. **Idea Generation**: Uses AI to analyze posts and generate SaaS ideas.
3. **Idea Approval**: Sends ideas to Discord for approval or removal.
4. **Newsletter Distribution**: Sends approved ideas to subscribers via email.

## Requirements
- **n8n**: To run the workflows.
- **MySQL**: For storing Reddit posts, SaaS ideas, and newsletter subscriptions.
- **API Keys**:
  - Google Gemini (for AI analysis).
  - Discord Bot (for idea approval).
  - Gmail (for sending newsletters).

## Getting Started
1. Clone this repository:
   ```bash
   git clone https://github.com/atilvural/n8n-workspace.git
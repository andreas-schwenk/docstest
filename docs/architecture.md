---
title: Architecture
---

LibreQ currently consists of the following main components:

- **Frontend**  
  Public web interface for browsing and viewing questions

- **API**  
  Backend scripts for metadata, indexing, and internal data access

- **MariaDB**  
  Storage for question metadata, topic trees, and related project data

- **Moodle**  
  Authoring and rendering environment, including support for STACK questions

- **Preview Renderer**  
  Automated screenshot generation using Node.js and Puppeteer

## Architecture

```text
                    +--------------------+
                    |     Frontend       |
                    |   public website   |
                    +--------------------+
                              |
                              v
                    +--------------------+
                    |        API         |
                    |   project backend  |
                    +--------------------+
                              |
                              v
                    +--------------------+
                    |      MariaDB       |
                    |   project storage  |
                    +--------------------+

                    +--------------------+
                    |      Moodle        |
                    | question authoring |
                    |   and rendering    |
                    +--------------------+
                              |
                              v
                    +--------------------+
                    | Preview Renderer   |
                    | Node.js/Puppeteer  |
                    +--------------------+
```

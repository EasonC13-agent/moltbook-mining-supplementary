# Supplementary Materials: Mining Peer Learning on Moltbook

Supplementary materials for the paper "When OpenClaw AI Agents Teach Each Other: Peer Learning Patterns in the Moltbook Community" (EDM 2026).

## Contents

### `data/` - Dataset

| File | Size | Description |
|------|------|-------------|
| `moltbook_posts.csv` | 47MB | All posts in CSV format (68,228 posts) |
| `moltbook.db` | 65MB | SQLite database with same data |
| `aggregate_statistics.csv` | 378B | Summary statistics by category |
| `submolt_statistics.csv` | 675B | Per-community statistics |

#### Posts Schema

| Column | Type | Description |
|--------|------|-------------|
| `id` | TEXT | Unique post identifier (UUID) |
| `title` | TEXT | Post title |
| `body` | TEXT | Post content |
| `author_id` | TEXT | Author's unique identifier |
| `author_name` | TEXT | Author's display name |
| `submolt` | TEXT | Community name (e.g., "general", "ai", "philosophy") |
| `upvotes` | INTEGER | Number of upvotes |
| `downvotes` | INTEGER | Number of downvotes |
| `comment_count` | INTEGER | Number of comments |
| `created_at` | TIMESTAMP | Post creation time (ISO 8601) |
| `fetched_at` | TIMESTAMP | Data collection time |
| `is_question` | BOOLEAN | Whether post is a question (0/1) |
| `knowledge_type` | TEXT | "procedural", "conceptual", or "other" |
| `body_length` | INTEGER | Character count of body |

#### Usage Examples

**Python (pandas):**
```python
import pandas as pd
df = pd.read_csv('data/moltbook_posts.csv')
print(df.groupby('submolt').size().sort_values(ascending=False).head(10))
```

**SQLite:**
```bash
sqlite3 data/moltbook.db "SELECT submolt, COUNT(*) as cnt FROM posts GROUP BY submolt ORDER BY cnt DESC LIMIT 10"
```

### `classification/` - Coding Schemes

| File | Description |
|------|-------------|
| `knowledge_type.md` | Procedural vs. Conceptual classification criteria |
| `discourse_type.md` | Questions vs. Statements classification |
| `spam_filtering.md` | Spam detection methodology |
| `comment_taxonomy.md` | Comment pattern coding scheme (5 categories) |

### `scripts/` - Analysis Code

Processing scripts used for data analysis (Python).

## Data Collection

| Metric | Value |
|--------|-------|
| Collection period | January 28 - February 9, 2026 |
| Raw posts collected | 68,228 |
| After quality filtering | 28,683 |
| Platform total posts | 775,620 |
| Platform total comments | 12,123,362 |
| Registered agents | ~2.45 million |

## Data Source

All posts are publicly available on [Moltbook](https://moltbook.com), a social learning platform for AI agents built on OpenClaw. Posts were collected via the public API.

## Citation

```bibtex
@inproceedings{chen2026moltbook,
  title={When OpenClaw AI Agents Teach Each Other: Peer Learning Patterns in the Moltbook Community},
  author={Chen, Eason and others},
  booktitle={Proceedings of the 19th International Conference on Educational Data Mining},
  year={2026}
}
```

## License

MIT License

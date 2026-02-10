# Supplementary Materials: Mining Peer Learning on Moltbook

Supplementary materials for the paper "When OpenClaw AI Agents Teach Each Other: Peer Learning Patterns in the Moltbook Community" (EDM 2026).

## Contents

- `classification/` - Classification criteria and methods
  - `knowledge_type.md` - Procedural vs. Conceptual classification
  - `discourse_type.md` - Questions vs. Statements classification
  - `spam_filtering.md` - Spam detection and filtering methodology
  - `comment_taxonomy.md` - Comment pattern coding scheme

- `scripts/` - Data processing scripts
  - `classify_posts.py` - Post classification implementation
  - `filter_spam.py` - Spam filtering implementation
  - `compute_statistics.py` - Statistical analysis code

- `data/` - Anonymized aggregate statistics (no raw text)
  - `aggregate_statistics.csv` - Summary statistics by category
  - `submolt_statistics.csv` - Per-community statistics

## Data Collection Period

- **Start:** January 28, 2026
- **End:** February 9, 2026
- **Raw posts collected:** 68,228
- **After spam filtering:** 28,683
- **Platform scale:** 775,620 posts, 12,123,362 comments, 2.45M agents

## Privacy Notice

This repository contains only:
- Classification criteria and methodology
- Processing scripts
- Aggregate statistics

**No individual posts, comments, or identifiable information is included.**

## Citation

```bibtex
@inproceedings{anonymous2026moltbook,
  title={When OpenClaw AI Agents Teach Each Other: Peer Learning Patterns in the Moltbook Community},
  author={Anonymous},
  booktitle={Proceedings of the 19th International Conference on Educational Data Mining},
  year={2026}
}
```

## License

MIT License

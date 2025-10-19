# Fact-Checker Skill for Claude

A comprehensive fact-checking and verification skill that enables Claude to analyze text, articles, and web content for factual accuracy using academic and journalistic approaches.

## Overview

This skill equips Claude with a fact-checker that extracts verifiable claims, cross-references them against trusted sources, and provides detailed credibility assessments with supporting evidence.

## What It Does

1. **Claim Extraction** - Identifies all verifiable factual statements in provided content
2. **Source Research** - Systematically searches trusted academic, government, and journalistic sources
3. **Credibility Assessment** - Rates each claim as TRUE/FALSE/PARTIALLY TRUE/UNVERIFIED with confidence levels
4. **Source Quality Rating** - Calculates credibility scores using weighted criteria (source type, methodology, recency, corroboration)
5. **Report Generation** - Compiles comprehensive findings with evidence, contradictions, and context

## Verification Framework

**Status Categories:**
- TRUE (with HIGH/MEDIUM/LOW confidence)
- FALSE (demonstrably incorrect)
- PARTIALLY TRUE (accurate but missing context)
- UNVERIFIED (insufficient evidence)
- OPINION/SUBJECTIVE (not fact-checkable)

**Credibility Scoring Formula:**
```
Total Score = (Source Credibility × 0.40) + (Methodology × 0.30) + 
              (Recency × 0.15) + (Corroboration × 0.15)
```

## Trusted Sources Included

- **Academic:** Google Scholar, PubMed, arXiv, Semantic Scholar, IEEE Xplore, JSTOR
- **Government:** Census Bureau, CDC, FDA, EPA, WHO, World Bank, UN Statistics
- **Fact-Checkers:** Snopes, PolitiFact, FactCheck.org, Reuters Fact Check, AP Fact Check
- **News:** Associated Press, Reuters, BBC, NYT, Washington Post, Wall Street Journal, The Guardian
- **Domain-Specific:** Medical journals (NEJM, Lancet, JAMA), scientific journals (Nature, Science), legal databases

## Installation

1. Download `fact-checker.zip`
2. In Claude: Settings → Skills → Add skill → Upload skill
3. Select the downloaded file

## Usage Examples

```
"Fact-check this article: [paste text or URL]"
"Verify these medical claims about [treatment]"
"Check the accuracy of these statistics"
"Analyze this news article for factual accuracy"
"Is this statement true? [statement]"
```

## Output Format

Each verification report includes:

- **Executive Summary** - Overall credibility score and key findings
- **Detailed Findings** - Per-claim verification with status, confidence level, supporting/contradictory evidence, and context
- **Source Bibliography** - Complete source list with credibility scores, types, dates, strengths, and limitations
- **Recommendations** - Suggestions for further verification and identified red flags

## License

MIT License - See LICENSE file for details

## Contributing

Contributions welcome! Please feel free to submit issues or pull requests to improve source coverage, verification methodology, or domain-specific guidance.

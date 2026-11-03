# Mixed Onsite Signals Lite

A Claude skill that finds the places where your website contradicts itself and lists incorrect data. This is the fast version: it reads the 20 to 25 pages that matter most and hands you the sharpest conflicts.

## Why it's important

AI may use your website alongside other sources to answer questions about your business. If your own pages give conflicting details, you're giving them conflicting evidence. Fixing those contradictions makes your site a clearer, more reliable reference for the facts you control.

If your pricing page says $49 and your FAQ says $59, or your About page says you were founded in 2015 and your footer says 2017, ChatGPT, Claude, and Google's AI answers can't tell which one is true. So they leave you out, or they tell your customers the wrong one.

## What it checks

It starts with your sitemap and reads up to 25 pages: any llms.txt or agents.md file, your homepage, your About page, your top 5 to 8 product or service pages, your shipping, returns, warranty and pricing pages, and a handful of FAQ pages. On every page it compares the visible text against the hidden data behind it, the meta description and structured data, because that's what AI reads first.

It looks hardest for the conflicts that do the most damage: an llms.txt file that disagrees with the live site, hidden product data that disagrees with the page, a meta description copied from the wrong product, an old domain or brand name still sitting in your FAQ, and a refund promise your policy page takes back.

It adjusts to the kind of business you run. A store gets checked for prices, specs, shipping and returns. A lender gets checked for rates, fees, loan limits, credit requirements and time to funding. A software company gets checked for plan prices, what each plan includes, user limits and trial length. An agency gets checked on the services it offers and the results it claims.

It won't pick a winner on anything regulated or promised, like rates or return windows. Those come back to you as questions, because only you know which one is real. It only reads your site. It never changes anything on it.

## What you get back

A one-line summary of how many pages it read and how many conflicts it found, then the sharpest contradictions at the top, each with a link that jumps straight to the problem on the live page. After that come the questions only you can answer, the fixes that live in a template or footer, and a full table, page by page.

It skips the long lists of clean pages. One line at the end tells you how many URLs on the site it didn't get to.

## Install

### Claude.ai and the Claude desktop app

Download [mixed-onsite-signals-lite.zip](mixed-onsite-signals-lite.zip) and upload it as a skill in your Claude settings.

### Claude Code

```
git clone https://github.com/seamar/mixed-onsite-signals-lite.git
cp -r mixed-onsite-signals-lite/skills/mixed-onsite-signals-lite ~/.claude/skills/
```

Restart Claude Code and it's ready.

If you use some other AI tool, paste everything below the header in `skills/mixed-onsite-signals-lite/SKILL.md` into your project instructions or system prompt. Whatever you use has to be able to browse the web, or it can't read the site.

## Use it

Ask Claude to run a quick conflicting info audit, or call the skill by name:

```
Run Mixed Onsite Signals Lite on example.com
```

Plenty of sites block automated requests, especially ones behind Cloudflare. If Claude can't load the pages, run it with a browser tool like Claude in Chrome so it reads the site the way you would.

## License

MIT. Use it, change it, run it for your clients.

Created by Sean Markey @ [Ranks](https://ranks.com)

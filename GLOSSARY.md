# Pro Git বাংলা অনুবাদ — Glossary

**Version: v1.0 (frozen, 2026-08-07)** — দেখুন [STYLE_GUIDE.md](STYLE_GUIDE.md)-এর "স্টাইল গাইড Freeze করা" সেকশন। এই ফাইলের core টার্ম-সিদ্ধান্তগুলো এখন স্থির; নতুন টার্ম যোগ করা চলবে, কিন্তু বিদ্যমান কোনো এন্ট্রি বদলাতে হলে সত্যিকারের টেকনিক্যাল কারণ লাগবে, শুধু "আরেকটু ভালো লাগছে" যথেষ্ট না।

এই ফাইলটাই Pro Git বাংলা অনুবাদের জন্য টার্মিনোলজির single source of truth।

**Workflow — নতুন কোনো টার্ম সামনে এলে:**
1. আগে এই ফাইলে চেক করুন।
2. থাকলে, ঠিক সেভাবেই ব্যবহার করুন — নতুন করে সিদ্ধান্ত নেবেন না।
3. না থাকলে, একবার সিদ্ধান্ত নিন, এই ফাইলে যোগ করুন, তারপর অনুবাদ চালিয়ে যান।
4. পরে গিয়ে সেই সিদ্ধান্ত আবার পাল্টাবেন না।

> **আপডেট (2026-08-07):** আগে (chapter 1-3-এর প্রথম ড্রাফটে) Git-এর মূল টার্মগুলো Latin script-এ রাখা হচ্ছিল (যেমন "branch তৈরি করা")। এখন থেকে নিচের টেবিল অনুযায়ী, বেশিরভাগ core noun/verb বাংলা script-এ transliterate করা হচ্ছে (যেমন "ব্রাঞ্চ তৈরি করা")। Chapter 1-3 এই কনভেনশন অনুযায়ী retrofit করা হয়েছে।

## সিদ্ধান্তের পেছনের যুক্তি (Decision Rationale)

টার্মগুলো arbitrary না — একটা সুনির্দিষ্ট নীতি মেনে ভাগ করা হয়েছে:

* **Transliterate (বাংলা script)** — যে core noun/verb বাক্যের মধ্যে বারবার আসে, আর Bangla case-suffix (এর/এ/ও) জুড়ে natural বাংলা বাক্য গঠনে ব্যবহার করতে হয় (ব্রাঞ্চ, কমিট, মার্জ, রিপোজিটরি...)। এগুলো বাংলা script-এ থাকলে বাক্যের ছন্দ ভাঙে না।
* **English-ই থাকবে** — যেগুলো (ক) UI/CLI-তে ব্যবহারকারী ঠিক এই বানানেই দেখবেন (Git, GitHub, HEAD, Pull Request), (খ) একটা নির্দিষ্ট technical state/mechanism-এর নাম যেটা প্রায়ই backtick-এ literal ভাবে quote করা হয় (Checkout, Rebase, Cherry-pick, Fast-forward, Detached HEAD), অথবা (গ) খুব কম ব্যবহৃত internals পরিভাষা যেটা glossary-তে কভার করার দরকার পড়েনি (blob, tree)।
* **Compound/Derived টার্ম** — যখন একটা glossary টার্ম (যেমন ব্রাঞ্চ, কমিট, কনফ্লিক্ট) কোনো ইংরেজি qualifier-এর সাথে জোড়া লাগে (topic branch, tracking branch, conflict marker), তখন শুধু glossary-ভুক্ত অংশটাই transliterate হয়, qualifier অংশ ইংরেজিতেই থাকে — যেমন "topic ব্রাঞ্চ", "tracking ব্রাঞ্চ", "কনফ্লিক্ট marker"। এভাবে নতুন compound টার্ম এলেও পুরো glossary নতুন করে না লিখেই সিদ্ধান্ত নেওয়া যায়।

এই তিনটা নীতিই future contributor-দের জন্য — glossary-কে "arbitrary লিস্ট" না ভেবে, উপরের যুক্তি দিয়ে নতুন টার্মের সিদ্ধান্ত নিজেই বের করা যাবে।

## বাংলা Script-এ Transliterate করা টার্ম

এই শব্দগুলো বাক্যের মধ্যে বাংলা script-এই লিখুন — এগুলো এখন এতটাই প্রচলিত যে বাংলা বাক্যের স্বাভাবিক অংশ হিসেবেই পড়া যায়।
বাংলা case-suffix (এর, এ, ও, গুলো, ইত্যাদি) সরাসরি জুড়ে দিন, স্বাভাবিক বাংলা বানানরীতি মেনে — Latin script-এর মতো হাইফেন দরকার নেই (যেমন "কমিট-এর" না, "কমিটের")।

| English | বাংলা | ব্যবহারের ধরন |
|---|---|---|
| Repository / Repo | রিপোজিটরি | "রিপোজিটরি তৈরি করা", "লোকাল রিপোজিটরি" |
| Commit | কমিট | "কমিট করা", "একটা কমিট", "কমিটের history" |
| Branch | ব্রাঞ্চ | "ব্রাঞ্চ তৈরি করা", "master ব্রাঞ্চ" |
| Merge | মার্জ | "মার্জ করা", "মার্জ commit" |
| Clone | ক্লোন | "ক্লোন করা", "ক্লোন করার পর" |
| Push | পুশ | "পুশ করা" |
| Pull | পুল | "পুল করা" |
| Fetch | ফেচ | "ফেচ করা" — *(মূল guide-এ ছিল না; push/pull/clone-এর প্যাটার্ন মেনে সামঞ্জস্যের জন্য যোগ করা হয়েছে)* |
| Remote | রিমোট | "রিমোট যোগ করা", "রিমোট রিপোজিটরি" |
| Tag | ট্যাগ | "ট্যাগ করা", "একটা ট্যাগ" |
| Working Tree | ওয়ার্কিং ট্রি | |
| Working Directory | ওয়ার্কিং ডিরেক্টরি | *(Working Tree-এর প্যাটার্ন মেনে যোগ করা হয়েছে, একই ধারণা)* |
| Staging Area | স্টেজিং এরিয়া | |
| Stage (verb) | স্টেজ করা | *(Staging Area-এর প্যাটার্ন মেনে যোগ করা হয়েছে)* |
| Snapshot | স্ন্যাপশট | |
| History | ইতিহাস | "commit history" → "কমিট ইতিহাস" বা প্রসঙ্গভেদে "কমিটের ইতিহাস" |
| Conflict | কনফ্লিক্ট | "merge conflict" → "মার্জ কনফ্লিক্ট" |
| Resolve (verb) | সমাধান করা | Transliteration না, native বাংলা verb — "conflict resolve করা" → "কনফ্লিক্ট সমাধান করা" |
| Source Code | সোর্স কোড | |
| Directory | ডিরেক্টরি | |
| File | ফাইল | |
| Project | প্রজেক্ট | |
| Developer | ডেভেলপার | |
| Open Source | ওপেন সোর্স | |
| Version Control | Version Control (ভার্সন কন্ট্রোল) | প্রথমবার উভয় ফর্ম দিন (নিয়ম ৬ দেখুন), এরপর যেকোনো একটা ফর্ম সামঞ্জস্যপূর্ণভাবে ব্যবহার করুন |

## English/Latin Script-এই থাকবে

এই টার্মগুলো literal command/flag হিসেবে এত বেশি ব্যবহৃত হয় যে বাংলা script-এ লিখলে বরং বিভ্রান্তিকর হবে।

| Term | নোট |
|---|---|
| Git | |
| GitHub | |
| HEAD | সবসময় বড় হাতের অক্ষরে |
| Checkout | |
| Rebase | rebasing, rebased-ও ইংরেজিতেই |
| Cherry-pick | |
| Fast-forward | "একটা fast-forward মার্জ", "`master` ব্রাঞ্চ fast-forward করা" — chapter 3-এ ইতিমধ্যে এভাবেই ব্যবহৃত |
| Detached HEAD | HEAD বড় হাতের অক্ষরে, পুরো phrase-টা ইংরেজিতে — যেমন tagging.asc-তে `"`detached HEAD`" state` |
| Upstream | "upstream ব্রাঞ্চ", "upstream-এ পুশ করা" — remote-branches.asc/remotes.asc-এ ইতিমধ্যে এভাবেই ব্যবহৃত |
| Pull Request | GitHub UI-তে exact এই বানানেই দেখা যায় |
| config / alias | |
| Index (staging area-র টেকনিক্যাল নাম) | সাধারণ প্রসঙ্গে "স্টেজিং এরিয়া"-ই ব্যবহার করুন; Git-এর টেকনিক্যাল নাম হিসেবে ব্যাখ্যা করার সময়ই শুধু ইংরেজি quote-এ "`index`" ব্যবহার করুন (দেখুন what-is-git.asc) |
| blob / tree (Git internal object types) | কম ব্যবহৃত internals টার্ম, glossary-তে কভার করা হয়নি বলে English-ই থাকবে — যেমন `nutshell.asc`-এ "একটা commit আর তার _blob_/_tree_" |

## Compound/Derived টার্ম

মূল glossary টার্ম + ইংরেজি qualifier-এর combination। "সিদ্ধান্তের পেছনের যুক্তি" সেকশনের নিয়ম অনুযায়ী, শুধু glossary-ভুক্ত অংশটাই transliterate হয়।

| ইংরেজি | বাংলা রেন্ডারিং | উদাহরণ (ইতিমধ্যে বইয়ে ব্যবহৃত) |
|---|---|---|
| Tracking Branch | Tracking ব্রাঞ্চ | remote-branches.asc: `"`tracking ব্রাঞ্চ`"` |
| Remote-tracking Branch | remote-tracking ব্রাঞ্চ | remote-branches.asc |
| Topic Branch | topic ব্রাঞ্চ | workflows.asc |
| Bare Repository | Bare রিপোজিটরি | *(এখনো ব্যবহার হয়নি, এই প্যাটার্ন অনুসরণ করুন)* |
| Conflict Marker | কনফ্লিক্ট marker | basic-branching-and-merging.asc-এ "conflict-resolution marker" হিসেবে ইতিমধ্যে ব্যবহৃত |
| Merge Conflict | মার্জ কনফ্লিক্ট | |
| Merge Commit | মার্জ কমিট | |
| Commit History | কমিট ইতিহাস | |

## কখনো অনুবাদ বা Transliterate করা হবে না

- কোনো `[source, ...]` ... `----` কোড ব্লকের ভেতরের যেকোনো কিছু (কমান্ড, ফ্ল্যাগ, আউটপুট) — অক্ষরে অক্ষরে অপরিবর্তিত।
- Inline code (`` `git commit` ``, `` `README.md` `` ইত্যাদি) যা কোনো literal কমান্ড, ফাইলের নাম, পাথ, ফ্ল্যাগ, বা identifier বোঝায়।
- Branch/remote-এর নাম যেমন `master`, `main`, `origin`, `iss53`, `hotfix`।
- ফাইলের নাম, পাথ, URL, variable নাম।
- `(((index term)))` মার্কার।
- `image::` directive-এর ভেতরের alt-text (ইংরেজিতেই); তবে `.caption` লাইন বাংলায়।

## পরিবর্তনের ইতিহাস

- **2026-08-07** — প্রাথমিক glossary তৈরি; chapter 1-3 নতুন convention অনুযায়ী retrofit করা হয়েছে। Fetch, Working Directory, এবং Stage (verb)-এর এন্ট্রি existing প্যাটার্নের সাথে সামঞ্জস্য রেখে যোগ করা হয়েছে।
- **2026-08-07 (v1.0)** — Glossary freeze করা হলো। "Decision Rationale" সেকশন আর "Compound/Derived টার্ম" টেবিল যোগ করা হয়েছে। Fast-forward, Detached HEAD, Index, Upstream, GitHub, Pull Request, Tracking Branch, Bare Repository, Conflict Marker-এর এন্ট্রি যোগ করা হয়েছে — এগুলোর প্রায় সবগুলোই chapter 1-3-এ ইতিমধ্যে শিপ হওয়া টেক্সট থেকে precedent হিসেবে নেওয়া, নতুন করে অনুমান করা হয়নি।

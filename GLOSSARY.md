# Pro Git বাংলা অনুবাদ — Glossary

এই ফাইলটাই Pro Git বাংলা অনুবাদের জন্য টার্মিনোলজির single source of truth।
নতুন কোনো টার্ম অনুবাদ করার আগে এখানে চেক করুন; এখানে না থাকলে, একটা সিদ্ধান্ত নিয়ে এই ফাইলে যোগ করুন, যাতে বাকি বইয়ে সেটা সামঞ্জস্যপূর্ণ থাকে (দেখুন [STYLE_GUIDE.md](STYLE_GUIDE.md)-এর নিয়ম ১৯: "Keep Consistent Terminology")।

> **আপডেট (2026-08-07):** আগে (chapter 1-3-এর প্রথম ড্রাফটে) Git-এর মূল টার্মগুলো Latin script-এ রাখা হচ্ছিল (যেমন "branch তৈরি করা")। এখন থেকে নিচের টেবিল অনুযায়ী, বেশিরভাগ core noun/verb বাংলা script-এ transliterate করা হচ্ছে (যেমন "ব্রাঞ্চ তৈরি করা")। Chapter 1-3 এই কনভেনশন অনুযায়ী retrofit করা হয়েছে।

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
| HEAD | সবসময় বড় হাতের অক্ষরে |
| Checkout | |
| Rebase | |
| Cherry-pick | |
| config / alias | |
| blob / tree (Git internal object types) | কম ব্যবহৃত internals টার্ম, glossary-তে কভার করা হয়নি বলে English-ই থাকবে — যেমন `nutshell.asc`-এ "একটা commit আর তার _blob_/_tree_" |

## কখনো অনুবাদ বা Transliterate করা হবে না

- কোনো `[source, ...]` ... `----` কোড ব্লকের ভেতরের যেকোনো কিছু (কমান্ড, ফ্ল্যাগ, আউটপুট) — অক্ষরে অক্ষরে অপরিবর্তিত।
- Inline code (`` `git commit` ``, `` `README.md` `` ইত্যাদি) যা কোনো literal কমান্ড, ফাইলের নাম, পাথ, ফ্ল্যাগ, বা identifier বোঝায়।
- Branch/remote-এর নাম যেমন `master`, `main`, `origin`, `iss53`, `hotfix`।
- ফাইলের নাম, পাথ, URL, variable নাম।
- `(((index term)))` মার্কার।
- `image::` directive-এর ভেতরের alt-text (ইংরেজিতেই); তবে `.caption` লাইন বাংলায়।

## পরিবর্তনের ইতিহাস

- **2026-08-07** — প্রাথমিক glossary তৈরি; chapter 1-3 নতুন convention অনুযায়ী retrofit করা হয়েছে। Fetch, Working Directory, এবং Stage (verb)-এর এন্ট্রি existing প্যাটার্নের সাথে সামঞ্জস্য রেখে যোগ করা হয়েছে।

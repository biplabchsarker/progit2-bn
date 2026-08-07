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
| Protocol | প্রোটোকল | Chapter 4-এ high-frequency core noun (SSH প্রোটোকল, HTTP প্রোটোকল...); অত্যন্ত প্রচলিত বাংলা loanword |
| Authentication | অথেনটিকেশন | সাধারণ security concept noun, conflict/snapshot-এর মতো একই ক্যাটেগরি। Verb রূপ: authenticate → অথেনটিকেট করা। Adjective রূপ: authenticated → অথেনটিকেটেড; unauthenticated → "অথেনটিকেশন ছাড়া" (আলাদা un-শব্দ না বানিয়ে phrase দিয়ে) |
| Group (GitLab-এর top-level org unit, Project-এর মতোই) | গ্রুপ | Project → প্রজেক্ট প্যাটার্নের সাথে সামঞ্জস্য রেখে |
| Port (network port) | পোর্ট | অত্যন্ত প্রচলিত বাংলা loanword |
| Firewall | ফায়ারওয়াল | প্রচলিত বাংলা loanword |
| Server | সার্ভার | Chapter 1-3-এই আগে থেকে এই রূপে ব্যবহৃত (remote-branches.asc), chapter 4-এ formalize করা হলো |
| Service | সার্ভিস | পোর্ট/ফায়ারওয়াল/প্রোটোকলের মতো একই ক্যাটেগরি — প্রচলিত loanword |
| Setup (noun, "a small setup") | সেটআপ | verb হিসেবে "সেট আপ করা" আগে থেকেই ব্যবহৃত; noun রূপও একই শব্দ |
| Interface | ইন্টারফেস | প্রচলিত loanword |
| Administration | অ্যাডমিনিস্ট্রেশন | প্রচলিত loanword |
| Organization (GitHub-এর top-level org unit) | অর্গানাইজেশন | GitLab-এর Group → গ্রুপ প্যাটার্নের সাথে সামঞ্জস্য রেখে। নিয়ম ৬-এর (Version Control) মতোই, বইয়ে প্রথম উল্লেখে উভয় ফর্ম দিন — "Organization (অর্গানাইজেশন)" (3-maintaining.asc-এ প্রথম ব্যবহৃত) — তারপর সবসময় শুধু "অর্গানাইজেশন" |
| Account | অ্যাকাউন্ট | অত্যন্ত প্রচলিত loanword |
| Notification | নোটিফিকেশন | প্রচলিত loanword |
| Token | টোকেন | প্রচলিত loanword |
| Avatar | অ্যাভাটার | প্রচলিত loanword |
| Profile | প্রোফাইল | প্রচলিত loanword |
| Team | টিম | Group/Organization-এর মতোই org-concept noun |
| Subgroup | উপগ্রুপ | বাংলা "উপ-" prefix + Group |
| Member | সদস্য | সাধারণ noun, native বাংলা শব্দ |
| Snippet | স্নিপেট | প্রচলিত loanword (কোড স্নিপেট) |
| Emoji | ইমোজি | প্রচলিত loanword |
| Export (verb, `git archive`-এর প্রসঙ্গে) | এক্সপোর্ট করা | কনফিগার করা/অথেনটিকেট করা-র মতোই loanword-transliteration প্যাটার্ন |

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
| Daemon | `git daemon` লিটারাল কমান্ডের সাথে ওভারল্যাপ করে বলে prose-এও English-ই থাকবে — section title "Git Daemon" অপরিবর্তিত |
| Hook | নির্দিষ্ট Git mechanism-এর নাম (pre-commit hook, post-receive hook...), Checkout/Rebase-এর মতো একই ক্যাটেগরি — ch08-এ আবার আসবে |
| SSH | প্রোটোকল/technology-র নাম হিসেবে সবসময় ইংরেজি acronym |
| Public key / Private key | "key" শব্দটার বাংলা ("কী") "কী?" (what?)-এর সাথে হুবহু এক বানান — বিভ্রান্তি এড়াতে পুরো phrase ইংরেজিতেই থাকবে |
| Passphrase | password-এর থেকে আলাদা একটা SSH-specific টার্ম — বাংলায় transliterate করলে ওই পার্থক্যটা হারিয়ে যায় |
| Namespace | কম ব্যবহৃত internals/GitLab টার্ম, blob/tree-র মতো একই ক্যাটেগরি |
| Wiki | GitLab UI-তে exact এই বানানেই দেখা যায়, GitHub UI টার্মের (Issues, Settings...) মতোই |
| Merge Request | GitLab-এর pull request-এর সমতুল্য UI টার্ম — Pull Request-এর মতোই কারণে ইংরেজিতেই থাকবে |
| Markdown | মার্কআপ ল্যাংগুয়েজের proper name |
| API | universal tech acronym |
| Settings | GitHub UI-তে exact এই বানানেই দেখা যায় (নিয়ম ১৭) |
| Webhook | নির্দিষ্ট mechanism-এর নাম, Hook-এর মতোই ক্যাটেগরি |
| Two-factor (Authentication) | নির্দিষ্ট security feature-এর নাম, Detached HEAD-এর মতোই ক্যাটেগরি — "Two-factor অথেনটিকেশন" (compound rule অনুযায়ী) |
| Watch (GitHub action, repo notifications subscribe করা) | Fork/Issue-এর মতোই নির্দিষ্ট UI action-এর নাম |
| Owner / Co-owner / Collaborator (project role) | Maintainer/Contributor-এর মতোই project-role noun ক্যাটেগরি — "Collaborators" GitHub-এর একটা literal menu-tab-এর নামও |
| Audit Log | literal UI tab-এর নাম, quote করে refer করা হয় |
| Task List | GitHub-এর নির্দিষ্ট feature-এর নাম |
| Mention (@mention feature) | নির্দিষ্ট UI action-এর নাম, Watch/Fork-এর মতোই |
| Ref / Refspec | low-level Git plumbing টার্ম, blob/tree/index-এর মতোই ক্যাটেগরি |
| Literal GitHub UI button/tab label (যেমন "New repository", "Add webhook", "Transfer ownership") | অনুবাদ না করে ইংরেজিতেই রাখুন, যাতে ইউজার আসল GitHub interface-এ সেটা খুঁজে পান — নিয়ম ১৭-এর সম্প্রসারণ |
| Access level label (read only / read-write / administrative-এর মতো literal permission label) | literal UI label হিসেবে ইংরেজিতেই থাকবে |
| Administrative (adjective form of Administration) | প্রশাসনিক — noun রূপ "অ্যাডমিনিস্ট্রেশন" ইংরেজি-বেসড থাকলেও adjective রূপ native বাংলা |
| Sign up / Log in (verb) | ইংরেজি verb + করা প্যাটার্নেই থাকবে ("sign up করা", "log in করা") — "সাইন আপ" transliterate করা হয়নি |
| Verified / Unverified | ভেরিফাই করা / "ভেরিফাই করা হয়নি" (phrase, আলাদা "আন-" শব্দ বানানো হয়নি — Authenticated/Unauthenticated প্যাটার্নের সাথে সামঞ্জস্য) |
| Configuration (noun) / Configure (verb) | কনফিগারেশন (noun, transliterate) / "কনফিগার করা" (verb, English+করা) |
| Fork | GitHub/GitLab UI-র একটা নির্দিষ্ট action-এর নাম, Pull/Merge Request-এর মতোই ক্যাটেগরি |
| Issue | GitHub/GitLab UI টার্ম, Wiki-র মতোই ক্যাটেগরি (lowercase-এই লেখা হয়, যেমন "issue তৈরি করা") |
| Access (standalone noun/verb, "SSH access", "access দেওয়া") | write access/read access/push access কম্পাউন্ডের precedent বাড়িয়ে standalone ব্যবহারেও প্রযোজ্য |
| Shell / git-shell | Unix concept + literal কমান্ড-নাম, Daemon/Hook-এর মতোই ক্যাটেগরি |
| CGI | প্রোটোকল/mechanism-এর acronym, SSH-এর মতোই ক্যাটেগরি |
| Instance ("repository instance", "GitLab instance") | কম ব্যবহৃত general CS noun, blob/tree-র মতোই ক্যাটেগরি — একবার transliterate করার চেষ্টা হয়েছিল (protocols.asc), কিন্তু বাকি chapter 4-এর সাথে মিলিয়ে English-এ ফিরিয়ে আনা হয়েছে |
| Patch | Chapter 1-এ (about-version-control.asc: "patch set", "patch") থেকেই English-এ প্রতিষ্ঠিত precedent |
| Contributor | Chapter 2-এ (remotes.asc: "কোনো contributor আর contribute করছেন না") থেকেই English-এ প্রতিষ্ঠিত precedent |
| Review / Code Review | Chapter 3/4-এ (workflows.asc, gitlab.asc: "code review-র সময়") থেকেই English-এ প্রতিষ্ঠিত precedent |
| Workflow | Chapter 1-4 জুড়ে সবসময় English (branching workflows, distributed workflows...) |
| Release | Chapter 1-4 জুড়ে সবসময় English ("ট্যাগ করা release", "build/release script") |
| Maintainer | Contributor-এর মতোই "প্রজেক্ট role" ক্যাটেগরি, একই যুক্তিতে English |
| Guideline | Review/Workflow-এর মতোই generic process-noun ক্যাটেগরি |
| Mailing List | Infrastructure-এর নাম, GitHub-এর মতোই ক্যাটেগরি |
| Squash | নির্দিষ্ট interactive-rebase action-এর নাম, Cherry-pick/Fast-forward-এর মতোই ক্যাটেগরি |
| Whitespace | সাধারণ প্রোগ্রামিং টার্ম, blob/tree-র মতোই ক্যাটেগরি |
| Shortlog | লিটারাল কমান্ডের নাম (`git shortlog`), Checkout/Rebase-এর মতোই ক্যাটেগরি |
| Changelog | টেকনিক্যাল convention/ফাইলের নাম |
| Build Number | টেকনিক্যাল টার্ম, একক ইউনিট হিসেবে English |
| Dictator and Lieutenants | নির্দিষ্ট নামের Git workflow model (Centralized/Integration-Manager Workflow-এর মতোই), proper name হিসেবে English |
| format-patch / mbox | লিটারাল কমান্ড/ফাইল-ফরম্যাটের নাম |
| Credential (credential helper) | Chapter 3/4/6-এ (remote-branches.asc, protocols.asc, 3-maintaining.asc) থেকেই English-এ প্রতিষ্ঠিত precedent |
| Hash / SHA-1 | Chapter 1-3-এ (what-is-git.asc, viewing-history.asc, nutshell.asc) থেকেই English-এ প্রতিষ্ঠিত precedent |
| Hunk | Chapter 1/2-এ (help.asc, recording-changes.asc) থেকেই English-এ প্রতিষ্ঠিত precedent |
| Stash | Chapter 2/3-এ (undoing.asc, basic-branching-and-merging.asc) থেকেই English-এ প্রতিষ্ঠিত precedent — `git stash` লিটারাল কমান্ডের সাথে ওভারল্যাপ, Checkout/Rebase-এর মতোই ক্যাটেগরি |
| GPG / Signature / Sign(ed/ing) | Chapter 1/2/5-এ (installing.asc, tagging.asc, maintaining.asc) থেকেই English-এ প্রতিষ্ঠিত precedent — "সাইন করা" ব্যবহার করবেন না, "sign করা"/"signed" |
| Rerere | Chapter 1/5-এ (first-time-setup.asc, maintaining.asc) থেকেই English-এ প্রতিষ্ঠিত precedent, `git rerere` লিটারাল কমান্ডের নাম |
| Submodule | নির্দিষ্ট Git feature-এর নাম, Daemon/Hook/Squash-এর মতোই ক্যাটেগরি, `git submodule` লিটারাল কমান্ডের সাথে ওভারল্যাপ |
| Subtree (merge) | নির্দিষ্ট Git feature-এর নাম, Submodule-এর মতোই ক্যাটেগরি, `git subtree`/`--subtree` লিটারাল কমান্ডের সাথে ওভারল্যাপ |
| Bisect | নির্দিষ্ট Git feature-এর নাম, `git bisect` লিটারাল কমান্ডের সাথে ওভারল্যাপ, Checkout/Rebase-এর মতোই ক্যাটেগরি |
| Blame | নির্দিষ্ট Git feature-এর নাম, `git blame` লিটারাল কমান্ডের সাথে ওভারল্যাপ, একই ক্যাটেগরি |
| Bundle | নির্দিষ্ট Git feature-এর নাম, `git bundle` লিটারাল কমান্ডের সাথে ওভারল্যাপ, একই ক্যাটেগরি |
| Reflog | নির্দিষ্ট Git mechanism-এর নাম, `git reflog` লিটারাল কমান্ডের সাথে ওভারল্যাপ, Ref/Refspec-এর মতোই ক্যাটেগরি |
| Worktree | নির্দিষ্ট Git feature-এর নাম, `git worktree` লিটারাল কমান্ডের সাথে ওভারল্যাপ, একই ক্যাটেগরি |
| Revision | Hash/SHA-1/Ref-এর মতোই low-level plumbing-adjacent noun ক্যাটেগরি, English-ই থাকবে (যেমন "Revision Selection" অধ্যায়ের শিরোনাম) |
| Replace (git replace) | নির্দিষ্ট Git command/feature-এর নাম, Checkout/Rebase-এর মতোই ক্যাটেগরি |
| Staged / Unstaged / Untracked (adjective, state-label) | Stage(verb)→স্টেজ করা থেকে আলাদা — chapter 2-এ (recording-changes.asc) থেকেই precedent, state-label হিসেবে English-ই থাকে |
| Unstage (verb) | "unstage করা" — English verb + করা প্যাটার্ন, Sign up করা/Log in করা-র মতোই |
| Username / Password | Chapter 3/4/6-এ প্রতিষ্ঠিত precedent অনুযায়ী transliterate — ইউজারনেম / পাসওয়ার্ড |
| Annotation (file annotation, `git blame`-এর প্রসঙ্গে) | কম ব্যবহৃত internals টার্ম, blob/tree-র মতোই ক্যাটেগরি |
| Grafting (history grafting) | নির্দিষ্ট টেকনিক্যাল mechanism-এর নাম, একই ক্যাটেগরি |
| Attribute (gitattributes) | নির্দিষ্ট Git feature-এর নাম, `.gitattributes` লিটারাল ফাইলের সাথে ওভারল্যাপ, Hook/Daemon-এর মতোই ক্যাটেগরি |
| Filter / Filter Driver (clean/smudge filter) | নির্দিষ্ট Git mechanism-এর নাম (gitattributes-এর filter attribute), Hook-এর মতোই ক্যাটেগরি — generic verb ব্যবহারে ("author দিয়ে ফিল্টার করা", chapter 2 precedent) transliterate থাকবে, কিন্তু এই নির্দিষ্ট mechanism-এর নাম হিসেবে English |
| Merge Driver / Diff Driver | Filter Driver-এর মতোই নির্দিষ্ট mechanism-এর নাম, English |
| Policy | Chapter 5-এ (contributing.asc) থেকেই English-এ প্রতিষ্ঠিত precedent |
| Environment Variable | Chapter 2/4-এ (recording-changes.asc, smart-http.asc) থেকেই English-এ প্রতিষ্ঠিত precedent |
| Line Ending (CRLF/LF) | নির্দিষ্ট টেকনিক্যাল টার্ম, Whitespace-এর মতোই ক্যাটেগরি, English |
| Keyword Expansion | নির্দিষ্ট Git mechanism-এর নাম, Filter Driver-এর মতোই ক্যাটেগরি |
| Template Directory (`git init` templates) | নির্দিষ্ট Git mechanism-এর নাম, একই ক্যাটেগরি |
| Mechanism / Argument / Directive | কম ব্যবহৃত generic CS/internals noun, blob/tree-র মতোই ক্যাটেগরি |
| Caveat / Exercise / Incantation | ক্যাজুয়াল টেকনিক্যাল প্রসঙ্গ (Scott Chacon-এর কণ্ঠস্বর, নিয়ম ২২), English-ই থাকবে |

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
| Interactive Staging | Interactive স্টেজিং | Staging Area/Stage(verb)-এর প্যাটার্ন মেনে — qualifier "Interactive" English-ই থাকে, base term "স্টেজিং" transliterate হয় |

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
- **2026-08-07 (chapter 4 prep)** — Chapter 4 (Git on the Server) অনুবাদ শুরুর আগে নতুন টার্ম যোগ করা হয়েছে: Protocol, Authentication, Group, Port, Firewall (transliterate); Daemon, Hook, SSH, Public/Private key, Passphrase, Namespace, Wiki, Merge Request (English-ই থাকবে)। প্যারালাল agent দিয়ে অনুবাদ করার আগে decide করে রাখা হয়েছে, যাতে আলাদা agent আলাদা সিদ্ধান্ত না নেয়।
- **2026-08-07 (chapter 4 অনুবাদের পর)** — অনুবাদ করার সময় agent-রা যে নতুন টার্ম নিয়ে সিদ্ধান্ত নিয়েছিল, সেগুলো consolidate করে যোগ করা হলো: Server, Service, Setup, Interface, Administration (transliterate); Fork, Issue, Access (standalone), Shell/git-shell, CGI, Instance (English-ই থাকবে); Authenticated/Unauthenticated adjective form। একটা inconsistency ধরা পড়েছিল ("instance" একটা ফাইলে transliterate হয়েছিল, বাকি দুটোয় English ছিল) — majority-এর সাথে মিলিয়ে ঠিক করা হয়েছে।
- **2026-08-07 (chapter 5 prep)** — Chapter 5 (Distributed Git) অনুবাদ শুরুর আগে ইতিমধ্যে shipped chapter 1-4-এ real precedent চেক করে দেখা গেল Patch, Contributor, Review, Workflow, Release — এই সবগুলোই আগে থেকে English-এ রয়ে গেছে (transliterate করার প্রাথমিক ধারণা ভুল ছিল)। এই precedent মেনে Maintainer, Guideline, Mailing List, Squash, Whitespace, Shortlog, Changelog, Build Number, Dictator and Lieutenants, format-patch/mbox — সবই English-ই রাখা হলো, নতুন করে transliterate না করে।
- **2026-08-07 (chapter 6 prep + পরে)** — Chapter 6 (GitHub) অনুবাদের আগে Organization, Account, Notification, Token, Avatar, Profile (transliterate) আর Markdown, API, Settings, Webhook, Two-factor, Watch (English) prep করা হয়েছিল। অনুবাদের সময় আরও কিছু যোগ হয়েছে: Team, Subgroup, Member, Snippet, Emoji (transliterate); Owner/Co-owner/Collaborator, Audit Log, Task List, Mention, Ref/Refspec, literal UI button/tab label, access-level label, Sign up/Log in verb, Verified/Unverified, Configuration/Configure noun-verb split (English)।
- **2026-08-07 (chapter 7-এর পর)** — অনুবাদের সময় agent-রা আরও কিছু judgment call নিয়েছিল, consolidate করে যোগ করা হলো: Staged/Unstaged/Untracked (adjective/state-label, English — Stage verb থেকে আলাদা), Unstage (verb, "unstage করা"), Username/Password (transliterate, precedent-confirmed), Annotation, Grafting (English, internals-category)।
- **2026-08-08 (editorial review — chapter 1)** — Chapter 1-এ একটা real glossary-violation পাওয়া গেছে: `first-time-setup.asc`-এ "কনফিগ" (config-এর clipped transliteration) লেখা হয়েছিল, যা "config/alias English-ই থাকবে" নিয়মের বিরোধী — ঠিক করে "config" করা হলো। এছাড়া STYLE_GUIDE.md-এ দুটো নতুন নিয়ম (২৪, ২৫) যোগ করা হয়েছে চ্যাপ্টার ৯ থেকে প্রযোজ্য হওয়ার জন্য — দেখুন STYLE_GUIDE.md।
- **2026-08-08 (editorial review — chapter 6-8)** — বাহ্যিক review-এর ভিত্তিতে দুটো সিদ্ধান্ত: (১) chapter 7-এ ভুলবশত দুটো জায়গায় "রিভিউ" transliterate হয়ে গিয়েছিল (Review-এর frozen English-precedent ভেঙে) — English "review"-এ ফিরিয়ে আনা হলো। (২) chapter 8-এর policy.asc-এ "enforce করা" সবজায়গায় "প্রয়োগ করা"-এ বদলানো হলো, apply→প্রয়োগ করা (chapter 5)-এর প্যাটার্নের সাথে সামঞ্জস্য রেখে। (৩) Organization-এর জন্য নিয়ম ৬-এর dual-form-on-first-mention প্যাটার্ন গ্রহণ করা হলো — এটা কেবল Organization-এর জন্যই প্রযোজ্য, সাধারণভাবে সব transliterated org-noun-এর জন্য না। Review-এ Stash/Credential/Namespace/maintain-contribute-customize নিয়ে যে "mixing" দাবি করা হয়েছিল, তা যাচাই করে ভুল প্রমাণিত হয়েছে (grep করে দেখা গেছে ইতিমধ্যেই consistent) — সেগুলোয় কোনো পরিবর্তন করা হয়নি।
- **2026-08-08 (chapter 8-এর পর)** — অনুবাদের সময় আরও কিছু judgment call consolidate করা হলো: Export (verb, "এক্সপোর্ট করা", transliterate); Mechanism/Argument/Directive (English, internals-noun ক্যাটেগরি); Caveat/Exercise/Incantation (English, Scott Chacon-এর ক্যাজুয়াল কণ্ঠস্বর)।
- **2026-08-07 (chapter 8 prep)** — Chapter 8 (Customizing Git) অনুবাদ শুরুর আগে chapter 1-6-এ real precedent চেক করে Policy, Environment Variable-কে English-এ প্রতিষ্ঠিত পাওয়া গেছে। নতুন টার্ম Attribute, Filter/Filter Driver, Merge Driver/Diff Driver, Line Ending, Keyword Expansion, Template Directory — সবই Hook/Daemon-এর প্যাটার্নে English রাখা হলো (নির্দিষ্ট Git feature/mechanism-এর নাম)।
- **2026-08-07 (chapter 7 prep)** — Chapter 7 (Git Tools) অনুবাদ শুরুর আগে chapter 1-6-এর shipped টেক্সটে real precedent চেক করে Credential, Hash/SHA-1, Hunk, Stash, GPG/Signature/Sign, Rerere — সবই English-এ প্রতিষ্ঠিত পাওয়া গেছে। নতুন টার্ম (আগে আসেনি) — Submodule, Subtree, Bisect, Blame, Bundle, Reflog, Worktree, Revision, Replace — সবই Checkout/Rebase/Daemon-এর প্যাটার্নে English রাখা হলো (নির্দিষ্ট Git feature/command-এর নাম)। Compound টার্ম Interactive Staging → "Interactive স্টেজিং" যোগ করা হয়েছে (Staging Area/Stage verb precedent অনুযায়ী)। PDF Bengali font থিম ফিক্স (theme/pdf/) deprioritize করা হয়েছে — `progit.asc`-এর `:pdf-theme:`/`:pdf-fontsdir:` অ্যাট্রিবিউট revert করে default build pipeline আবার সচল করা হয়েছে; থিম/ফন্ট ফাইলগুলো ভবিষ্যতের জন্য repo-তে থেকে যাচ্ছে।

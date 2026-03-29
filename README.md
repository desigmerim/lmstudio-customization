# lmstudio-customization
Customizations for LM Studio UI

LM Studio's UI is messy, so I've improved it.

All current code works with v0.4.0 to v0.4.8 (windows).

Should work for all v0.4 releases.

Pull requests welcome.

⚠️"main_window.js" is a single-line minified 32MB file. Use an editor that handles large files.


```

- Changed the color theme from Solarized Dark to a deep black theme (v0.4.8)
customLayerSolardark={id:"solardark",displayName:"Solarized Dark",mode:"dark",extends:"base.dark",semanticTokens:{"theme-swatch-shade-0":"rgb(0 43 54)","theme-swatch-shade-1":"rgb(2, 51, 63)","theme-swatch-shade-2":"rgb(3, 65, 81)","theme-swatch-shade-3":"rgb(6, 78, 98)","theme-swatch-shade-4":"rgb(13, 87, 107)","theme-swatch-shade-5":"rgb(28, 101, 121)","theme-swatch-shade-6":"rgb(39, 112, 132)","theme-swatch-shade-7":"rgb(72, 141, 160)","theme-swatch-shade-8":"rgb(105, 161, 176)","theme-swatch-shade-9":"rgb(128, 179, 194)","theme-swatch-shade-10":"rgb(155, 196, 207)",background:"rgb(0 43 54)",foreground:"rgb(174 187 199)",warning:"rgb(181 137 0)",destructive:"rgb(220 50 47)",active:"38 139 210","lm-indigo":"108 113 196","lm-green":"133 153 0","lm-red":"220 50 47","lm-yellow":"181 137 0","lm-blue":"38 139 210","lm-orange":"203 75 22","lm-teal":"65 176 188"},componentTokens:{appheader:"0 39 50","ascii-logo":"42 161 152","chatbody-foreground":"147 161 161",chatbubble:"2 56 70",chatbody:"0 43 54",chatinput:"2 56 70","chatinput-foreground":"154 167 169","chatinput-placeholder":"131 148 150",ring:"88 110 117"},customSwatches:{}}},
Replace to:
customLayerSolardark={id:"solardark",displayName:"Solarized Dark",mode:"dark",extends:"base.dark",semanticTokens:{"theme-swatch-shade-0":"rgb(14 14 14)","theme-swatch-shade-1":"rgb(8 8 8)","theme-swatch-shade-2":"rgb(20 20 20)","theme-swatch-shade-3":"rgb(28 28 28)","theme-swatch-shade-4":"rgb(38 38 38)","theme-swatch-shade-5":"rgb(52 52 52)","theme-swatch-shade-6":"rgb(70 70 70)","theme-swatch-shade-7":"rgb(95 95 95)","theme-swatch-shade-8":"rgb(125 125 125)","theme-swatch-shade-9":"rgb(160 160 160)","theme-swatch-shade-10":"rgb(200 200 200)",background:"rgb(14 14 14)",foreground:"rgb(210 210 210)",warning:"rgb(180 140 0)",destructive:"rgb(200 45 42)",active:"40 130 220","lm-indigo":"90 105 210","lm-green":"100 175 80","lm-red":"200 45 42","lm-yellow":"180 140 0","lm-blue":"40 130 220","lm-orange":"200 90 30","lm-teal":"40 160 200"},componentTokens:{appheader:"4 4 4","ascii-logo":"40 160 200","chatbody-foreground":"215 215 215",chatbubble:"18 18 18",chatbody:"14 14 14",chatinput:"18 18 18","chatinput-foreground":"200 200 200","chatinput-placeholder":"110 110 110",ring:"40 130 220"},customSwatches:{}}},

- Change the base font (v0.4.8)
tab-size: 4; /* 3 */\n  font-family: ui-sans-serif, system
Replace to:
tab-size: 4; /* 3 */\n  font-family: "Comic Sans MS", ui-sans-serif, system

- Monospaced font in code boxes (v0.4.8)
--fontStack-monospace: ui-monospace, SFMono-Regular, SF Mono, Menlo, Consolas, Liberation Mono,\r\n
Replace to:
--fontStack-monospace: ui-monospace, "Comic Sans MS",\r\n

- Scroll bar always visible (v0.4.8)
::-webkit-scrollbar-thumb {\r\n  background: #1c1c1c00;\r\n  border-radius: 2px;\r\n}\r\n\r\n:hover::-webkit-scrollbar-thumb {\r\n  background: #7a7a7a50;\r\n  cursor: pointer;\r\n  opacity: 0.1;\r\n}\r\n\r\n::-webkit-scrollbar-corner {\r\n  background: #00000000;\r\n}\r\n\r\n::-webkit-scrollbar-thumb:hover {\r\n  background: #7a7a7a;\r\n}
Replace to:
::-webkit-scrollbar-thumb {\r\n  background: #7a7a7a50;\r\n  border-radius: 2px;\r\n}\r\n\r\n:hover::-webkit-scrollbar-thumb {\r\n  background: #7a7a7a50;\r\n  cursor: pointer;\r\n  opacity: 0.1;\r\n}\r\n\r\n::-webkit-scrollbar-corner {\r\n  background: #00000000;\r\n}\r\n\r\n::-webkit-scrollbar-thumb:hover {\r\n  background: #7a7a7a50;\r\n}

- Change title bar color [3 places] (v0.4.8)
[1st place]
var(--tw-bg-opacity));\n}\r\n.bg-\\[\\#3154e1\\] {\n  --tw-bg-opacity: 1;\n  background-color: rgb(49 84 225
Replace to:
var(--tw-bg-opacity));\n}\r\n.bg-\\[\\#3154e1\\] {\n  --tw-bg-opacity: 1;\n  background-color: rgb(40 35 35
[2nd place]
[#222222] dark:text-[#DADADA]",e.WindowsAppStatusBarBackground="bg-[#3154e1]
Replace to:
[#222222] dark:text-[#DADADA]",e.WindowsAppStatusBarBackground="bg-[#282323]
[3rd place]
background-color: rgb(38 44 50 / var(--tw-bg-opacity));\n}\r\n.bg-\\[\\#3154e1
Replace to:
background-color: rgb(38 44 50 / var(--tw-bg-opacity));\n}\r\n.bg-\\[\\#282323

- Change Model tab bar color (v0.4.8)
"lm-indigo":"90 105 210"
Replace to:
"lm-indigo":"86 78 72"

- Widen line spacing (v0.4.8)
line-height {\r\n  line-height: 1.6
Replace to:
line-height {\r\n  line-height: 1.8

- Change Model Parameters - Accent Color (3 points RGB 40 130 220 → 90 80 75) (v0.4.8)
active:"40 130 220","lm-indigo":"90 105 210","lm-green":"100 175 80","lm-red":"200 45 42","lm-yellow":"180 140 0","lm-blue":"40 130 220","lm-orange":"200 90 30","lm-teal":"40 160 200"},componentTokens:{appheader:"4 4 4","ascii-logo":"40 160 200","chatbody-foreground":"215 215 215",chatbubble:"18 18 18",chatbody:"14 14 14",chatinput:"18 18 18","chatinput-foreground":"200 200 200","chatinput-placeholder":"110 110 110",ring:"40 130 220"}
Replace to:
active:"90 80 75","lm-indigo":"90 105 210","lm-green":"100 175 80","lm-red":"200 45 42","lm-yellow":"180 140 0","lm-blue":"90 80 75","lm-orange":"200 90 30","lm-teal":"40 160 200"},componentTokens:{appheader:"4 4 4","ascii-logo":"40 160 200","chatbody-foreground":"215 215 215",chatbubble:"18 18 18",chatbody:"14 14 14",chatinput:"18 18 18","chatinput-foreground":"200 200 200","chatinput-placeholder":"110 110 110",ring:"90 80 75"}

- Sort folders and chats alphabetically. (v0.4.8)
e.getChatSidebarComparator=function(t){const e="asc"===t.direction?1:-1;return(i,o)=>{const l="directory"===i.type?0:1,s="directory"===o.type?0:1;if(l!==s)return l-s;if("alphabetical"===t.field){const t=r(i),a=r(o),n=String(t).localeCompare(String(a),void 0,{sensitivity:"base"});return 0!==n?n*e:i.relativePath.localeCompare(o.relativePath)}{let r,l;return"file"===i.type&&"file"===o.type?(r=a(i,t.field),l=a(o,t.field)):"directory"===i.type&&"directory"===o.type?(r=n(i,t.field),l=n(o,t.field)):(r=0,l=0),r!==l?(r-l)*e:i.relativePath.localeCompare(o.relativePath)}}}
Replace to:
e.getChatSidebarComparator=function(t){return(i,o)=>{const l="directory"===i.type?0:1,s="directory"===o.type?0:1;if(l!==s)return l-s;const a=r(i),n=r(o),c=String(a).localeCompare(String(n),void 0,{sensitivity:"base"});return 0!==c?c:i.relativePath.localeCompare(o.relativePath)}}

- Markdown table text color (v0.4.8)
\r\n.markdown-body table td {\r\n  padding: 6px 13px;\r\n}
Replace to:
\r\n.markdown-body table td {\r\n  padding: 6px 13px;\r\n  color: rgb(230 230 220);\r\n}

- Blockquote text color (v0.4.8)
.markdown-body blockquote {\r\n  margin: 0;\r\n  padding: 0 1em;\r\n  color: var(--fgColor-muted);\r\n
Replace to:
.markdown-body blockquote {\r\n  margin: 0;\r\n  padding: 0 1em;\r\n  color: rgb(210, 210, 195);\r\n

- Reduce the weight of the bolded part within ** (v0.4.8)
markdown-body strong {\r\n  font-weight: var(--base-text-weight-semibold, 600)
Replace to:
markdown-body strong {\r\n  font-weight: var(--base-text-weight-semibold, 300)

- Reduce the weight of the headline text. (v0.4.8)
markdown-body {\r\n  --font-scale-h1: 1.6em;\r\n  --font-scale-h2: 1.35em;\r\n  --font-scale-h3: 1.18em;\r\n  --font-scale-h4: 1.13em;\r\n  --font-scale-h5: 1.1em;\r\n  --font-scale-h6: 1.08em;\r\n\r\n  --font-weight-h1: 600;\r\n  --font-weight-h2: 600;\r\n  --font-weight-h3: 500;\r\n  --font-weight-h4: 500;\r\n  --font-weight-h5: 500;\r\n  --font-weight-h6: 500;\r\n\r\n
Replace to:
markdown-body {\r\n  --font-scale-h1: 1.6em;\r\n  --font-scale-h2: 1.35em;\r\n  --font-scale-h3: 1.18em;\r\n  --font-scale-h4: 1.13em;\r\n  --font-scale-h5: 1.1em;\r\n  --font-scale-h6: 1.08em;\r\n\r\n  --font-weight-h1: 300;\r\n  --font-weight-h2: 300;\r\n  --font-weight-h3: 300;\r\n  --font-weight-h4: 300;\r\n  --font-weight-h5: 300;\r\n  --font-weight-h6: 300;\r\n\r\n

- Make the bold text enclosed in ** thinner. (v0.4.8)
\n.markdown-body strong {\r\n  font-weight: var(--base-text-weight-semibold, 300);\r\n}\r\n\
Replace to:
\n.markdown-body strong {\r\n  font-weight: 400;\r\n}\r\n\

- Change the MD table to draw even if there is no "-" in the rightmost column of the separator row. (v0.4.8)
hideCodeBlockCopyButton:u,hideCodeBlockLanguageHeader:g,codeblockIsClosedOverride:p,...v})=>{const m=(0,d.useMemo)((()=>({...k.customTagComponents,
Replace to:
hideCodeBlockCopyButton:u,hideCodeBlockLanguageHeader:g,codeblockIsClosedOverride:p,...v})=>{t=t.replace(/\|\s*:\s*(?=\|)/g,"|:-");const m=(0,d.useMemo)((()=>({...k.customTagComponents,


    Last updated: 2026-03-30
```

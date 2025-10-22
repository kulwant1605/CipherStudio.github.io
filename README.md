<!DOCTYPE html><html><head>
      <title>CipherStudio</title>
      <meta charset="utf-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      
      <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.22/dist/katex.min.css">
      
      
      
      
      
      <style>
      code[class*=language-],pre[class*=language-]{color:#333;background:0 0;font-family:Consolas,"Liberation Mono",Menlo,Courier,monospace;text-align:left;white-space:pre;word-spacing:normal;word-break:normal;word-wrap:normal;line-height:1.4;-moz-tab-size:8;-o-tab-size:8;tab-size:8;-webkit-hyphens:none;-moz-hyphens:none;-ms-hyphens:none;hyphens:none}pre[class*=language-]{padding:.8em;overflow:auto;border-radius:3px;background:#f5f5f5}:not(pre)>code[class*=language-]{padding:.1em;border-radius:.3em;white-space:normal;background:#f5f5f5}.token.blockquote,.token.comment{color:#969896}.token.cdata{color:#183691}.token.doctype,.token.macro.property,.token.punctuation,.token.variable{color:#333}.token.builtin,.token.important,.token.keyword,.token.operator,.token.rule{color:#a71d5d}.token.attr-value,.token.regex,.token.string,.token.url{color:#183691}.token.atrule,.token.boolean,.token.code,.token.command,.token.constant,.token.entity,.token.number,.token.property,.token.symbol{color:#0086b3}.token.prolog,.token.selector,.token.tag{color:#63a35c}.token.attr-name,.token.class,.token.class-name,.token.function,.token.id,.token.namespace,.token.pseudo-class,.token.pseudo-element,.token.url-reference .token.variable{color:#795da3}.token.entity{cursor:help}.token.title,.token.title .token.punctuation{font-weight:700;color:#1d3e81}.token.list{color:#ed6a43}.token.inserted{background-color:#eaffea;color:#55a532}.token.deleted{background-color:#ffecec;color:#bd2c00}.token.bold{font-weight:700}.token.italic{font-style:italic}.language-json .token.property{color:#183691}.language-markup .token.tag .token.punctuation{color:#333}.language-css .token.function,code.language-css{color:#0086b3}.language-yaml .token.atrule{color:#63a35c}code.language-yaml{color:#183691}.language-ruby .token.function{color:#333}.language-markdown .token.url{color:#795da3}.language-makefile .token.symbol{color:#795da3}.language-makefile .token.variable{color:#183691}.language-makefile .token.builtin{color:#0086b3}.language-bash .token.keyword{color:#0086b3}pre[data-line]{position:relative;padding:1em 0 1em 3em}pre[data-line] .line-highlight-wrapper{position:absolute;top:0;left:0;background-color:transparent;display:block;width:100%}pre[data-line] .line-highlight{position:absolute;left:0;right:0;padding:inherit 0;margin-top:1em;background:hsla(24,20%,50%,.08);background:linear-gradient(to right,hsla(24,20%,50%,.1) 70%,hsla(24,20%,50%,0));pointer-events:none;line-height:inherit;white-space:pre}pre[data-line] .line-highlight:before,pre[data-line] .line-highlight[data-end]:after{content:attr(data-start);position:absolute;top:.4em;left:.6em;min-width:1em;padding:0 .5em;background-color:hsla(24,20%,50%,.4);color:#f4f1ef;font:bold 65%/1.5 sans-serif;text-align:center;vertical-align:.3em;border-radius:999px;text-shadow:none;box-shadow:0 1px #fff}pre[data-line] .line-highlight[data-end]:after{content:attr(data-end);top:auto;bottom:.4em}html body{font-family:'Helvetica Neue',Helvetica,'Segoe UI',Arial,freesans,sans-serif;font-size:16px;line-height:1.6;color:#333;background-color:#fff;overflow:initial;box-sizing:border-box;word-wrap:break-word}html body>:first-child{margin-top:0}html body h1,html body h2,html body h3,html body h4,html body h5,html body h6{line-height:1.2;margin-top:1em;margin-bottom:16px;color:#000}html body h1{font-size:2.25em;font-weight:300;padding-bottom:.3em}html body h2{font-size:1.75em;font-weight:400;padding-bottom:.3em}html body h3{font-size:1.5em;font-weight:500}html body h4{font-size:1.25em;font-weight:600}html body h5{font-size:1.1em;font-weight:600}html body h6{font-size:1em;font-weight:600}html body h1,html body h2,html body h3,html body h4,html body h5{font-weight:600}html body h5{font-size:1em}html body h6{color:#5c5c5c}html body strong{color:#000}html body del{color:#5c5c5c}html body a:not([href]){color:inherit;text-decoration:none}html body a{color:#08c;text-decoration:none}html body a:hover{color:#00a3f5;text-decoration:none}html body img{max-width:100%}html body>p{margin-top:0;margin-bottom:16px;word-wrap:break-word}html body>ol,html body>ul{margin-bottom:16px}html body ol,html body ul{padding-left:2em}html body ol.no-list,html body ul.no-list{padding:0;list-style-type:none}html body ol ol,html body ol ul,html body ul ol,html body ul ul{margin-top:0;margin-bottom:0}html body li{margin-bottom:0}html body li.task-list-item{list-style:none}html body li>p{margin-top:0;margin-bottom:0}html body .task-list-item-checkbox{margin:0 .2em .25em -1.8em;vertical-align:middle}html body .task-list-item-checkbox:hover{cursor:pointer}html body blockquote{margin:16px 0;font-size:inherit;padding:0 15px;color:#5c5c5c;background-color:#f0f0f0;border-left:4px solid #d6d6d6}html body blockquote>:first-child{margin-top:0}html body blockquote>:last-child{margin-bottom:0}html body hr{height:4px;margin:32px 0;background-color:#d6d6d6;border:0 none}html body table{margin:10px 0 15px 0;border-collapse:collapse;border-spacing:0;display:block;width:100%;overflow:auto;word-break:normal;word-break:keep-all}html body table th{font-weight:700;color:#000}html body table td,html body table th{border:1px solid #d6d6d6;padding:6px 13px}html body dl{padding:0}html body dl dt{padding:0;margin-top:16px;font-size:1em;font-style:italic;font-weight:700}html body dl dd{padding:0 16px;margin-bottom:16px}html body code{font-family:Menlo,Monaco,Consolas,'Courier New',monospace;font-size:.85em;color:#000;background-color:#f0f0f0;border-radius:3px;padding:.2em 0}html body code::after,html body code::before{letter-spacing:-.2em;content:'\00a0'}html body pre>code{padding:0;margin:0;word-break:normal;white-space:pre;background:0 0;border:0}html body .highlight{margin-bottom:16px}html body .highlight pre,html body pre{padding:1em;overflow:auto;line-height:1.45;border:#d6d6d6;border-radius:3px}html body .highlight pre{margin-bottom:0;word-break:normal}html body pre code,html body pre tt{display:inline;max-width:initial;padding:0;margin:0;overflow:initial;line-height:inherit;word-wrap:normal;background-color:transparent;border:0}html body pre code:after,html body pre code:before,html body pre tt:after,html body pre tt:before{content:normal}html body blockquote,html body dl,html body ol,html body p,html body pre,html body ul{margin-top:0;margin-bottom:16px}html body kbd{color:#000;border:1px solid #d6d6d6;border-bottom:2px solid #c7c7c7;padding:2px 4px;background-color:#f0f0f0;border-radius:3px}@media print{html body{background-color:#fff}html body h1,html body h2,html body h3,html body h4,html body h5,html body h6{color:#000;page-break-after:avoid}html body blockquote{color:#5c5c5c}html body pre{page-break-inside:avoid}html body table{display:table}html body img{display:block;max-width:100%;max-height:100%}html body code,html body pre{word-wrap:break-word;white-space:pre}}.markdown-preview{width:100%;height:100%;box-sizing:border-box}.markdown-preview ul{list-style:disc}.markdown-preview ul ul{list-style:circle}.markdown-preview ul ul ul{list-style:square}.markdown-preview ol{list-style:decimal}.markdown-preview ol ol,.markdown-preview ul ol{list-style-type:lower-roman}.markdown-preview ol ol ol,.markdown-preview ol ul ol,.markdown-preview ul ol ol,.markdown-preview ul ul ol{list-style-type:lower-alpha}.markdown-preview .newpage,.markdown-preview .pagebreak{page-break-before:always}.markdown-preview pre.line-numbers{position:relative;padding-left:3.8em;counter-reset:linenumber}.markdown-preview pre.line-numbers>code{position:relative}.markdown-preview pre.line-numbers .line-numbers-rows{position:absolute;pointer-events:none;top:1em;font-size:100%;left:0;width:3em;letter-spacing:-1px;border-right:1px solid #999;-webkit-user-select:none;-moz-user-select:none;-ms-user-select:none;user-select:none}.markdown-preview pre.line-numbers .line-numbers-rows>span{pointer-events:none;display:block;counter-increment:linenumber}.markdown-preview pre.line-numbers .line-numbers-rows>span:before{content:counter(linenumber);color:#999;display:block;padding-right:.8em;text-align:right}.markdown-preview .mathjax-exps .MathJax_Display{text-align:center!important}.markdown-preview:not([data-for=preview]) .code-chunk .code-chunk-btn-group{display:none}.markdown-preview:not([data-for=preview]) .code-chunk .status{display:none}.markdown-preview:not([data-for=preview]) .code-chunk .output-div{margin-bottom:16px}.markdown-preview .md-toc{padding:0}.markdown-preview .md-toc .md-toc-link-wrapper .md-toc-link{display:inline;padding:.25rem 0}.markdown-preview .md-toc .md-toc-link-wrapper .md-toc-link div,.markdown-preview .md-toc .md-toc-link-wrapper .md-toc-link p{display:inline}.markdown-preview .md-toc .md-toc-link-wrapper.highlighted .md-toc-link{font-weight:800}.scrollbar-style::-webkit-scrollbar{width:8px}.scrollbar-style::-webkit-scrollbar-track{border-radius:10px;background-color:transparent}.scrollbar-style::-webkit-scrollbar-thumb{border-radius:5px;background-color:rgba(150,150,150,.66);border:4px solid rgba(150,150,150,.66);background-clip:content-box}html body[for=html-export]:not([data-presentation-mode]){position:relative;width:100%;height:100%;top:0;left:0;margin:0;padding:0;overflow:auto}html body[for=html-export]:not([data-presentation-mode]) .markdown-preview{position:relative;top:0;min-height:100vh}@media screen and (min-width:914px){html body[for=html-export]:not([data-presentation-mode]) .markdown-preview{padding:2em calc(50% - 457px + 2em)}}@media screen and (max-width:914px){html body[for=html-export]:not([data-presentation-mode]) .markdown-preview{padding:2em}}@media screen and (max-width:450px){html body[for=html-export]:not([data-presentation-mode]) .markdown-preview{font-size:14px!important;padding:1em}}@media print{html body[for=html-export]:not([data-presentation-mode]) #sidebar-toc-btn{display:none}}html body[for=html-export]:not([data-presentation-mode]) #sidebar-toc-btn{position:fixed;bottom:8px;left:8px;font-size:28px;cursor:pointer;color:inherit;z-index:99;width:32px;text-align:center;opacity:.4}html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] #sidebar-toc-btn{opacity:1}html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .md-sidebar-toc{position:fixed;top:0;left:0;width:300px;height:100%;padding:32px 0 48px 0;font-size:14px;box-shadow:0 0 4px rgba(150,150,150,.33);box-sizing:border-box;overflow:auto;background-color:inherit}html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .md-sidebar-toc::-webkit-scrollbar{width:8px}html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .md-sidebar-toc::-webkit-scrollbar-track{border-radius:10px;background-color:transparent}html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .md-sidebar-toc::-webkit-scrollbar-thumb{border-radius:5px;background-color:rgba(150,150,150,.66);border:4px solid rgba(150,150,150,.66);background-clip:content-box}html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .md-sidebar-toc a{text-decoration:none}html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .md-sidebar-toc .md-toc{padding:0 16px}html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .md-sidebar-toc .md-toc .md-toc-link-wrapper .md-toc-link{display:inline;padding:.25rem 0}html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .md-sidebar-toc .md-toc .md-toc-link-wrapper .md-toc-link div,html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .md-sidebar-toc .md-toc .md-toc-link-wrapper .md-toc-link p{display:inline}html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .md-sidebar-toc .md-toc .md-toc-link-wrapper.highlighted .md-toc-link{font-weight:800}html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .markdown-preview{left:300px;width:calc(100% - 300px);padding:2em calc(50% - 457px - 300px / 2);margin:0;box-sizing:border-box}@media screen and (max-width:1274px){html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .markdown-preview{padding:2em}}@media screen and (max-width:450px){html body[for=html-export]:not([data-presentation-mode])[html-show-sidebar-toc] .markdown-preview{width:100%}}html body[for=html-export]:not([data-presentation-mode]):not([html-show-sidebar-toc]) .markdown-preview{left:50%;transform:translateX(-50%)}html body[for=html-export]:not([data-presentation-mode]):not([html-show-sidebar-toc]) .md-sidebar-toc{display:none}
/* Please visit the URL below for more information: */
/*   https://shd101wyy.github.io/markdown-preview-enhanced/#/customize-css */

      </style>
      <!-- The content below will be included at the end of the <head> element. --><script type="text/javascript">
  document.addEventListener("DOMContentLoaded", function () {
    // your code here
  });
</script></head><body for="html-export">
    
    
      <div class="crossnote markdown-preview  ">
      <div>
<h1 id="-cipherstudio---complete-documentation">📘 CipherStudio - Complete Documentation </h1>
<h2 id="table-of-contents">Table of Contents </h2>
<ol>
<li><a href="#project-overview">Project Overview</a></li>
<li><a href="#features">Features</a></li>
<li><a href="#tech-stack">Tech Stack</a></li>
<li><a href="#architecture">Architecture</a></li>
<li><a href="#installation--setup">Installation &amp; Setup</a></li>
<li><a href="#environment-variables">Environment Variables</a></li>
<li><a href="#api-documentation">API Documentation</a></li>
<li><a href="#frontend-documentation">Frontend Documentation</a></li>
<li><a href="#database-schema">Database Schema</a></li>
<li><a href="#deployment-guide">Deployment Guide</a></li>
<li><a href="#usage-guide">Usage Guide</a></li>
<li><a href="#troubleshooting">Troubleshooting</a></li>
</ol>
<hr>
<h2 id="project-overview">Project Overview </h2>
<p><strong>CipherStudio</strong> is a modern, cloud-based code editor platform that allows users to create, edit, and preview web projects in real-time. Built with the MERN stack, it provides an integrated development environment (IDE) directly in the browser using Sandpack.</p>
<h3 id="key-capabilities">Key Capabilities </h3>
<ul>
<li>🔐 Secure user authentication with JWT</li>
<li>📁 Project and file management system</li>
<li>💻 Live code editing with syntax highlighting</li>
<li>👀 Real-time preview of code changes</li>
<li>🌐 Multi-language support (JavaScript, JSX, CSS, HTML, JSON)</li>
<li>💾 Auto-save functionality</li>
<li>🎨 Modern, responsive UI</li>
</ul>
<hr>
<h2 id="features">Features </h2>
<h3 id="user-management">User Management </h3>
<ul>
<li>User registration with email validation</li>
<li>Secure login with JWT tokens</li>
<li>Password hashing with bcrypt</li>
<li>Token-based authentication</li>
<li>Auto-login on page refresh</li>
<li>Secure logout</li>
</ul>
<h3 id="project-management">Project Management </h3>
<ul>
<li>Create unlimited projects</li>
<li>Update project names</li>
<li>Delete projects (cascade delete all files)</li>
<li>View all user projects</li>
<li>Unique project slugs with nanoid</li>
</ul>
<h3 id="file-system">File System </h3>
<ul>
<li>Create files and folders</li>
<li>Hierarchical folder structure</li>
<li>Update file content</li>
<li>Delete files/folders (recursive)</li>
<li>Duplicate name prevention</li>
<li>File size tracking</li>
<li>Language detection from file extension</li>
</ul>
<h3 id="code-editor">Code Editor </h3>
<ul>
<li>Live code preview with Sandpack</li>
<li>Syntax highlighting</li>
<li>Multi-tab support</li>
<li>Error display</li>
<li>Auto-refresh preview</li>
<li>Closable tabs</li>
<li>Line numbers</li>
<li>Code wrapping</li>
</ul>
<hr>
<h2 id="tech-stack">Tech Stack </h2>
<h3 id="frontend">Frontend </h3>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"framework"</span><span class="token operator">:</span> <span class="token string">"React 18.3.1"</span><span class="token punctuation">,</span>
  <span class="token property">"build-tool"</span><span class="token operator">:</span> <span class="token string">"Vite 6.0.5"</span><span class="token punctuation">,</span>
  <span class="token property">"styling"</span><span class="token operator">:</span> <span class="token string">"TailwindCSS 3.4.17"</span><span class="token punctuation">,</span>
  <span class="token property">"routing"</span><span class="token operator">:</span> <span class="token string">"React Router DOM 7.1.1"</span><span class="token punctuation">,</span>
  <span class="token property">"editor"</span><span class="token operator">:</span> <span class="token string">"Sandpack React 2.22.2"</span><span class="token punctuation">,</span>
  <span class="token property">"http-client"</span><span class="token operator">:</span> <span class="token string">"Axios 1.7.9"</span><span class="token punctuation">,</span>
  <span class="token property">"notifications"</span><span class="token operator">:</span> <span class="token string">"React Hot Toast 2.4.1"</span><span class="token punctuation">,</span>
  <span class="token property">"state"</span><span class="token operator">:</span> <span class="token string">"Context API"</span>
<span class="token punctuation">}</span>
</code></pre><h3 id="backend">Backend </h3>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"runtime"</span><span class="token operator">:</span> <span class="token string">"Node.js 18+"</span><span class="token punctuation">,</span>
  <span class="token property">"framework"</span><span class="token operator">:</span> <span class="token string">"Express 4.21.2"</span><span class="token punctuation">,</span>
  <span class="token property">"database"</span><span class="token operator">:</span> <span class="token string">"MongoDB with Mongoose 8.9.5"</span><span class="token punctuation">,</span>
  <span class="token property">"authentication"</span><span class="token operator">:</span> <span class="token string">"JWT (jsonwebtoken 9.0.2)"</span><span class="token punctuation">,</span>
  <span class="token property">"password"</span><span class="token operator">:</span> <span class="token string">"bcryptjs 2.4.3"</span><span class="token punctuation">,</span>
  <span class="token property">"id-generation"</span><span class="token operator">:</span> <span class="token string">"nanoid 5.0.9"</span><span class="token punctuation">,</span>
  <span class="token property">"cors"</span><span class="token operator">:</span> <span class="token string">"cors 2.8.5"</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h2 id="architecture">Architecture </h2>
<h3 id="system-architecture">System Architecture </h3>
<pre data-role="codeBlock" data-info="" class="language-text"><code>┌─────────────────────────────────────────────────────────┐
│                    Frontend (Vercel)                    │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐   │
│  │  React App   │  │   Context    │  │  Components  │   │
│  │  (Vite)      │─▶│   Provider   │─▶│  &amp; Pages     │   │
│  └──────────────┘  └──────────────┘  └──────────────┘   │
│         │                                      │        │
│         └───────────── Axios ──────────────────┘        │
└─────────────────────────────────────────────────────────┘
                            │
                            ▼ HTTPS/REST API
┌─────────────────────────────────────────────────────────┐
│                    Backend (Render)                     │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐   │
│  │   Express    │─▶│   Routes     │─▶│ Controllers  │   │
│  │   Server     │  │              │  │              │   │
│  └──────────────┘  └──────────────┘  └──────────────┘   │
│         │                  │                  │         │
│         ▼                  ▼                  ▼         │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐   │
│  │  Middleware  │  │    Models    │  │   MongoDB    │   │
│  │  (Auth/CORS) │  │  (Mongoose)  │─▶│   Database   │   │
│  └──────────────┘  └──────────────┘  └──────────────┘   │
└─────────────────────────────────────────────────────────┘
</code></pre><h3 id="folder-structure">Folder Structure </h3>
<pre data-role="codeBlock" data-info="" class="language-text"><code>CipherStudio/
├── backend/
│   └── server/
│       ├── config/          # Database configuration
│       │   └── db.js
│       ├── controllers/     # Business logic
│       │   ├── auth.controller.js
│       │   ├── File.controller.js
│       │   └── project.controller.js
│       ├── middlewares/     # Authentication middleware
│       │   └── auth.middleware.js
│       ├── models/          # Mongoose schemas
│       │   ├── User.model.js
│       │   ├── project.model.js
│       │   └── files.model.js
│       ├── routes/          # API routes
│       │   ├── auth.routes.js
│       │   ├── project.routes.js
│       │   └── File.routes.js
│       ├── .env            # Environment variables
│       ├── .env.sample     # Environment template
│       └── app.js          # Express app entry
│
└── frontend/
    └── cipherStudio/
        ├── public/          # Static assets
        ├── src/
        │   ├── assets/      # Images, icons
        │   ├── components/  # React components
        │   │   ├── Login.jsx
        │   │   ├── Navbar.jsx
        │   │   ├── CodeEditor.jsx
        │   │   └── SandpackEditor.jsx
        │   ├── context/     # Context API
        │   │   └── AppContext.jsx
        │   ├── pages/       # Page components
        │   │   ├── Home.jsx
        │   │   ├── Editor.jsx
        │   │   └── NotFound.jsx
        │   ├── App.jsx      # Main app
        │   ├── main.jsx     # Entry point
        │   ├── App.css
        │   └── index.css
        ├── .env            # Environment variables
        └── vite.config.js  # Vite configuration
</code></pre><hr>
<h2 id="installation--setup">Installation &amp; Setup </h2>
<h3 id="prerequisites">Prerequisites </h3>
<ul>
<li><strong>Node.js</strong> 18.x or higher</li>
<li><strong>MongoDB</strong> 4.4 or higher (local or Atlas)</li>
<li><strong>Git</strong> for version control</li>
<li><strong>npm</strong> or <strong>yarn</strong> package manager</li>
</ul>
<h3 id="step-1-clone-repository">Step 1: Clone Repository </h3>
<pre data-role="codeBlock" data-info="bash" class="language-bash bash"><code><span class="token function">git</span> clone https://github.com/kulwantolkha/cipherstudio.git
<span class="token builtin class-name">cd</span> CipherStudio
</code></pre><h3 id="step-2-backend-setup">Step 2: Backend Setup </h3>
<h4 id="install-dependencies">Install Dependencies </h4>
<pre data-role="codeBlock" data-info="bash" class="language-bash bash"><code><span class="token builtin class-name">cd</span> backend/server
<span class="token function">npm</span> <span class="token function">install</span>
</code></pre><h4 id="create-environment-file">Create Environment File </h4>
<pre data-role="codeBlock" data-info="bash" class="language-bash bash"><code><span class="token function">cp</span> .env.sample .env
</code></pre><p>Edit <code>.env</code>:</p>
<pre data-role="codeBlock" data-info="env" class="language-env env"><code>PORT=5000
MONGODB_URI=mongodb://localhost:27017/cipherstudio
JWT_SECRET=your_super_secret_jwt_key_minimum_32_characters_long
</code></pre><h4 id="start-backend-server">Start Backend Server </h4>
<pre data-role="codeBlock" data-info="bash" class="language-bash bash"><code><span class="token comment"># Development mode with auto-reload</span>
<span class="token function">npm</span> run dev

<span class="token comment"># Production mode</span>
<span class="token function">npm</span> start
</code></pre><p>Server runs on: <code>http://localhost:5000</code></p>
<h3 id="step-3-frontend-setup">Step 3: Frontend Setup </h3>
<h4 id="install-dependencies-1">Install Dependencies </h4>
<pre data-role="codeBlock" data-info="bash" class="language-bash bash"><code><span class="token builtin class-name">cd</span> <span class="token punctuation">..</span>/<span class="token punctuation">..</span>/frontend/cipherStudio
<span class="token function">npm</span> <span class="token function">install</span>
</code></pre><h4 id="create-environment-file-1">Create Environment File </h4>
<pre data-role="codeBlock" data-info="bash" class="language-bash bash"><code><span class="token function">cp</span> .env.sample .env
</code></pre><p>Edit <code>.env</code>:</p>
<pre data-role="codeBlock" data-info="env" class="language-env env"><code>VITE_API_URL=http://localhost:5000
</code></pre><h4 id="start-development-server">Start Development Server </h4>
<pre data-role="codeBlock" data-info="bash" class="language-bash bash"><code><span class="token function">npm</span> run dev
</code></pre><p>Frontend runs on: <code>http://localhost:5173</code></p>
<h3 id="step-4-verify-installation">Step 4: Verify Installation </h3>
<ol>
<li>
<p><strong>Backend Health Check</strong></p>
<pre data-role="codeBlock" data-info="bash" class="language-bash bash"><code><span class="token function">curl</span> http://localhost:5000/test
</code></pre><p>Should return:</p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"message"</span><span class="token operator">:</span> <span class="token string">"Backend is working!"</span><span class="token punctuation">,</span>
  <span class="token property">"cors"</span><span class="token operator">:</span> <span class="token string">"enabled"</span>
<span class="token punctuation">}</span>
</code></pre></li>
<li>
<p><strong>Frontend Access</strong></p>
<ul>
<li>Open browser: <code>http://localhost:5173</code></li>
<li>Should see CipherStudio homepage</li>
</ul>
</li>
<li>
<p><strong>Database Connection</strong></p>
<ul>
<li>Check backend terminal logs</li>
<li>Should see: <code>MongoDB Connected: &lt;your-db-name&gt;</code></li>
</ul>
</li>
</ol>
<hr>
<h2 id="environment-variables">Environment Variables </h2>
<h3 id="backend-env">Backend (.env) </h3>
<table>
<thead>
<tr>
<th>Variable</th>
<th>Description</th>
<th>Required</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>PORT</code></td>
<td>Server port number</td>
<td>✅</td>
<td><code>5000</code></td>
</tr>
<tr>
<td><code>MONGODB_URI</code></td>
<td>MongoDB connection string</td>
<td>✅</td>
<td><code>mongodb://localhost:27017/cipherstudio</code></td>
</tr>
<tr>
<td><code>JWT_SECRET</code></td>
<td>Secret key for JWT tokens</td>
<td>✅</td>
<td><code>your_super_secret_key_here</code></td>
</tr>
<tr>
<td><code>FRONTEND_URL</code></td>
<td>Allowed frontend origins</td>
<td>❌</td>
<td><code>http://localhost:5173,https://yourdomain.com</code></td>
</tr>
</tbody>
</table>
<p><strong>Security Notes:</strong></p>
<ul>
<li>Use a strong JWT_SECRET (minimum 32 characters)</li>
<li>Never commit <code>.env</code> file to Git</li>
<li>Use different secrets for development and production</li>
</ul>
<h3 id="frontend-env">Frontend (.env) </h3>
<table>
<thead>
<tr>
<th>Variable</th>
<th>Description</th>
<th>Required</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>VITE_API_URL</code></td>
<td>Backend API base URL</td>
<td>✅</td>
<td><code>http://localhost:5000</code></td>
</tr>
</tbody>
</table>
<p><strong>Notes:</strong></p>
<ul>
<li>In production, set to your deployed backend URL</li>
<li>No trailing slash</li>
<li>Must start with <code>VITE_</code> to be accessible in code</li>
</ul>
<hr>
<h2 id="api-documentation">API Documentation </h2>
<h3 id="base-url">Base URL </h3>
<ul>
<li><strong>Development:</strong> <code>http://localhost:5000</code></li>
<li><strong>Production:</strong> <code>https://your-backend-url.com</code></li>
</ul>
<h3 id="authentication">Authentication </h3>
<p>All authenticated routes require a JWT token in the Authorization header:</p>
<pre data-role="codeBlock" data-info="" class="language-text"><code>Authorization: Bearer &lt;token&gt;
</code></pre><hr>
<h3 id="auth-endpoints">Auth Endpoints </h3>
<h4 id="1-register-user">1. Register User </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>POST /api/auth/register
</code></pre><p><strong>Request Body:</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"firstName"</span><span class="token operator">:</span> <span class="token string">"John"</span><span class="token punctuation">,</span>
  <span class="token property">"lastName"</span><span class="token operator">:</span> <span class="token string">"Doe"</span><span class="token punctuation">,</span>
  <span class="token property">"email"</span><span class="token operator">:</span> <span class="token string">"john@example.com"</span><span class="token punctuation">,</span>
  <span class="token property">"password"</span><span class="token operator">:</span> <span class="token string">"password123"</span><span class="token punctuation">,</span>
  <span class="token property">"mobile"</span><span class="token operator">:</span> <span class="token string">"1234567890"</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Response (201):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"token"</span><span class="token operator">:</span> <span class="token string">"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."</span><span class="token punctuation">,</span>
  <span class="token property">"user"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3a"</span><span class="token punctuation">,</span>
    <span class="token property">"firstName"</span><span class="token operator">:</span> <span class="token string">"John"</span><span class="token punctuation">,</span>
    <span class="token property">"lastName"</span><span class="token operator">:</span> <span class="token string">"Doe"</span><span class="token punctuation">,</span>
    <span class="token property">"email"</span><span class="token operator">:</span> <span class="token string">"john@example.com"</span><span class="token punctuation">,</span>
    <span class="token property">"mobile"</span><span class="token operator">:</span> <span class="token string">"1234567890"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Error Responses:</strong></p>
<ul>
<li><code>400</code> - Missing fields or user already exists</li>
<li><code>500</code> - Server error</li>
</ul>
<hr>
<h4 id="2-login-user">2. Login User </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>POST /api/auth/login
</code></pre><p><strong>Request Body:</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"email"</span><span class="token operator">:</span> <span class="token string">"john@example.com"</span><span class="token punctuation">,</span>
  <span class="token property">"password"</span><span class="token operator">:</span> <span class="token string">"password123"</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Response (200):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"token"</span><span class="token operator">:</span> <span class="token string">"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."</span><span class="token punctuation">,</span>
  <span class="token property">"user"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3a"</span><span class="token punctuation">,</span>
    <span class="token property">"firstName"</span><span class="token operator">:</span> <span class="token string">"John"</span><span class="token punctuation">,</span>
    <span class="token property">"lastName"</span><span class="token operator">:</span> <span class="token string">"Doe"</span><span class="token punctuation">,</span>
    <span class="token property">"email"</span><span class="token operator">:</span> <span class="token string">"john@example.com"</span><span class="token punctuation">,</span>
    <span class="token property">"mobile"</span><span class="token operator">:</span> <span class="token string">"1234567890"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Error Responses:</strong></p>
<ul>
<li><code>400</code> - Missing email or password</li>
<li><code>401</code> - Invalid credentials</li>
<li><code>500</code> - Server error</li>
</ul>
<hr>
<h4 id="3-get-current-user">3. Get Current User </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>GET /api/auth/user
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Response (200):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"user"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3a"</span><span class="token punctuation">,</span>
    <span class="token property">"firstName"</span><span class="token operator">:</span> <span class="token string">"John"</span><span class="token punctuation">,</span>
    <span class="token property">"lastName"</span><span class="token operator">:</span> <span class="token string">"Doe"</span><span class="token punctuation">,</span>
    <span class="token property">"email"</span><span class="token operator">:</span> <span class="token string">"john@example.com"</span><span class="token punctuation">,</span>
    <span class="token property">"mobile"</span><span class="token operator">:</span> <span class="token string">"1234567890"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Error Responses:</strong></p>
<ul>
<li><code>401</code> - Not authenticated or invalid token</li>
<li><code>500</code> - Server error</li>
</ul>
<hr>
<h3 id="project-endpoints">Project Endpoints </h3>
<h4 id="1-create-project">1. Create Project </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>POST /api/projects
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Request Body:</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"My React App"</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Response (201):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"project"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3b"</span><span class="token punctuation">,</span>
    <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"My React App"</span><span class="token punctuation">,</span>
    <span class="token property">"slug"</span><span class="token operator">:</span> <span class="token string">"abc123xyz"</span><span class="token punctuation">,</span>
    <span class="token property">"userId"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3a"</span><span class="token punctuation">,</span>
    <span class="token property">"createdAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:00:00.000Z"</span><span class="token punctuation">,</span>
    <span class="token property">"updatedAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:00:00.000Z"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h4 id="2-get-user-projects">2. Get User Projects </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>GET /api/projects/user/:userId
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Response (200):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"projects"</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token punctuation">{</span>
      <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3b"</span><span class="token punctuation">,</span>
      <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"My React App"</span><span class="token punctuation">,</span>
      <span class="token property">"slug"</span><span class="token operator">:</span> <span class="token string">"abc123xyz"</span><span class="token punctuation">,</span>
      <span class="token property">"userId"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3a"</span><span class="token punctuation">,</span>
      <span class="token property">"createdAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:00:00.000Z"</span><span class="token punctuation">,</span>
      <span class="token property">"updatedAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:00:00.000Z"</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h4 id="3-get-project-by-id">3. Get Project by ID </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>GET /api/projects/:id
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Response (200):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"project"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3b"</span><span class="token punctuation">,</span>
    <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"My React App"</span><span class="token punctuation">,</span>
    <span class="token property">"slug"</span><span class="token operator">:</span> <span class="token string">"abc123xyz"</span><span class="token punctuation">,</span>
    <span class="token property">"userId"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3a"</span><span class="token punctuation">,</span>
    <span class="token property">"createdAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:00:00.000Z"</span><span class="token punctuation">,</span>
    <span class="token property">"updatedAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:00:00.000Z"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h4 id="4-update-project">4. Update Project </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>PUT /api/projects/:id
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Request Body:</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"Updated Project Name"</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Response (200):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"project"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3b"</span><span class="token punctuation">,</span>
    <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"Updated Project Name"</span><span class="token punctuation">,</span>
    <span class="token property">"slug"</span><span class="token operator">:</span> <span class="token string">"abc123xyz"</span><span class="token punctuation">,</span>
    <span class="token property">"userId"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3a"</span><span class="token punctuation">,</span>
    <span class="token property">"createdAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:00:00.000Z"</span><span class="token punctuation">,</span>
    <span class="token property">"updatedAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:30:00.000Z"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h4 id="5-delete-project">5. Delete Project </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>DELETE /api/projects/:id
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Response (200):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"message"</span><span class="token operator">:</span> <span class="token string">"Project deleted successfully"</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h3 id="file-endpoints">File Endpoints </h3>
<h4 id="1-create-filefolder">1. Create File/Folder </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>POST /api/files
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Request Body (File):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"projectId"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3b"</span><span class="token punctuation">,</span>
  <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"App.jsx"</span><span class="token punctuation">,</span>
  <span class="token property">"type"</span><span class="token operator">:</span> <span class="token string">"file"</span><span class="token punctuation">,</span>
  <span class="token property">"content"</span><span class="token operator">:</span> <span class="token string">"export default function App() { return &lt;div&gt;Hello&lt;/div&gt;; }"</span><span class="token punctuation">,</span>
  <span class="token property">"language"</span><span class="token operator">:</span> <span class="token string">"jsx"</span><span class="token punctuation">,</span>
  <span class="token property">"parentId"</span><span class="token operator">:</span> <span class="token null keyword">null</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Request Body (Folder):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"projectId"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3b"</span><span class="token punctuation">,</span>
  <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"components"</span><span class="token punctuation">,</span>
  <span class="token property">"type"</span><span class="token operator">:</span> <span class="token string">"folder"</span><span class="token punctuation">,</span>
  <span class="token property">"parentId"</span><span class="token operator">:</span> <span class="token null keyword">null</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Response (201):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"file"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3c"</span><span class="token punctuation">,</span>
    <span class="token property">"projectId"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3b"</span><span class="token punctuation">,</span>
    <span class="token property">"parentId"</span><span class="token operator">:</span> <span class="token null keyword">null</span><span class="token punctuation">,</span>
    <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"App.jsx"</span><span class="token punctuation">,</span>
    <span class="token property">"type"</span><span class="token operator">:</span> <span class="token string">"file"</span><span class="token punctuation">,</span>
    <span class="token property">"content"</span><span class="token operator">:</span> <span class="token string">"export default function App() { return &lt;div&gt;Hello&lt;/div&gt;; }"</span><span class="token punctuation">,</span>
    <span class="token property">"language"</span><span class="token operator">:</span> <span class="token string">"jsx"</span><span class="token punctuation">,</span>
    <span class="token property">"sizeInBytes"</span><span class="token operator">:</span> <span class="token number">52</span><span class="token punctuation">,</span>
    <span class="token property">"createdAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:00:00.000Z"</span><span class="token punctuation">,</span>
    <span class="token property">"updatedAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:00:00.000Z"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h4 id="2-get-project-files">2. Get Project Files </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>GET /api/files/project/:projectId
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Response (200):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"files"</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token punctuation">{</span>
      <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3c"</span><span class="token punctuation">,</span>
      <span class="token property">"projectId"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3b"</span><span class="token punctuation">,</span>
      <span class="token property">"parentId"</span><span class="token operator">:</span> <span class="token null keyword">null</span><span class="token punctuation">,</span>
      <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"App.jsx"</span><span class="token punctuation">,</span>
      <span class="token property">"type"</span><span class="token operator">:</span> <span class="token string">"file"</span><span class="token punctuation">,</span>
      <span class="token property">"content"</span><span class="token operator">:</span> <span class="token string">"export default function App() { return &lt;div&gt;Hello&lt;/div&gt;; }"</span><span class="token punctuation">,</span>
      <span class="token property">"language"</span><span class="token operator">:</span> <span class="token string">"jsx"</span><span class="token punctuation">,</span>
      <span class="token property">"sizeInBytes"</span><span class="token operator">:</span> <span class="token number">52</span><span class="token punctuation">,</span>
      <span class="token property">"createdAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:00:00.000Z"</span><span class="token punctuation">,</span>
      <span class="token property">"updatedAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:00:00.000Z"</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h4 id="3-get-folder-contents">3. Get Folder Contents </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>GET /api/files/folder/:folderId
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Response (200):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"contents"</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token punctuation">{</span>
      <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3d"</span><span class="token punctuation">,</span>
      <span class="token property">"projectId"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3b"</span><span class="token punctuation">,</span>
      <span class="token property">"parentId"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3c"</span><span class="token punctuation">,</span>
      <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"Button.jsx"</span><span class="token punctuation">,</span>
      <span class="token property">"type"</span><span class="token operator">:</span> <span class="token string">"file"</span><span class="token punctuation">,</span>
      <span class="token property">"content"</span><span class="token operator">:</span> <span class="token string">"..."</span><span class="token punctuation">,</span>
      <span class="token property">"language"</span><span class="token operator">:</span> <span class="token string">"jsx"</span><span class="token punctuation">,</span>
      <span class="token property">"sizeInBytes"</span><span class="token operator">:</span> <span class="token number">120</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h4 id="4-get-file-by-id">4. Get File by ID </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>GET /api/files/:id
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Response (200):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"file"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3c"</span><span class="token punctuation">,</span>
    <span class="token property">"projectId"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3b"</span><span class="token punctuation">,</span>
    <span class="token property">"parentId"</span><span class="token operator">:</span> <span class="token null keyword">null</span><span class="token punctuation">,</span>
    <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"App.jsx"</span><span class="token punctuation">,</span>
    <span class="token property">"type"</span><span class="token operator">:</span> <span class="token string">"file"</span><span class="token punctuation">,</span>
    <span class="token property">"content"</span><span class="token operator">:</span> <span class="token string">"export default function App() { return &lt;div&gt;Hello&lt;/div&gt;; }"</span><span class="token punctuation">,</span>
    <span class="token property">"language"</span><span class="token operator">:</span> <span class="token string">"jsx"</span><span class="token punctuation">,</span>
    <span class="token property">"sizeInBytes"</span><span class="token operator">:</span> <span class="token number">52</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h4 id="5-update-file">5. Update File </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>PUT /api/files/:id
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Request Body:</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"content"</span><span class="token operator">:</span> <span class="token string">"export default function App() { return &lt;div&gt;Updated!&lt;/div&gt;; }"</span><span class="token punctuation">,</span>
  <span class="token property">"name"</span><span class="token operator">:</span> <span class="token string">"App.jsx"</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Response (200):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"file"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"_id"</span><span class="token operator">:</span> <span class="token string">"60d5ec49f1b2c72b8c8e4f3c"</span><span class="token punctuation">,</span>
    <span class="token property">"content"</span><span class="token operator">:</span> <span class="token string">"export default function App() { return &lt;div&gt;Updated!&lt;/div&gt;; }"</span><span class="token punctuation">,</span>
    <span class="token property">"sizeInBytes"</span><span class="token operator">:</span> <span class="token number">58</span><span class="token punctuation">,</span>
    <span class="token property">"updatedAt"</span><span class="token operator">:</span> <span class="token string">"2025-01-22T10:30:00.000Z"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h4 id="6-delete-filefolder">6. Delete File/Folder </h4>
<pre data-role="codeBlock" data-info="http" class="language-http http"><code>DELETE /api/files/:id
<span class="token header"><span class="token header-name keyword">Authorization</span><span class="token punctuation">:</span> <span class="token header-value">Bearer &lt;token&gt;</span></span>
</code></pre><p><strong>Response (200):</strong></p>
<pre data-role="codeBlock" data-info="json" class="language-json json"><code><span class="token punctuation">{</span>
  <span class="token property">"success"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token property">"message"</span><span class="token operator">:</span> <span class="token string">"file deleted successfully"</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Note:</strong> Deleting a folder recursively deletes all its contents.</p>
<hr>
<h2 id="frontend-documentation">Frontend Documentation </h2>
<h3 id="components">Components </h3>
<h4 id="1-appcontextjsx">1. <strong>AppContext.jsx</strong> </h4>
<p>Global state management using Context API.</p>
<p><strong>Provides:</strong></p>
<ul>
<li><code>user</code> - Current logged-in user</li>
<li><code>token</code> - JWT authentication token</li>
<li><code>showLogin</code> - Login modal visibility</li>
<li><code>loading</code> - Authentication loading state</li>
<li><code>login(email, password)</code> - Login function</li>
<li><code>register(...)</code> - Registration function</li>
<li><code>logout()</code> - Logout function</li>
<li><code>axios</code> - Configured axios instance</li>
</ul>
<p><strong>Usage:</strong></p>
<pre data-role="codeBlock" data-info="jsx" class="language-jsx jsx"><code><span class="token keyword module keyword-import">import</span> <span class="token imports"><span class="token punctuation">{</span> useAppContext <span class="token punctuation">}</span></span> <span class="token keyword module keyword-from">from</span> <span class="token string">'../context/AppContext'</span><span class="token punctuation">;</span>

<span class="token keyword keyword-function">function</span> <span class="token function"><span class="token maybe-class-name">MyComponent</span></span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword keyword-const">const</span> <span class="token punctuation">{</span> user<span class="token punctuation">,</span> login<span class="token punctuation">,</span> logout <span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token function">useAppContext</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  
  <span class="token keyword control-flow keyword-if">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>user<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword control-flow keyword-return">return</span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">onClick</span><span class="token script language-javascript"><span class="token script-punctuation punctuation">=</span><span class="token punctuation">{</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token arrow operator">=&gt;</span> <span class="token function">login</span><span class="token punctuation">(</span><span class="token string">'email'</span><span class="token punctuation">,</span> <span class="token string">'pass'</span><span class="token punctuation">)</span><span class="token punctuation">}</span></span><span class="token punctuation">&gt;</span></span><span class="token plain-text">Login</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
  
  <span class="token keyword control-flow keyword-return">return</span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">onClick</span><span class="token script language-javascript"><span class="token script-punctuation punctuation">=</span><span class="token punctuation">{</span>logout<span class="token punctuation">}</span></span><span class="token punctuation">&gt;</span></span><span class="token plain-text">Logout</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre><hr>
<h4 id="2-loginjsx">2. <strong>Login.jsx</strong> </h4>
<p>Authentication modal for login and registration.</p>
<p><strong>Features:</strong></p>
<ul>
<li>Toggle between login/register</li>
<li>Form validation</li>
<li>Error handling with toast notifications</li>
<li>Loading states</li>
</ul>
<p><strong>Props:</strong> None (uses context)</p>
<hr>
<h4 id="3-navbarjsx">3. <strong>Navbar.jsx</strong> </h4>
<p>Top navigation bar.</p>
<p><strong>Features:</strong></p>
<ul>
<li>Logo/brand</li>
<li>User info display</li>
<li>Login/Logout button</li>
<li>Responsive design</li>
</ul>
<p><strong>Props:</strong> None (uses context)</p>
<hr>
<h4 id="4-sandpackeditorjsx">4. <strong>SandpackEditor.jsx</strong> </h4>
<p>Main code editor component using Sandpack.</p>
<p><strong>Features:</strong></p>
<ul>
<li>Live code preview</li>
<li>Multi-file support</li>
<li>Syntax highlighting</li>
<li>Auto-save</li>
<li>File creation/deletion</li>
<li>Tab management</li>
</ul>
<p><strong>Props:</strong></p>
<pre data-role="codeBlock" data-info="typescript" class="language-typescript typescript"><code><span class="token punctuation">{</span>
  projectId<span class="token operator">:</span> <span class="token builtin">string</span><span class="token punctuation">;</span>  <span class="token comment">// Project ID</span>
  files<span class="token operator">:</span> <span class="token builtin">Array</span><span class="token operator">&lt;</span>File<span class="token operator">&gt;</span><span class="token punctuation">;</span> <span class="token comment">// File objects from API</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Usage:</strong></p>
<pre data-role="codeBlock" data-info="jsx" class="language-jsx jsx"><code><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span><span class="token class-name">SandpackEditor</span></span> 
  <span class="token attr-name">projectId</span><span class="token attr-value"><span class="token punctuation attr-equals">=</span><span class="token punctuation">"</span>60d5ec49f1b2c72b8c8e4f3b<span class="token punctuation">"</span></span>
  <span class="token attr-name">files</span><span class="token script language-javascript"><span class="token script-punctuation punctuation">=</span><span class="token punctuation">{</span>projectFiles<span class="token punctuation">}</span></span>
<span class="token punctuation">/&gt;</span></span>
</code></pre><hr>
<h3 id="pages">Pages </h3>
<h4 id="1-homejsx">1. <strong>Home.jsx</strong> </h4>
<p>Landing page showing user's projects.</p>
<p><strong>Features:</strong></p>
<ul>
<li>Project list grid</li>
<li>Create new project</li>
<li>Open editor</li>
<li>Delete project</li>
<li>Empty state</li>
</ul>
<hr>
<h4 id="2-editorjsx">2. <strong>Editor.jsx</strong> </h4>
<p>Full-screen code editor page.</p>
<p><strong>Features:</strong></p>
<ul>
<li>Loads project by ID from URL</li>
<li>Fetches project files</li>
<li>Renders SandpackEditor</li>
<li>Loading state</li>
<li>Error handling</li>
</ul>
<p><strong>Route:</strong> <code>/editor/:projectId</code></p>
<hr>
<h4 id="3-notfoundjsx">3. <strong>NotFound.jsx</strong> </h4>
<p>404 error page.</p>
<p><strong>Route:</strong> <code>*</code> (catch-all)</p>
<hr>
<h3 id="routing">Routing </h3>
<pre data-role="codeBlock" data-info="jsx" class="language-jsx jsx"><code><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span><span class="token class-name">Routes</span></span><span class="token punctuation">&gt;</span></span><span class="token plain-text">
  </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span><span class="token class-name">Route</span></span> <span class="token attr-name">path</span><span class="token attr-value"><span class="token punctuation attr-equals">=</span><span class="token punctuation">"</span>/<span class="token punctuation">"</span></span> <span class="token attr-name">element</span><span class="token script language-javascript"><span class="token script-punctuation punctuation">=</span><span class="token punctuation">{</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span><span class="token class-name">Home</span></span> <span class="token punctuation">/&gt;</span></span><span class="token punctuation">}</span></span> <span class="token punctuation">/&gt;</span></span><span class="token plain-text">
  </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span><span class="token class-name">Route</span></span> <span class="token attr-name">path</span><span class="token attr-value"><span class="token punctuation attr-equals">=</span><span class="token punctuation">"</span>/editor/:projectId<span class="token punctuation">"</span></span> <span class="token attr-name">element</span><span class="token script language-javascript"><span class="token script-punctuation punctuation">=</span><span class="token punctuation">{</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span><span class="token class-name">Editor</span></span> <span class="token punctuation">/&gt;</span></span><span class="token punctuation">}</span></span> <span class="token punctuation">/&gt;</span></span><span class="token plain-text">
  </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span><span class="token class-name">Route</span></span> <span class="token attr-name">path</span><span class="token attr-value"><span class="token punctuation attr-equals">=</span><span class="token punctuation">"</span>*<span class="token punctuation">"</span></span> <span class="token attr-name">element</span><span class="token script language-javascript"><span class="token script-punctuation punctuation">=</span><span class="token punctuation">{</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span><span class="token class-name">NotFound</span></span> <span class="token punctuation">/&gt;</span></span><span class="token punctuation">}</span></span> <span class="token punctuation">/&gt;</span></span><span class="token plain-text">
</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span><span class="token class-name">Routes</span></span><span class="token punctuation">&gt;</span></span>
</code></pre><hr>
<h2 id="database-schema">Database Schema </h2>
<h3 id="user-model">User Model </h3>
<pre data-role="codeBlock" data-info="javascript" class="language-javascript javascript"><code><span class="token punctuation">{</span>
  <span class="token literal-property property">firstName</span><span class="token operator">:</span> <span class="token punctuation">{</span> <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">String</span><span class="token punctuation">,</span> <span class="token literal-property property">required</span><span class="token operator">:</span> <span class="token boolean">true</span> <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">lastName</span><span class="token operator">:</span> <span class="token punctuation">{</span> <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">String</span><span class="token punctuation">,</span> <span class="token literal-property property">required</span><span class="token operator">:</span> <span class="token boolean">true</span> <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">email</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">String</span><span class="token punctuation">,</span> 
    <span class="token literal-property property">required</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span> 
    <span class="token literal-property property">unique</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token literal-property property">lowercase</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token literal-property property">trim</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">password</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">String</span><span class="token punctuation">,</span> 
    <span class="token literal-property property">required</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token literal-property property">minLength</span><span class="token operator">:</span> <span class="token number">6</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">mobile</span><span class="token operator">:</span> <span class="token punctuation">{</span> <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">String</span> <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">createdAt</span><span class="token operator">:</span> <span class="token punctuation">{</span> <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">,</span> <span class="token keyword module keyword-default">default</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">.</span><span class="token property-access">now</span> <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">updatedAt</span><span class="token operator">:</span> <span class="token punctuation">{</span> <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">,</span> <span class="token keyword module keyword-default">default</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">.</span><span class="token property-access">now</span> <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Indexes:</strong></p>
<ul>
<li><code>email</code> (unique)</li>
</ul>
<hr>
<h3 id="project-model">Project Model </h3>
<pre data-role="codeBlock" data-info="javascript" class="language-javascript javascript"><code><span class="token punctuation">{</span>
  <span class="token literal-property property">name</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">String</span><span class="token punctuation">,</span> 
    <span class="token literal-property property">required</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token literal-property property">trim</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">slug</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">String</span><span class="token punctuation">,</span> 
    <span class="token literal-property property">required</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token literal-property property">unique</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">userId</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token maybe-class-name">ObjectId</span><span class="token punctuation">,</span> 
    <span class="token literal-property property">ref</span><span class="token operator">:</span> <span class="token string">'User'</span><span class="token punctuation">,</span>
    <span class="token literal-property property">required</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">createdAt</span><span class="token operator">:</span> <span class="token punctuation">{</span> <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">,</span> <span class="token keyword module keyword-default">default</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">.</span><span class="token property-access">now</span> <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">updatedAt</span><span class="token operator">:</span> <span class="token punctuation">{</span> <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">,</span> <span class="token keyword module keyword-default">default</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">.</span><span class="token property-access">now</span> <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Indexes:</strong></p>
<ul>
<li><code>slug</code> (unique)</li>
<li><code>userId</code></li>
</ul>
<hr>
<h3 id="file-model">File Model </h3>
<pre data-role="codeBlock" data-info="javascript" class="language-javascript javascript"><code><span class="token punctuation">{</span>
  <span class="token literal-property property">projectId</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token maybe-class-name">ObjectId</span><span class="token punctuation">,</span> 
    <span class="token literal-property property">ref</span><span class="token operator">:</span> <span class="token string">'Project'</span><span class="token punctuation">,</span>
    <span class="token literal-property property">required</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">parentId</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token maybe-class-name">ObjectId</span><span class="token punctuation">,</span> 
    <span class="token literal-property property">ref</span><span class="token operator">:</span> <span class="token string">'File'</span><span class="token punctuation">,</span>
    <span class="token keyword module keyword-default">default</span><span class="token operator">:</span> <span class="token keyword null nil keyword-null">null</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">name</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">String</span><span class="token punctuation">,</span> 
    <span class="token literal-property property">required</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token literal-property property">trim</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">String</span><span class="token punctuation">,</span> 
    <span class="token keyword keyword-enum">enum</span><span class="token operator">:</span> <span class="token punctuation">[</span><span class="token string">'file'</span><span class="token punctuation">,</span> <span class="token string">'folder'</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token literal-property property">required</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">content</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">String</span><span class="token punctuation">,</span>
    <span class="token keyword module keyword-default">default</span><span class="token operator">:</span> <span class="token string">''</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">language</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">String</span><span class="token punctuation">,</span>
    <span class="token keyword module keyword-default">default</span><span class="token operator">:</span> <span class="token string">'plaintext'</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">sizeInBytes</span><span class="token operator">:</span> <span class="token punctuation">{</span> 
    <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">Number</span><span class="token punctuation">,</span>
    <span class="token keyword module keyword-default">default</span><span class="token operator">:</span> <span class="token number">0</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">createdAt</span><span class="token operator">:</span> <span class="token punctuation">{</span> <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">,</span> <span class="token keyword module keyword-default">default</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">.</span><span class="token property-access">now</span> <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token literal-property property">updatedAt</span><span class="token operator">:</span> <span class="token punctuation">{</span> <span class="token literal-property property">type</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">,</span> <span class="token keyword module keyword-default">default</span><span class="token operator">:</span> <span class="token known-class-name class-name">Date</span><span class="token punctuation">.</span><span class="token property-access">now</span> <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><p><strong>Indexes:</strong></p>
<ul>
<li><code>projectId</code></li>
<li><code>parentId</code></li>
<li>Compound: <code>projectId + parentId + name</code> (unique)</li>
</ul>
<hr>
<h2 id="deployment-guide">Deployment Guide </h2>
<h3 id="backend-deployment-render">Backend Deployment (Render) </h3>
<h4 id="step-1-prepare-backend">Step 1: Prepare Backend </h4>
<ol>
<li>Ensure <code>.gitignore</code> excludes <code>.env</code> and <code>node_modules</code></li>
<li>Commit all changes</li>
<li>Push to GitHub</li>
</ol>
<h4 id="step-2-create-render-service">Step 2: Create Render Service </h4>
<ol>
<li>Go to <a href="https://dashboard.render.com/">Render Dashboard</a></li>
<li>Click <strong>New</strong> → <strong>Web Service</strong></li>
<li>Connect your GitHub repository</li>
<li>Configure:
<ul>
<li><strong>Name:</strong> <code>cipherstudio-backend</code></li>
<li><strong>Branch:</strong> <code>main</code></li>
<li><strong>Root Directory:</strong> <code>backend/server</code></li>
<li><strong>Build Command:</strong> <code>npm install</code></li>
<li><strong>Start Command:</strong> <code>npm start</code></li>
<li><strong>Environment:</strong> <code>Node</code></li>
</ul>
</li>
</ol>
<h4 id="step-3-set-environment-variables">Step 3: Set Environment Variables </h4>
<p>Add in Render dashboard:</p>
<pre data-role="codeBlock" data-info="" class="language-text"><code>PORT=5000
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/cipherstudio
JWT_SECRET=your_production_secret_key_here_minimum_32_chars
FRONTEND_URL=https://your-frontend-url.vercel.app
</code></pre><h4 id="step-4-deploy">Step 4: Deploy </h4>
<ul>
<li>Click <strong>Create Web Service</strong></li>
<li>Wait 5-10 minutes for deployment</li>
<li>Note your backend URL: <code>https://your-app.onrender.com</code></li>
</ul>
<hr>
<h3 id="frontend-deployment-vercel">Frontend Deployment (Vercel) </h3>
<h4 id="step-1-prepare-frontend">Step 1: Prepare Frontend </h4>
<ol>
<li>Update <code>.env</code>:<pre data-role="codeBlock" data-info="env" class="language-env env"><code>VITE_API_URL=https://your-backend.onrender.com
</code></pre></li>
<li>Commit changes</li>
<li>Push to GitHub</li>
</ol>
<h4 id="step-2-deploy-to-vercel">Step 2: Deploy to Vercel </h4>
<ol>
<li>Go to <a href="https://vercel.com/dashboard">Vercel Dashboard</a></li>
<li>Click <strong>Add New</strong> → <strong>Project</strong></li>
<li>Import your GitHub repository</li>
<li>Configure:
<ul>
<li><strong>Framework Preset:</strong> Vite</li>
<li><strong>Root Directory:</strong> <code>frontend/cipherStudio</code></li>
<li><strong>Build Command:</strong> <code>npm run build</code></li>
<li><strong>Output Directory:</strong> <code>dist</code></li>
</ul>
</li>
</ol>
<h4 id="step-3-set-environment-variables-1">Step 3: Set Environment Variables </h4>
<p>Add in Vercel:</p>
<pre data-role="codeBlock" data-info="" class="language-text"><code>VITE_API_URL=https://your-backend.onrender.com
</code></pre><h4 id="step-4-deploy-1">Step 4: Deploy </h4>
<ul>
<li>Click <strong>Deploy</strong></li>
<li>Wait 2-3 minutes</li>
<li>Your app will be live at: <code>https://your-app.vercel.app</code></li>
</ul>
<hr>
<h3 id="mongodb-setup-atlas">MongoDB Setup (Atlas) </h3>
<ol>
<li>Create account at <a href="https://www.mongodb.com/cloud/atlas">MongoDB Atlas</a></li>
<li>Create new cluster (free tier available)</li>
<li>Create database user</li>
<li>Whitelist IP: <code>0.0.0.0/0</code> (allow all)</li>
<li>Get connection string:<pre data-role="codeBlock" data-info="" class="language-text"><code>mongodb+srv://username:password@cluster.mongodb.net/cipherstudio?retryWrites=true&amp;w=majority
</code></pre></li>
<li>Add to backend environment variables</li>
</ol>
<hr>
<h2 id="usage-guide">Usage Guide </h2>
<h3 id="for-end-users">For End Users </h3>
<h4 id="1-register-account">1. Register Account </h4>
<ol>
<li>Click <strong>Login</strong> button</li>
<li>Click <strong>Sign Up</strong></li>
<li>Enter details:
<ul>
<li>First Name</li>
<li>Last Name</li>
<li>Email</li>
<li>Password (min 6 characters)</li>
</ul>
</li>
<li>Click <strong>Create Account</strong></li>
</ol>
<h4 id="2-create-project">2. Create Project </h4>
<ol>
<li>On homepage, click <strong>New Project</strong></li>
<li>Enter project name</li>
<li>Click <strong>Create</strong></li>
<li>Project created with default React files</li>
</ol>
<h4 id="3-edit-code">3. Edit Code </h4>
<ol>
<li>Click <strong>Open Editor</strong> on any project</li>
<li>See file list on top</li>
<li>Click file tabs to switch between files</li>
<li>Type code in left panel</li>
<li>See live preview in right panel</li>
<li>Click <strong>Save All</strong> to persist changes</li>
</ol>
<h4 id="4-add-new-file">4. Add New File </h4>
<ol>
<li>In editor, click <strong>+ New File</strong></li>
<li>Enter filename (e.g., <code>Button.jsx</code>)</li>
<li>Press Enter or click <strong>Create</strong></li>
<li>File appears in tabs and file list</li>
</ol>
<h4 id="5-delete-file">5. Delete File </h4>
<ol>
<li>In file list, click <strong>Delete</strong> next to filename</li>
<li>Confirm deletion</li>
</ol>
<h4 id="6-delete-project">6. Delete Project </h4>
<ol>
<li>On homepage, click <strong>Delete</strong> on project card</li>
<li>Confirm deletion</li>
<li>All project files deleted</li>
</ol>
<h4 id="7-logout">7. Logout </h4>
<ol>
<li>Click your name in navbar</li>
<li>Click <strong>Logout</strong></li>
<li>Redirected to homepage</li>
</ol>
<hr>
<h3 id="for-developers">For Developers </h3>
<h4 id="running-tests">Running Tests </h4>
<pre data-role="codeBlock" data-info="bash" class="language-bash bash"><code><span class="token comment"># Backend</span>
<span class="token builtin class-name">cd</span> backend/server
<span class="token function">npm</span> <span class="token builtin class-name">test</span>

<span class="token comment"># Frontend</span>
<span class="token builtin class-name">cd</span> frontend/cipherStudio
<span class="token function">npm</span> <span class="token builtin class-name">test</span>
</code></pre><h4 id="linting">Linting </h4>
<pre data-role="codeBlock" data-info="bash" class="language-bash bash"><code><span class="token comment"># Frontend</span>
<span class="token function">npm</span> run lint
</code></pre><h4 id="building-for-production">Building for Production </h4>
<pre data-role="codeBlock" data-info="bash" class="language-bash bash"><code><span class="token comment"># Frontend</span>
<span class="token function">npm</span> run build
<span class="token comment"># Creates optimized build in dist/</span>
</code></pre><hr>
<h2 id="troubleshooting">Troubleshooting </h2>
<h3 id="common-issues">Common Issues </h3>
<h4 id="1-mongodb-connection-failed">1. <strong>MongoDB Connection Failed</strong> </h4>
<p><strong>Error:</strong></p>
<pre data-role="codeBlock" data-info="" class="language-text"><code>MongooseServerSelectionError: connect ECONNREFUSED
</code></pre><p><strong>Solutions:</strong></p>
<ul>
<li>Check MongoDB is running: <code>mongod --version</code></li>
<li>Verify <code>MONGODB_URI</code> in <code>.env</code></li>
<li>For Atlas: check IP whitelist</li>
<li>For local: start MongoDB: <code>mongod</code></li>
</ul>
<hr>
<h4 id="2-jwt-token-invalid">2. <strong>JWT Token Invalid</strong> </h4>
<p><strong>Error:</strong></p>
<pre data-role="codeBlock" data-info="" class="language-text"><code>401 Unauthorized - Invalid token
</code></pre><p><strong>Solutions:</strong></p>
<ul>
<li>Check <code>JWT_SECRET</code> is set</li>
<li>Clear browser localStorage</li>
<li>Login again</li>
<li>Verify token hasn't expired (default 7 days)</li>
</ul>
<hr>
<h4 id="3-cors-error">3. <strong>CORS Error</strong> </h4>
<p><strong>Error:</strong></p>
<pre data-role="codeBlock" data-info="" class="language-text"><code>Access to XMLHttpRequest blocked by CORS policy
</code></pre><p><strong>Solutions:</strong></p>
<ul>
<li>Verify frontend URL in backend CORS config</li>
<li>Check <code>VITE_API_URL</code> in frontend <code>.env</code></li>
<li>Restart both servers</li>
<li>Clear browser cache</li>
</ul>
<hr>
<h4 id="4-file-save-failed">4. <strong>File Save Failed</strong> </h4>
<p><strong>Error:</strong></p>
<pre data-role="codeBlock" data-info="" class="language-text"><code>Failed to save files
</code></pre><p><strong>Solutions:</strong></p>
<ul>
<li>Check you're logged in</li>
<li>Verify project ownership</li>
<li>Check network tab for actual error</li>
<li>Ensure backend is running</li>
</ul>
<hr>
<h4 id="5-sandpack-not-loading">5. <strong>Sandpack Not Loading</strong> </h4>
<p><strong>Error:</strong></p>
<pre data-role="codeBlock" data-info="" class="language-text"><code>Preview shows blank screen
</code></pre><p><strong>Solutions:</strong></p>
<ul>
<li>Check browser console for errors</li>
<li>Verify file syntax is valid</li>
<li>Try refreshing preview</li>
<li>Check network for CDN blocks (adblockers)</li>
</ul>
<hr>
<h4 id="6-login-looplogout-on-refresh">6. <strong>Login Loop/Logout on Refresh</strong> </h4>
<p><strong>Solutions:</strong></p>
<ul>
<li>Clear browser localStorage</li>
<li>Check <code>VITE_API_URL</code> is correct</li>
<li>Verify <code>/api/auth/user</code> endpoint works</li>
<li>Check browser console for errors</li>
</ul>
<hr>
<h3 id="debug-checklist">Debug Checklist </h3>
<h4 id="backend-issues">Backend Issues </h4>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> MongoDB connected (check logs)</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> <code>.env</code> file exists with all variables</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Server running on correct port</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> CORS configured for frontend URL</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Routes registered in <code>app.js</code></li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> JWT_SECRET is set</li>
</ul>
<h4 id="frontend-issues">Frontend Issues </h4>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> <code>.env</code> file has <code>VITE_API_URL</code></li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Server running (check terminal)</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Check browser console for errors</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Check Network tab for failed requests</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> localStorage has token (if logged in)</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> CORS errors in console</li>
</ul>
<hr>
<h3 id="getting-help">Getting Help </h3>
<ol>
<li>
<p><strong>Check Logs</strong></p>
<ul>
<li>Backend: Terminal running <code>npm run dev</code></li>
<li>Frontend: Browser DevTools Console</li>
<li>Network: DevTools Network tab</li>
</ul>
</li>
<li>
<p><strong>Common Log Locations</strong></p>
<ul>
<li>Render: Dashboard → Logs tab</li>
<li>Vercel: Dashboard → Deployment → Build Logs</li>
</ul>
</li>
<li>
<p><strong>Report Issues</strong></p>
<ul>
<li>GitHub Issues: Include error message, steps to reproduce</li>
<li>Email: <a href="mailto:support@cipherstudio.com">support@cipherstudio.com</a></li>
</ul>
</li>
</ol>
<hr>
<h2 id="security-best-practices">Security Best Practices </h2>
<h3 id="backend-1">Backend </h3>
<ul>
<li>✅ Password hashing with bcrypt (10 rounds)</li>
<li>✅ JWT tokens with expiration</li>
<li>✅ Protected routes with middleware</li>
<li>✅ Input validation</li>
<li>✅ Error handling without exposing internals</li>
<li>✅ CORS restricted to known origins</li>
</ul>
<h3 id="frontend-1">Frontend </h3>
<ul>
<li>✅ XSS prevention (React escapes by default)</li>
<li>✅ Tokens in localStorage (consider httpOnly cookies for production)</li>
<li>✅ No sensitive data in client code</li>
<li>✅ HTTPS in production</li>
</ul>
<h3 id="recommendations">Recommendations </h3>
<ul>
<li>Use environment-specific secrets</li>
<li>Rotate JWT secrets periodically</li>
<li>Implement rate limiting</li>
<li>Add request logging</li>
<li>Use HTTPS everywhere</li>
<li>Validate all user input</li>
<li>Sanitize file uploads</li>
</ul>
<hr>
<h2 id="performance-optimization">Performance Optimization </h2>
<h3 id="backend-2">Backend </h3>
<ul>
<li>Add database indexing</li>
<li>Implement caching (Redis)</li>
<li>Compress responses</li>
<li>Optimize queries</li>
<li>Use connection pooling</li>
</ul>
<h3 id="frontend-2">Frontend </h3>
<ul>
<li>Code splitting</li>
<li>Lazy loading routes</li>
<li>Optimize images</li>
<li>Use production build</li>
<li>CDN for static assets</li>
<li>Memoize expensive operations</li>
</ul>
<hr>
<h2 id="future-enhancements">Future Enhancements </h2>
<h3 id="planned-features">Planned Features </h3>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Real-time collaboration (WebSockets)</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Code sharing via unique links</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Terminal integration</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Git integration</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Export projects as ZIP</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Theme customization</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Dark/Light mode</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Code snippets library</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Folder upload</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Search functionality</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Code formatting (Prettier)</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Multiple file upload</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Project templates</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox"> Deployment integration</li>
</ul>
<hr>
<h2 id="acknowledgments">Acknowledgments </h2>
<ul>
<li><a href="https://sandpack.codesandbox.io/">Sandpack</a> - Live code editor</li>
<li><a href="https://www.mongodb.com/">MongoDB</a> - Database</li>
<li><a href="https://react.dev/">React</a> - UI Library</li>
<li><a href="https://expressjs.com/">Express</a> - Backend framework</li>
<li><a href="https://vitejs.dev/">Vite</a> - Build tool</li>
</ul>
</div>
      </div>
      
      
    
    
    
    
    
    
  
    </body></html>

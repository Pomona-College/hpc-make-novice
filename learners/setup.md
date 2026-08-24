---
title: Setup
---

## Running on Sagehen (recommended at Pomona)

This workshop runs equally well on a personal laptop or on Sagehen, Pomona College's research computing cluster. To use Sagehen:

1. Sign in at [https://ondemand.hpc.pomona.edu](https://ondemand.hpc.pomona.edu) using your Pomona credentials and DUO MFA at [https://duo.pomona.edu](https://duo.pomona.edu).
2. Open **Clusters > Sagehen Shell Access** for a browser-based bash terminal.
3. `make` is available on every Sagehen node, so you can build and re-run pipelines directly on the cluster — including from inside a SLURM batch job.
4. Cecil Sagehen's lab teammates often keep their pipelines under `/bigdata/lab/<labname>/pipelines/` so the Makefile and its outputs are versioned alongside the data.

## Files

You need to download some files to follow this lesson:

1. Download [make-lesson.zip][zip-file].

2. Move `make-lesson.zip` into a directory which you can access via your bash shell.

3. Open a Bash shell window.

4. Navigate to the directory where you downloaded the file.

5. Unpack `make-lesson.zip`:
  
  ```source
  $ unzip make-lesson.zip
  ```

6. Change into the `make-lesson` directory:
  
  ```source
  $ cd make-lesson
  ```

## Software

You also need to have the following software installed on your computer to
follow this lesson:

### GNU Make

#### Linux

Make is a standard tool on most Linux systems and should already be available.
Check if you already have Make installed by typing `make -v` into a terminal.

One exception is Debian, and you should install Make from the terminal using
`sudo apt-get install make`.

#### OSX

You will need to have Xcode installed (download from the
[Apple website](https://developer.apple.com/xcode/)).
Check if you already have Make installed by typing `make -v` into a terminal.

#### Windows

Use the Software Carpentry
[Windows installer](https://github.com/swcarpentry/windows-installer).

### Python

Python2 or Python3, Numpy and Matplotlib are required.
They can be installed separately, but the easiest approach is to install
[Anaconda](https://www.anaconda.com/distribution/) which includes all of the
necessary python software.

[zip-file]: files/make-lesson.zip

<!-- highlight <labname>/<myusername> placeholders in code blocks; remove if the varnish theme handles this natively -->
<script>(function(){var CSS='.sh-placeholder{color:#c2410c;font-weight:700}[data-bs-theme="dark"] .sh-placeholder,html.dark .sh-placeholder{color:#fdba74}@media (prefers-color-scheme: dark){[data-bs-theme="auto"] .sh-placeholder{color:#fdba74}}';var RX=/<labname>|<myusername>/g;function firstMatch(el){var w=document.createTreeWalker(el,NodeFilter.SHOW_TEXT,null),nodes=[],full='';while(w.nextNode()){nodes.push({n:w.currentNode,s:full.length});full+=w.currentNode.nodeValue;}RX.lastIndex=0;var m;while((m=RX.exec(full))){var s=m.index,e=s+m[0].length,inSpan=false,parts=[];for(var j=0;j<nodes.length;j++){var ns=nodes[j].s,ne=ns+nodes[j].n.nodeValue.length;if(ne<=s||ns>=e)continue;parts.push({node:nodes[j].n,a:Math.max(s-ns,0),b:Math.min(e-ns,nodes[j].n.nodeValue.length)});var p=nodes[j].n.parentNode;while(p&&p!==el){if(p.classList&&p.classList.contains('sh-placeholder')){inSpan=true;break;}p=p.parentNode;}}if(!inSpan&&parts.length)return parts;}return null;}function wrapParts(parts){for(var i=parts.length-1;i>=0;i--){var t=parts[i].node,txt=t.nodeValue,a=parts[i].a,b=parts[i].b;var span=document.createElement('span');span.className='sh-placeholder';span.textContent=txt.slice(a,b);var f=document.createDocumentFragment();if(a>0)f.appendChild(document.createTextNode(txt.slice(0,a)));f.appendChild(span);if(b<txt.length)f.appendChild(document.createTextNode(txt.slice(b)));t.parentNode.replaceChild(f,t);}}function run(){var st=document.createElement('style');st.textContent=CSS;document.head.appendChild(st);document.querySelectorAll('pre,code').forEach(function(el){var guard=0,parts;while((parts=firstMatch(el))&&guard++<500){wrapParts(parts);}});}if(document.readyState==='loading'){document.addEventListener('DOMContentLoaded',run);}else{run();}})();</script>

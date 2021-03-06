<!DOCTYPE html>
<html class="js no-mobile desktop no-ie chrome chrome66 creating-accessible-react-apps-talk-section gradient rgba opacity textshadow multiplebgs boxshadow borderimage borderradius cssreflections csstransforms csstransitions no-touch retina fontface domloaded no-title-footer w-1440 gt-240 gt-320 gt-480 gt-640 gt-768 gt-800 gt-1024 gt-1280 lt-1680 lt-1920 no-portrait landscape" id="index-page"><script type="text/javascript" src="chrome-extension://eoknmaajkanapojcdeccofmeimpddoim/xhr_overload.js"></script><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
  
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">

  <title>Creating Accessible React Apps</title>

  <link rel="stylesheet" href="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/reveal.css">
  <link rel="stylesheet" href="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/a11y-react.css">
  <link rel="icon" sizes="120x120" href="https://svinkle.github.io/creating-accessible-react-apps-talk/images/mobile-phone.png">

  <!-- Theme used for syntax highlighting of code -->
  <link rel="stylesheet" href="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/prism.css">

  <!-- Plugins -->
  <link rel="stylesheet" href="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/helper.css">
  <link rel="stylesheet" href="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/title-footer.css">

  <!-- Printing and PDF exports -->
  <script>
  var link = document.createElement('link');
link.rel = 'stylesheet';
link.type = 'text/css';
link.href = window.location.search.match(/print-pdf/gi)
  ? 'css/print/pdf.css'
  : 'css/print/paper.css';
document.getElementsByTagName('head')[0].appendChild(link);
</script><link rel="stylesheet" type="text/css" href="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/paper.css"><script type="text/javascript" src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/marked.js"></script><script type="text/javascript" src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/markdown.js"></script><script type="text/javascript" src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/notes.js"></script><script type="text/javascript" src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/helper.js"></script><script type="text/javascript" src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/title-footer.js"></script>
</head>

<body data-gr-c-s-loaded="true">
  <div class="reveal slide center ready" role="application" data-transition-speed="default" data-background-transition="fade">
    <a id="global-skip-link" href="https://svinkle.github.io/creating-accessible-react-apps-talk/#table-of-contents">Show navigation</a><div class="slides" style="width: 960px; height: 700px; zoom: 1.03543;">
      <section data-state="no-title-footer" class="present" style="top: 32.5px; display: block;" data-id="0"><div class="accessibilityWrapper" tabindex="-1">
        <h1 class="logo logo-font">Creating Accessible React Apps</h1>
       


        <div class="intro-slide">
          <ul class="list-of-links-without-an-underline-cause-i-feel-like-it">
            <li>
              <a href="https://svinkle.me/">Balram Singh</a> • <a href="https://twitter.com/erbalramsingh">@erbalramsingh</a>
            </li>
           
          </ul>
        </div> 


      </div></section>
      <section class="stack future" style="top: 0px; display: block;" data-previous-indexv="0" hidden="" aria-hidden="true">
        <section data-id="1/0" class="past" style="top: 330px; display: block;" hidden="" aria-hidden="true"><div class="accessibilityWrapper" tabindex="-1">
          <h2>Can React apps be accessible? <span role="img" aria-label="">🤔</span></h2>
          <aside class="notes">
            <p><strong>Can React apps be accessible?</strong></p>
            <p>It seems like there's sometimes a <em>bit</em> of reserve or hesitation when considering building an app with newer technology like React.</p>
            <p>Often times folks may feel like these types of apps are difficult or perhaps impossible to be made accessible by their very nature of relying so heavily on JavaScript.</p>
            <p>Also, what I mean when I say "accessible" I don't mean making react "available" to developers, but rather making sure your React based apps are usable by people with disabilities who rely on assistive technology such as a screen reader.</p>
            <p>Well, to answer this question…</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="" style="top: 330px; display: block;" data-id="1/1" aria-hidden="true"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Yes! <span role="img" aria-label="">🎉</span></h3>
          <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/yes.webp" width="480" height="360" alt="Children from Charlie Brown cartoon celebrating as baloons fall from the ceiling.">
          <p>Continue on to find out how…</p>
          <aside class="notes">
            <p>Yes, React apps can <em>absolutely</em> be made to be accessible for people with disabilities!</p>
            <p>So today I'm here to share some tips that I found to help with this.</p>
            <span role="img" aria-label="">👉</span>
          </aside>
        </div></section>
      </section>
      <section class="future" style="top: 330px; display: block;" data-id="2" hidden="" aria-hidden="true"><div class="accessibilityWrapper" tabindex="-1">
        <h2>Agenda <span role="img" aria-label="">✅</span></h2>
        <ol>
          <li>Notes on getting started</li>
          <li>Setting the page <code>title</code></li>
          <li>Live announcements</li>
          <li>Focus management</li>
          <li>React's accessibility linter</li>
          <li>Using <code>React.Fragment</code></li>
          <li>Writing semantic HTML</li>
        </ol>
        <aside class="notes">
          <p>For the agenda…</p>
          <ol>
            <li>I'll start with a few, high-level notes when first getting started with creating Reat apps</li>
            <li>We'll look at how to set the page <code>title</code></li>
            <li>We'll review how to create a live announcements component</li>
            <li>We'll explore how to manage keyboard focus <em>between</em> components and when loading new pages</li>
            <li>We'll take a brief look at React's accessibility linter which comes with each new app</li>
            <li>We'll spotlight a new feature with React <code>Fragment</code>s</li>
            <li>I'll share some thoughts on writing semantic HTML within React components</li>
            <li>And at the end I'll go through a small demo app I created to help illustrate each point</li>
          </ol>
          <span role="img" aria-label="">👉</span>
        </aside>
      </div></section>
      <section hidden="" aria-hidden="true" class="stack future" style="top: 0px; display: none;" data-previous-indexv="0">
        <section data-id="3/0" style="top: 330px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h2>Notes on getting started <span role="img" aria-label="">📓</span></h2>
          <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/notes.webp" width="480" height="286" alt="Ryan Howard from The Office, looking rather annoyed, writes in a notebook.">
          <aside class="notes">
            <p>A few things to watch for when first starting to develop with React.</p>
            <p>These took me a little by surprise at first, but it wasn't too long before I got used to it.</p>
            <p>And if you do make a mistake and write something incorrectly, you'll get a friendly warning in your browser devtools console with tips on how to fix the issue.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="3/1" style="top: 330px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>camelCase</h3>
          <p>Write attributes in camelCase <span role="img" aria-label="">🐪</span></p>
          <ul>
            <li><code>tabindex</code> <span role="img" aria-label="needs to be written as">👉</span> <code>tabIndex</code></li>
            <li><code>contenteditable</code> <span role="img" aria-label="needs to be written as">👉</span> <code>contentEditable</code></li>
            <li><code>maxlength</code> <span role="img" aria-label="needs to be written as">👉</span> <code>maxLength</code></li>
          </ul>
          <p>(<code>aria-*</code> and <code>data-*</code> are exempt from this.)</p>
          <aside class="notes">
            <p>When it comes to writing HTML attributes in React components, they need to be written in <code>camelCase</code> style.</p>
            <p>This means that when an attribute name is made up of two words, the second word in the attribute must start with a capital letter.</p>
            <p>So for example…</p>
            <ol>
              <li>The attribute <code>tabindex</code> needs to be written as <code>tabIndex</code> with a capital 'I'.</li>
              <li>The attribute <code>contenteditable</code> needs to be written as <code>contentEditable</code> with a capital 'E'.</li>
              <li>And the last example, the attribute <code>maxlength</code> needs to be written as <code>maxLength</code> with a capital 'L'.</li>
            </ol>
            <p>Note that <code>aria</code> and <code>data</code> attributes are exempt from this rule.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="3/2" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Reserved words</h3>
          <p>When HTML conflicts with JS <span role="img" aria-label="">😕</span></p>
          <ul>
            <li><code>for</code> <span role="img" aria-label="needs to be written as">👉</span> <code>htmlFor</code></li>
            <li><code>class</code> <span role="img" aria-label="needs to be written as">👉</span> <code>className</code></li>
          </ul>
          <aside class="notes">
            <p>There are a few reserved word conflicts when writing HTML attributes in React components.</p>
            <p>For example…</p>
            <ol>
              <li>The reserved word <code>for</code> is used in HTML when pairing a <code>label</code> with an <code>input</code> element. In JavaScript, <code>for</code> is used to loop through items using an index until a specified condition evaluates to <code>false</code>. So, the <code>for</code> attribute needs to be written as <code>htmlFor</code>.</li>
              <li>Another example, the reserved word <code>class</code> is used in HTML to allow CSS and JavaScript to select and access specific elements via the <code>class</code> selector. In JavaScript, it's used to create a <code>class</code> declaration. So when adding a <code>class</code> to an element, this needs to be written as <code>className</code>.</li>
            </ol>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="3/3" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Self closing elements require <code aria-label="a closing slash">/</code></h3>
          <ul>
            <li><code class=" language-markup"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>…<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span></code> <span role="img" aria-label="needs to be written as">👉</span> <code class=" language-markup"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>…<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span></code></li>
            <li><code class=" language-markup"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>meta</span> <span class="token attr-name">charset</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>utf-8<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span></code> <span role="img" aria-label="needs to be written as">👉</span> <code class=" language-markup"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>meta</span> <span class="token attr-name">charset</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>utf-8<span class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span></code></li>
            <li><code class=" language-markup"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span></code> <span role="img" aria-label="needs to be written as">👉</span> <code class=" language-markup"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span></code></li>
          </ul>
          <aside class="notes">
            <p>In HTML5 there are a few elements which do not feature a closing tag.</p>
            <p>Just like back in the old XHTML days, JSX (which is a sub-set of JavaScript used to write React components) requires self closing elements to have the forward slash.</p>
            <p>For example, HTML elements such as <code>img</code>, <code>meta</code>, and <code>input</code> all require a closing forward slash.</p>
            <span role="img" aria-label="">👉</span>
          </aside>
        </div></section>
      </section>
      <section hidden="" aria-hidden="true" class="stack future" style="top: 0px; display: none;" data-previous-indexv="0">
        <section data-id="4/0" style="top: 330px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h2>Setting the page <code>title</code> <span role="img" aria-label="">📰</span></h2>
          <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/page-title.webp" width="480" height="341" alt="Homer Simpsons&#39;s web page, featuring many animated gifs and a dancing Jesus.">
          <aside class="notes">
            <p>Now, let's take a look at how to set the page <code>title</code> and why doing so is so critical to accessibility of your app.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="4/1" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>The problem… <span role="img" aria-label="">🤔</span></h3>
          <p>When someone using a <strong>screen reader</strong> loads a new page, the initial page announcement is always the same.</p>
          <aside class="notes">
            <p>So, here's the problem. When someone using a <strong>screen reader</strong> loads a new page, the initial page announcement is always the same. Why?</p>
            <p>Typically with a Single Page App, the page <code>title</code> element in the <code>head</code> section of the document remains static. This is a problem for other folks, too, as we'll see.</p>
            <p>So, we overcome this issue by setting a unique page <code>title</code>, but does anyone know any other benifits to doing this?</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="4/2" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Set the page <code>title</code>! <span role="img" aria-label="">👍</span></h3>
          <ul>
            <li>Updates the browser tab for sighted users</li>
            <li>Helps with Search Engine Optimization</li>
            <li>Often the first content announced by screen readers</li>
          </ul>
          <aside class="notes">
            <p>By setting the page <code>title</code> we benifit in a few ways:</p>
            <ol>
              <li>It updates the content in the browser tab, so sighted users have a better understanding of where they are in the app, specifically when deep-linking</li>
              <li>It helps to increase Search Engine Optimization when something like Google goes through and indexes your app content</li>
              <li>And the page <code>title</code> content is often the first bit of information announced by screen readers, so users of assistive technology will have a better understanding of their current place within the app</li>
            </ol>
            <p>So, how do we do this in React?</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="4/3" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Use <code>document.title</code></h3>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token function">componentDidMount</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  document<span class="token punctuation">.</span>title <span class="token operator">=</span> <span class="token string">'My page title'</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
          <ul>
            <li>Not specific to React</li>
            <li><a href="https://developer.mozilla.org/en-US/docs/Web/API/Document/title">More on MDN</a></li>
          </ul>
          <aside class="notes">
            <p>The simplest method I found to set the <code>title</code> is by using the JavaScript <code>document.title</code> global property.</p>
            <p>On the screen here is a function called "component did mount." This is a React lifecycle method. The code within this function executes when the component is loaded onto the screen.</p>
            <p>The single line within this function is using <code>document.title</code> to set a string value of, "My page title." So when this components loads, the page <code>title</code> will be set to this value.</p>
            <p>It's also worth noting this is not specific or unique to React; this method can be used in any JavaScript based application or web site.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="4/4" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Other existing components</h3>
          <ul>
            <li>
              <a href="https://npmjs.com/package/react-document-title">react-document-title</a>
              <pre class=" language-jsx"><code class=" language-jsx"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>DocumentTitle</span> <span class="token attr-name">title</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>My page title<span class="token punctuation">'</span></span><span class="token punctuation">&gt;</span></span>
  <span class="token operator">&lt;</span><span class="token operator">!</span><span class="token operator">--</span> content <span class="token operator">--</span><span class="token operator">&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>DocumentTitle</span><span class="token punctuation">&gt;</span></span></code></pre>
            </li>
            <li>
              <a href="https://npmjs.com/package/react-helmet">react-helmet</a>
              <pre class=" language-jsx"><code class=" language-jsx"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>Helmet</span><span class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>meta</span> <span class="token attr-name">charSet</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>utf-8<span class="token punctuation">'</span></span> <span class="token punctuation">/&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>My page title<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>link</span> <span class="token attr-name">rel</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>stylesheet<span class="token punctuation">'</span></span> 
<span class="token attr-name">href</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>css/page-specific.css<span class="token punctuation">'</span></span> <span class="token punctuation">/&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>Helmet</span><span class="token punctuation">&gt;</span></span></code></pre>
            </li>
          </ul>
          <aside class="notes">
            <p>I felt like it would be worth mentioning that there are other, pre-existing components that other developers have made for setting the title. These components can be included in your project via <code>npm</code>.</p>
            <p>For example…</p>
            <ol>
              <li>The first one called <code>react-document-title</code> can be used by wrapping your content with a <code>DocumentTitle</code> component. Then, add a <code>title</code> prop and set its value to the desired page title.</li>
              <li>The other one here called <code>react-helmet</code> is used by creating a <code>Helmet</code> component. Within this you can set anything you'd like that would normally appear in the <code>head</code> section of a page. For example, setting the character set, the page <code>title</code> text, or even including page specific CSS document.</li>
            </ol>
            <span role="img" aria-label="">👉</span>
          </aside>
        </div></section>
      </section>
      <section hidden="" aria-hidden="true" class="stack future" style="top: 350px; display: none;" data-previous-indexv="0">
        <section data-id="5/0" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h2>Live announcements <span role="img" aria-label="">📢</span></h2>
          <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/announcement.gif" width="480" height="480" alt="A man using a megaphone. For some reason, a hamburger is seen coming from his mouth, going through the megaphone, and out comes an even larger hamburger.">
          <aside class="notes">
            <p>Now let's take a look at a complete, live announcements component.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="5/1" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>The problem… <span role="img" aria-label="">🤔</span></h3>
          <p>When a Single Page App fetches data, the new content is visibly displayed.</p>
          <p>However, screen reader users recieve no indication of the available content.</p>
          <aside class="notes">
            <p>Sometimes when you're working with a single page app, it's common that you would request data from an external data source.</p>
            <p>When the data is output to the user interface, sighted users can see that content is now available and ready for consumption.</p>
            <p>For people who rely on assistive technology, however, they might be unaware that anything's taken place. So, it's a good idea to announce when and if the data request was successful or not, and if successful, how many items are now on displayed the screen as a result.</p>
            <p>Can anyone think of any other situation or user experience when a live announcement would be ideal?</p>
            <ul>
              <li>Loading state</li>
              <li>Search result state</li>
              <li>Perhaps a dyamic form submission on success/error</li>
            </ul>
            <p>How do we overcome this issue?</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="5/2" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Create a Live <code>Announcements</code> component <span role="img" aria-label="">👍</span></h3>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token keyword">import</span> React <span class="token keyword">from</span> <span class="token string">'react'</span><span class="token punctuation">;</span>

<span class="token keyword">class</span> <span class="token class-name">Announcements</span> <span class="token keyword">extends</span> <span class="token class-name">React<span class="token punctuation">.</span>Component</span> <span class="token punctuation">{</span>
  <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">aria-live</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>polite<span class="token punctuation">"</span></span> <span class="token attr-name">aria-atomic</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>true<span class="token punctuation">"</span></span> 
<span class="token attr-name">className</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>visuallyhidden<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>message<span class="token punctuation">}</span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>

<span class="token keyword">export</span> <span class="token keyword">default</span> Announcements<span class="token punctuation">;</span></code></pre>
          <aside class="notes">
            <p>Let's create a live announcements component which will help announce new app state.</p>
            <p>Here we have the Announcements component in its entirety.</p>
            <ol>
              <li>First thing is to import React from React</li>
              <li>Then we create the class definition with, <code>class Announcements extends React.Component</code></li>
              <li>Within the class we have a single <code>render</code> method with a <code>return</code> statement. This simply returns a <code>div</code> element.</li>
              <li>The <code>div</code> element features the <code>aria-live</code> attribute with the value of "polite" which means assistive technology will wait until other messages are finished being announced and then this content will be read aloud.</li>
              <li>The <code>div</code> also features the <code>aria-atomic</code> attribute which ensures all content, not just updated or changed content, will be announced.</li>
              <li>Within the <code>div</code> is the line, <code>this.props.message</code> wrapped in curly braces. This will output the message text when it's passed to the Announcements component here.</li>
              <li>Finally, we <code>export</code> the Announcements component so it can be used elsewhere in the app.</li>
            </ol>
            <p>Now that we have the component writen and available, how do we use it?</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="5/3" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Usage, part 1</h3>
          <p>Create a <code>state</code> property</p>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token keyword">this</span><span class="token punctuation">.</span>state <span class="token operator">=</span> <span class="token punctuation">{</span>
  message<span class="token punctuation">:</span> <span class="token keyword">null</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span></code></pre>
          <aside class="notes">
            <p>To start, in a parent component which will call the Announcements component, we'll create a new <code>state</code> property.</p>
            <p>We'll call this property, <code>message</code>, and set its value to <code>null</code> for now.</p>
            <p>So, on the screen there's a <code>this.state</code> object declaration, and inside the object is a property called, <code>message</code> with its default value set to <code>null</code>.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="5/4" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Usage, part 2</h3>
          <p>Set the <code>state</code> property</p>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  message<span class="token punctuation">:</span> <span class="token string">'Some message about the current state'</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span></code></pre>
          <aside class="notes">
            <p>Next, at the point in your app when you recieve your data, either successfully or if things didn't work out as expected, we'll set the content of the <code>message</code> property.</p>
            <p>To do so, you call the <code>this.setState</code> function and pass in an <code>object</code> parameter.</p>
            <p>This object will feature the <code>message</code> property we created earlier, with its value set to the string of text we want to announce.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="5/5" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Usage, part 3</h3>
          <p>Send message to <code>&lt;Announcements /&gt;</code> component</p>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>Announcements</span> <span class="token attr-name">message</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>message<span class="token punctuation">}</span></span> <span class="token punctuation">/&gt;</span></span></code></pre>
          <aside class="notes">
            <p>Lastly, we'll include the Announcements component within the parent component.</p>
            <p>In order to send it the message text from state to the Announcements component, we use a prop.</p>
            <p>The prop on the screen here is called, <code>message</code> with its value being set to <code>this.state.message</code>.</p>
            <p>So when this component loads, the message will be announced by a screen reader and the person using the app will be informed of the current state message.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="5/6" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Other existing components</h3>
          <ul>
            <li>
              <a href="https://npmjs.com/package/react-aria-live">react-aria-live</a>
              <pre class=" language-jsx"><code class=" language-jsx"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>LiveAnnouncer</span><span class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>LiveMessage</span> <span class="token attr-name">message</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>a11yMessage<span class="token punctuation">}</span></span> 
<span class="token attr-name">aria-live</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>polite<span class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span>
  <span class="token operator">&lt;</span>button onClick<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState</span><span class="token punctuation">(</span><span class="token punctuation">{</span> 
a11yMessage<span class="token punctuation">:</span> <span class="token string">'Button Pressed'</span> <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
    Press me
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>LiveAnnouncer</span><span class="token punctuation">&gt;</span></span></code></pre>
            </li>
            <li>
              <a href="https://npmjs.com/package/react-a11y-announcer">react-a11y-announcer</a>
              <br>(Literally the same thing I described earlier)
            </li>
          </ul>
          <aside class="notes">
            <p>Like with setting the page <code>title</code>, there are other existing components for creating live regions.</p>
            <p>For example…</p>
            <ol>
              <li>This one called <code>react-aria-live</code> requires a LiveAnnouncer component to be added to your template. Then within this there's a LiveMessage component which takes the same <code>message</code> prop as described before, along with the <code>aria-live</code> attribute. Also within the LiveAnnouncer component is your content that would be dynamically updated based on some event.</li>
              <li>The other component I found called <code>react-a11y-announcer</code> is literally the same thing that I came up with which I described ealier.</li>
            </ol>
            <p>So, those are both available for you to check out.</p>
            <span role="img" aria-label="">👉</span>
          </aside>
        </div></section>
      </section>
      <section hidden="" aria-hidden="true" class="stack future" style="top: 350px; display: none;" data-previous-indexv="0">
        <section data-id="6/0" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h2>Focus management <span role="img" aria-label="">☕️</span></h2>
          <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/focus-1.gif" width="480" height="360" alt="Bill Lumber, from Office Space, standing, arm resting on an office cubicle wall, slowley sipping coffee.">
          <aside class="notes">
            <p>Moving on now to the concept of focus management.</p>
            <p>Well planned focus management is critical in creating a successful and comfortable user experience, especially for highly dynamic or single page apps.</p>
            <p>What I mean by focus management is moving the <em>keyboard cursor</em> from one place in the app to another in order to assist the person on the other side of the screen in moving along with the intended flow of the app in order to complete their task.</p>
            <p>Let's take a look at a couple examples.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="6/1" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>The problem… <span role="img" aria-label="">🤔</span></h3>
          <p>A loading screen in our app displays a message in-between fetching new data. Sighted users can read the message a wait patiently… <em>probably</em>.</p>
          <p>However, screen reader users do not recieve this message conveying the current app state. They might get discouraged or blame themselves when something takes a long time to load.</p>
          <aside class="notes">
            <p>So, in the example scenario here, the app we're working with has a loading screen which displays in-between fetching data.</p>
            <p>When this screen appears, sighter users can read the message just fine and wait for the next screen to load.</p>
            <p>However, screen reader users are not made aware of the current state which might be a bit frustrating or concerning if the app takes a while to fetch data. They could start to wonder if the app is broken or even blame themselves that they did somthing incorrectly.</p>
            <p>How to make sure the loading message is shared with everyone using the app?</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="6/2" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Focus management! <span role="img" aria-label="">👍</span></h3>
          <p>Let's shift focus to the Loading message container when it gets displayed.</p>
          <aside class="notes">
            <p>One way to fix the issue is focus management! Let's send the keyboard focus to the Loading message container in order for someone using assistive technology to also recieve the message.</p>
            <p>How do we actually manage focus in a react app?</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="6/3" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Selecting an element</h3>
          <p>Kind of like jQuery. <span role="img" aria-label="">🤷‍♂️</span></p>
          <pre class=" language-js"><code class=" language-js"><span class="token keyword">var</span> loadingMessage <span class="token operator">=</span> <span class="token function">$</span><span class="token punctuation">(</span><span class="token string">'#loadingMessage'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token comment">// …</span>
loadingMessage<span class="token punctuation">.</span><span class="token function">focus</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span></code></pre>
          <aside class="notes">
            <p>Well, it can be helpful to think about how you might be used to selecting an element with something like jQuery.</p>
            <p>On the screen is an example of the jQuery dollar selector, caching a reference to the "loading message" element in a variable called <code>loadingMessage</code>.</p>
            <p>Somewhere else in this app, we could use the variable and call its <code>focus</code> method to set the keyboard cursor directly onto this element.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="6/4" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>The React way</h3>
          <p>Use a function <code>ref</code> to reference the element elsewhere in the component.</p>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token operator">&lt;</span>div
  ref<span class="token operator">=</span><span class="token punctuation">{</span>
    <span class="token punctuation">(</span>loadingMessage<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span>
      <span class="token keyword">this</span><span class="token punctuation">.</span>loadingMessage <span class="token operator">=</span> loadingMessage<span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
  tabIndex<span class="token operator">=</span><span class="token string">'-1'</span>
  <span class="token operator">&gt;</span>
  Loading…
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span></code></pre>
          <aside class="notes">
            <p>In React, the concept's <em>pretty</em> much the same, but how we arrive there is a little different.</p>
            <p>In order to select an element, "the react way," we create what's called a "function ref," or, <code>ref</code> for short.</p>
            <p>The <code>ref</code> is a prop that is set on the element we want to reference elsewhere in the component. It allows us to select and reference, in React, an actual DOM node on the page.</p>
            <p>So as an example…</p>
            <ol>
              <li>What's on the screen here is a plain <code>div</code> element. Within the <code>div</code> is the phrase, "loading." This is meant to be displayed when the app is in a loading state.</li>
              <li>The <code>div</code> features a prop called <code>ref</code>, and this <code>ref</code> is being assigned a regular, ES6 style function.</li>
              <li>The function is being passed a parameter called <code>loadingMessage</code>. And within the function is a single assignment statement of, <code>this.loadingMessage</code> equals <code>loadingMessage</code>.</li>
              <li>This sets the <code>ref</code> of the <code>div</code> to the class property <code>this.loadingMessage</code>.</li>
            </ol>
            <p>Now that we have the <code>ref</code> setup, how do we use it?</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="6/5" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Using the <code>ref</code>…</h3>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token function">componentDidMount</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">this</span><span class="token punctuation">.</span>loadingMessage<span class="token punctuation">.</span><span class="token function">focus</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
          <aside class="notes">
            <p>In order to use the <code>ref</code>, we can use the "component did mount" lifecycle method again, and then call the <code>focus</code> method on the <code>ref</code> element.</p>
            <p>On the screen here is the <code>componentDidMount</code> method. Within this is a single line which reads, <code>this.loadingMessage.focus</code>.</p>
            <p>When this component loads, the keyboard focus indicator will be automatically sent to this element which will then announce it's text content, <em>"loading"</em>.</p>
            <span role="img" aria-label="">👉</span>
          </aside>
        </div></section>
      </section>
      <section hidden="" aria-hidden="true" class="stack future" style="top: 350px; display: none;" data-previous-indexv="0">
        <section data-id="7/0" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h2>More focus management! <span role="img" aria-label="">🐶</span></h2>
          <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/focus-2.gif" width="480" height="308" alt="A pair of adorable pug puppies running on green grass.">
          <aside class="notes">
            <p>Another important example of focus management is adjusting keybord focus when moving from page to page in React.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="7/1" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>The problem… <span role="img" aria-label="">🤔</span></h3>
          <p>When using React Router's <code>&lt;Link /&gt;</code> component, the browser never <em>actually</em> reloads, leaving the user's focus state in an unknown position.</p>
          <aside class="notes">
            <p>So, why exactly do we need do manage focus when loading a new page?</p>
            <p>When using React Router's Link component, new pages are inserted into React's Virtual DOM without reloading the browser. As a result, pages are precieved to load very quickly, it's sort of React's claim to fame.</p>
            <p>However, people who depend on assistive technology, such as a screen reader, have to search around the page to find what changed when activating the link.</p>
            <p>How do we overcome this issue?</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="7/2" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Our new friend, <code>ref</code></h3>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token operator">&lt;</span>div
  ref<span class="token operator">=</span><span class="token punctuation">{</span>
    <span class="token punctuation">(</span>contentContainer<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span>
      <span class="token keyword">this</span><span class="token punctuation">.</span>contentContainer <span class="token operator">=</span> contentContainer<span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
  tabIndex<span class="token operator">=</span><span class="token string">"-1"</span>
  aria<span class="token operator">-</span>labelledby<span class="token operator">=</span><span class="token string">"pageHeading"</span>
  <span class="token operator">&gt;</span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>Header</span> <span class="token punctuation">/&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>pageHeading<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>…<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
      <span class="token comment">// Content components…</span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>Footer</span> <span class="token punctuation">/&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span></code></pre>
          <aside class="notes">
            <p>Coming back to the "ref" concept, one path we can take to resolve this is to create a <code>ref</code> on the outer-most container element and use that <code>ref</code> to shift focus to the "page."</p>
            <p>The idea is when a new page loads into view, focus is sent to the top of the page. From there, the user can navigate forward from this point, discovering content in the same manner as if a full page reload had taken place.</p>
            <p>So, for this example that's on the screen…</p>
            <ol>
              <li>There's a wrapper <code>div</code> element which holds all of the page content, including the <code>header</code>, <code>footer</code>, etc.</li>
              <li>On the <code>div</code> there's a <code>ref</code> with is function assignment. With this function we're passing in the parameter <code>contentContainer</code> and assigning it to the class property, <code>this.contentContainer</code>.</li>
              <li>Also on the <code>div</code> is a <code>tabindex</code> attribute with its value set to <code>-1</code>. This ensures that the <code>div</code> will be able to programatically receive focus, but not be added to the natural focus order.</li>
              <li>The other attribute on the <code>div</code> is <code>aria-labelledby</code> with its value set to the <code>id</code> of the page heading. This helps to give extra context of where the user curently is by announcing the page heading content when the <code>div</code> receives focus.</li>
            </ol>
            <p>So, how do we use the "ref?"</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="7/3" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Set "page" focus via <code>ref</code></h3>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token function">componentDidMount</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">this</span><span class="token punctuation">.</span>contentContainer<span class="token punctuation">.</span><span class="token function">focus</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
          <aside class="notes">
            <aside class="notes">
              <p>Again, we can use the <code>ref</code> within the "component did mount" lifecycle method, and then call the <code>focus</code> method on the <code>ref</code> class property.</p>
              <p>To reiterate, when the "page" loads, the keyboard focus indicator will be sent to the container <code>div</code> element and the user can continue on with content discovery from this point.</p>
              <span role="img" aria-label="">👉</span>
            </aside>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="7/4" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3><span role="img" aria-label="">🔥</span> New <code>ref</code> syntax</h3>
          <p>React <strong>16.3</strong> has introduced a new, simpler way to create <code>ref</code>s.</p>
          <aside class="notes">
            <p>Now, if after learning about how to create a <code>ref</code> using the function syntax is a little confusing (and it is for me, too) there's actually a brand new way to create a <code>ref</code> which is coming in React 16.3.</p>
            <p>Let's take a look at an example of this new syntax…</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="7/5" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>The <code>createRef()</code> method</h3>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token comment">// 1. Create a new class property</span>
loading <span class="token operator">=</span> React<span class="token punctuation">.</span><span class="token function">createRef</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// 2. Assign the class property to</span>
<span class="token comment">// the element via ref prop</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">ref</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>loading<span class="token punctuation">}</span></span> <span class="token attr-name">tabIndex</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>-1<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
  Loading…
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>

<span class="token comment">// 3. Call the focus method within componentDidMount</span>
<span class="token keyword">this</span><span class="token punctuation">.</span>loading<span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">focus</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span></code></pre>
          <aside class="notes">
            <p>Coming back to the Loading component example, the snippets of code on the screen here gives a general outline of the new <code>ref</code> syntax.</p>
            <ol>
              <li>The first part to this is to create a new class property. Displayed here is an assignment statement which reads; <code>loading</code> equals <code>React.createRef</code>. This creates a new class property called <code>loading</code> and creates a new <code>ref</code> object for use later in the component.</li>
              <li>Now that we have our <code>ref</code> object created, the next step is to assign the <code>ref</code> to an element using the <code>ref</code> prop. On the screen is a <code>div</code> element with its <code>ref</code> prop being assigned, <code>this.loading</code>. At this point, the <code>loading</code> class property we created in the first step now references the <code>div</code> in our <code>render</code> method.</li>
              <li>Finally, the last step is to actually use the <code>loading</code> class property. With this example of sending focus to the <code>div</code> when the component loads, we can add a single line of code within the Loading component's <code>componentDidMount</code> method. The line reads, <code>this.loading.value.focus</code>. And with this, focus would be send to the <code>div</code> when the component loads onto the screen.<p></p>
            </li></ol>
            <p>So, you may have noticed the <code>value</code> node of that last line. This represents the <em>actual</em> element which has been assigned to the <code>ref</code> object. In this example, it represents the <code>div</code> element.</p>
            <p>With this in mind you might imagine what we'd need to write in order to get the current value of an <code>input</code> element. It would look something like <code>this.refName.value.value</code>. So that may look a little odd when it's written out, but that's how its done.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
      </section>
      <section hidden="" aria-hidden="true" class="stack future" style="top: 350px; display: none;" data-previous-indexv="0">
        <section data-id="8/0" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h2>Using <code>Fragment</code> components <span role="img" aria-label="">🍰</span></h2>
          <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/fragments.gif" width="480" height="389" alt="A close-up of a cupcake. Its top icing decoration is slowley being applied, one icing bag squeeze at a time with pink and blue icing.">
          <aside class="notes">
            <p>Let's talk about a new feature available now as of React 16.2, Fragment components.</p>
            <p>What are fragments and why should we use them? How do they help with accessibility of our apps?</p>
            <p>Let's answer these questions…</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="8/1" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>What are <code>Fragment</code>s?</h3>
          <p><a href="https://reactjs.org/docs/fragments.html">Fragments</a> let you group a list of elements/child components without adding extra nodes to the DOM.</p>
          <aside class="notes">
            <p>So, what are Fragments?</p>
            <p><strong>Fragments</strong> let you group a list of elements or child components together without adding extra nodes to the DOM.</p>
            <p>Since React component templates must be wrapped with an element in order to be returned within the <code>render</code> method, often times developers will just wrap with a <code>div</code>. This works, but if you're not careful, this might also lead to invalid HTML.</p>
            <p>With Fragments, we can now wrap templates with a "fragment element." When the component is rendered, the Fragment element itself is not sent to the DOM, rendering only the HTML required to properly output your content.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="8/2" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Wrapping your content with a <code>div</code>…</h3>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">return</span> <span class="token punctuation">(</span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>Hello<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>World<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
  <span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
          <aside class="notes">
            <p>For example…</p>
            <ol>
              <li>The code snippet on the screen features a <code>render</code> method with a <code>return</code> statement.</li>
              <li>Within this is a <code>div</code> element which is wrapping some table cell, <code>td</code> elements with the word "hello" in one and "world" in the other.</li>
            </ol>
            <p>I think it's safe to say this compoent is meant to be a child of some other data table component.</p>
            <p>Wrapping template code with a <code>div</code> like this is very common. But if you were to wrap table content with a <code>div</code> element here…</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="8/3" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>…may lead to invalid HTML <span role="img" aria-label="">😱</span></h3>
          <pre class=" language-markup"><code class=" language-markup"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>table</span><span class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>Hello<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>World<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>table</span><span class="token punctuation">&gt;</span></span></code></pre>
          <aside class="notes">
            <p>…it would result in invalid HTML being generated and sent to the browser: <code>div</code>s are not valid child elements of table rows.</p>
            <p>So, how do we meet React's requirement of wrapping content with a single element without generating invalid HTML?</p>
            <p><em>[Any guesses from the audience]</em></p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="8/4" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Our new friend <code>React.Fragment</code></h3>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">return</span> <span class="token punctuation">(</span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>React.Fragment</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>Hello<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>World<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>React.Fragment</span><span class="token punctuation">&gt;</span></span>
  <span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
          <aside class="notes">
            <p>You guessed it, with a Fragment!</p>
            <p>Now the code snippet on the screen features a <code>Fragment</code> element which is wrapping the <code>td</code> element table cells.</p>
            <p>With this we can check out how the generated markup is looking…</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="8/5" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>The result <span role="img" aria-label="">👍</span></h3>
          <pre class=" language-markup"><code class=" language-markup"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>table</span><span class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>Hello<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>World<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>table</span><span class="token punctuation">&gt;</span></span></code></pre>
          <aside class="notes">
            <p>And here's the result…</p>
            <p>That looks much better! Semantic, valid HTML with no extra wrapper elements. Nice!</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <!-- <section>
          <h3><span role="img" aria-label="">🔥</span> Newer, optional syntax</h3>
          <pre>
            <code class="language-jsx">
              render() {
                return (
                  &lt;&gt;
                    &lt;td&gt;Hello&lt;/td&gt;
                    &lt;td&gt;World&lt;/td&gt;
                  &lt;/&gt;
                );
              }
            </code>
          </pre>
          <p>Make sure your editor/tooling supports this before using.</p>
          <aside class="notes">
            <p>I feel it's worth mentioning that there is another way of creating <code>Fragment</code> elements. Basically you just remove the <code>React.Fragment</code> string from within the beginning and end <code>Fragment</code> tag and leave the angle brackets behind. This syntax is specific to JSX and is meant to be a quicker and more convienent way of creating <code>Fragment</code>s.</p>
            <p>Now, there may be issues when using this when your editor or other tools like linters or formatters don't know about this syntax. So, it's recommended to make sure you have the latest versions of your editor and any related tooling to provide the necessary support for this.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </section> -->
      </section>
      <section hidden="" aria-hidden="true" class="stack future" style="top: 350px; display: none;" data-previous-indexv="0">
        <section data-id="9/0" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h2>React's accessibility linter <span role="img" aria-label="">🛀</span></h2>
          <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/linter.gif" width="480" height="269" alt="A smiling man opens a door to greet a guest. While doing so the man uses a lint roller to remove lint from his neck tie.">
          <aside class="notes">
            <p>React has an accessibility linter which is pre-packaged with each app.</p>
            <p>As a general note, a code linter is a handy tool which helps to ensure clean code, or code standards as determined by the team or individual. In other words, they let you know when something's not quite right.</p>
            <p>Let's look at a few ways we can use the linter to help ensure a more accessible React app.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="9/1" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3><code>eslint-plugin-jsx-a11y</code></h3>
          <p>Outputs errors to the browser console automatically.</p>
          <pre class=" language-jsx"><code class=" language-jsx"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>images/chrome-console.png<span class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span></code></pre>
          <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/chrome-console.png" alt="Screen capture of Chrome&#39;s developer tools console. A warning message states, &#39;img elements must have an alt prop, either with meaningful text, or an empty string for decorative images.&#39;">
          <aside class="notes">
            <p>The linter in question is called "eslint-plugin-jsx-a11y" and it comes with each app created with the "create-react-app" utility.</p>
            <p>By default, without any setup or configuration on your part, the linter outputs errors found to the browser devtools console.</p>
            <p>For example…</p>
            <ol>
              <li>On the screen is an <code>img</code> element with a valid <code>src</code> attribute, but it's missing its <code>alt</code> attribute. <em>[Does anyone know what happens when a screen reader interacts with an image with no <code>alt</code> attribute?]</em></li>
              <li>Below this is a screenshot of the Chrome devtools console with the output, "<code>img</code> elements must have an <code>alt</code> prop, either with meaningful text, or an empty string for decorative images"</li>
            </ol>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="9/2" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>Code editor a11y linting? <span role="img" aria-label="">🤔</span></h3>
          <p>Let's output errors directly in the editor, too.</p>
          <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/atom-editor.png" alt="Screen capture of Atom text editor. A warning message appears overtop of some code with the following message, &#39;img elements must have an alt prop, either with meaningful text, or an empty string for decorative images.&#39;" class="atom-editor">
          <aside class="notes">
            <p>Outputting errors to the console like that is pretty helpful, but I think this would be even better if these errors were displayed in my editor while I'm writing code.</p>
            <p>On the screen here is a screenshot of my Atom editor outputting an accessibility error with my code. It's the same error as in the console in the previous slide.</p>
            <p>So, let's see how we can set this up.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="9/3" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h4>1. Install ESLint Plugin</h4>
          <ul>
            <li>Atom: <a href="https://atom.io/packages/linter-eslint">linter-eslint</a></li>
            <li>Sublime Text: <a href="https://packagecontrol.io/packages/SublimeLinter-contrib-eslint">SublimeLinter-contrib-eslint</a></li>
            <li>VS Code: <a href="https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint">ESLint</a></li>
          </ul>
          <aside class="notes">
            <p>First install the ESLint plugin for your editor. This is usually done within the editor as part of the editor package manager.</p>
            <p>I've got links to some of the more popular editors these days. The names of the plugins include:</p>
            <ol>
              <li>"linter dash eslint" for Atom</li>
              <li>"Sublime linter dash contrib dash eslint" for Sublime Text</li>
              <li>"ESLint" for VS Code</li>
            </ol>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="9/4" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h4>2. Install ESLint &amp;&amp; <code>eslint-plugin-jsx-a11y</code></h4>
          <pre class=" language-bash"><code class=" language-bash">npm install eslint eslint-plugin-jsx-a11y --save-dev</code></pre>
          <aside class="notes">
            <p>Next, install ESLint and the <code>eslint-plugin-jsx-a11y</code> packages from <code>npm</code>.</p>
            <p>You would asccomplish this by opening your terminal application, changing to your app directory, and typing:</p>
            <p><code>npm install eslint eslint dash plugin dash jsx dash a11y dash dash save dash dev</code></p>
            <p>This command will install these utilities only for your current project, as each project you work on could have a different configuration.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="9/5" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h4>3. Update the <code>.eslintrc</code> file</h4>
          <p>Add to the "plugins" section:</p>
          <pre class=" language-bash"><code class=" language-bash">"plugins": [
  "jsx-a11y"
]</code></pre>
          <p>Add to the "extends" section:</p>
          <pre class=" language-bash"><code class=" language-bash">"extends": [
  "plugin:jsx-a11y/recommended"
]</code></pre>
          <aside class="notes">
            <p>The last thing to do is update, or create if it doesn't exist, your project's <code>eslint.rc</code> file.</p>
            <p>In the <em>plugins</em> section of this file, you'd add "jsx dash a11y." This loads the accessibility plugin for use with your editor's ESLint plugin.</p>
            <p>In the <em>extends</em> section, you'd add "plugin colon jsx dash a11y forward-slash recommended." This loads the default, recommended rules for the plugin to test your code against.</p>
            <p>So, after this is all done, you'd just restart your editor and you should see some errors come up when you've got some accessibility issues in your code!</p>
            <span role="img" aria-label="">👉</span>
          </aside>
        </div></section>
      </section>
      <section hidden="" aria-hidden="true" class="stack future" style="top: 350px; display: none;" data-previous-indexv="0">
        <section data-id="10/0" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h2>Writing semantic HTML in React <span role="img" aria-label="">⌨️</span></h2>
          <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/writing.webp" width="480" height="269" alt="Kermit the Frog aggressively types on an old type writer.">
          <aside class="notes">
            <p>The last thing I want to discuss is writing HTML in React.</p>
            <p>In the past I've been asked the very broad, open ended question, "How accessible is React?"</p>
            <p>This was coming from the knowledge that other frameworks or libraries had great difficulty when it came to accessibility as a result of the framework team providing third-party user interfaces and components.</p>
            <p>In other words, if something wasn't accessible, there's not a great chance of it <em>actually</em> getting fixed as it relied on a third-party team.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="10/1" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <a href="https://twitter.com/heydonworks/status/962005610723069954" target="_blank">
            <img src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/heydon.png" alt="Screen capture of Twitter. A tweet from Heydon Pickering (@heydonworks) reads, &#39;React code doesn&#39;t have to be inaccessible any more than hip-hop has to be misogynist.&#39; Opens in a new window.">
          </a>
          <aside class="notes">
            <p>On this slide is a relavent quote from Heydon Pickering. It reads…</p>
            <p>React code doesn't <em>have</em> to be inaccessible any more than hip-hop <em>has</em> to be misogynist.</p>
            <p>I believe this to be true and is actually a nice seguey into my next point…</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="10/2" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>React Components are ES6 Classes</h3>
          <p>Since React uses <a href="https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Classes">ES6 classes</a> and standard HTML markup to generate its components, it’s up to you to continue to write good, clean, semantic HTML.</p>
          <aside class="notes">
            <p>What I've found is that since React uses ES6 classes and standard HTML markup within its templates to create and export components, it's up to you, the developer, to continue to write valid, semantic HTML.</p>
            <p>With the exception of using a third-party module from <code>npm</code> it's really all up to you. React doesn't force you to use something that someone else made, thus lowering the risk of creating an inaccessible product.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
        <section class="future" aria-hidden="true" data-id="10/3" style="top: 350px; display: none;"><div class="accessibilityWrapper" tabindex="-1">
          <h3>In other words…</h3>
          <p>If there are accessibility issues, <strong><em>it's your fault</em></strong> . This is a good thing! <span role="img" aria-label="">👍</span></p>
          <aside class="notes">
            <p>In other words; if there are any accessibility issues, <em>it's your fault</em>.</p>
            <p>And this is a good thing!</p>
            <p>It's up to you as the developer to fix these issues. You don't have to wait for a third-party developer group to <em>maybe</em> get around to fixing these issues <em>someday</em>. You can do it youself, <strong>today</strong>.</p>
            <span role="img" aria-label="">👇</span>
          </aside>
        </div></section>
      </section>   
      <section hidden="" aria-hidden="true" class="future" style="top: 350px; display: none;" data-id="13"><div class="accessibilityWrapper" tabindex="-1">
        <h2>Thanks! <span role="img" aria-label="">🙂</span></h2>
        <aside class="notes">
          <p>Thank you, everyone!</p>
          <p><em>[Questions?]</em></p>
        </aside>
      </div></section>
    </div>
  <div class="backgrounds">
    <div class="slide-background present" data-loaded="true" style="display: block;"></div>
    <div class="slide-background stack future" data-loaded="true" style="display: block;">
      <div class="slide-background past" data-loaded="true" style="display: block;"></div><div class="slide-background present" data-loaded="true" style="display: block;"></div></div><div class="slide-background future" data-loaded="true" style="display: block;"></div><div class="slide-background stack future" data-loaded="true" style="display: none;"><div class="slide-background present" data-loaded="true" style="display: none;"></div><div class="slide-background future" style="display: none;" data-loaded="true"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div></div><div class="slide-background stack future" style="display: none;" data-loaded="true"><div class="slide-background present" data-loaded="true" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div></div><div class="slide-background stack future" style="display: none;"><div class="slide-background present" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div></div><div class="slide-background stack future" style="display: none;"><div class="slide-background present" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div></div><div class="slide-background stack future" style="display: none;"><div class="slide-background present" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div></div><div class="slide-background stack future" style="display: none;"><div class="slide-background present" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div></div><div class="slide-background stack future" style="display: none;"><div class="slide-background present" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div></div><div class="slide-background stack future" style="display: none;"><div class="slide-background present" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div></div><div class="slide-background stack future" style="display: none;"><div class="slide-background present" style="display: none;"></div><div class="slide-background future" style="display: none;"></div></div><div class="slide-background future" style="display: none;"></div><div class="slide-background future" style="display: none;"></div></div><div class="progress" style="display: block;"><span style="width: 0px;"></span></div><aside class="controls" style="display: block;"><button class="navigate-left" aria-label="previous slide" disabled="disabled"></button><button class="navigate-right enabled" aria-label="next slide"></button><button class="navigate-up" aria-label="above slide" disabled="disabled"></button><button class="navigate-down" aria-label="below slide" disabled="disabled"></button></aside><ul id="table-of-contents" aria-hidden="true"><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/0">1. Creating Accessible React Apps</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/1/0">2. Can React apps be accessible? 🤔</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/1/1">3. Yes! 🎉</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/2">4. Agenda ✅</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/3/0">5. Notes on getting started 📓</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/3/1">6. camelCase</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/3/2">7. Reserved words</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/3/3">8. Self closing elements require /</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/4/0">9. Setting the page title 📰</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/4/1">10. The problem… 🤔</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/4/2">11. Set the page title! 👍</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/4/3">12. Use document.title</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/4/4">13. Other existing components</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/5/0">14. Live announcements 📢</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/5/1">15. The problem… 🤔</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/5/2">16. Create a Live Announcements component 👍</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/5/3">17. Usage, part 1</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/5/4">18. Usage, part 2</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/5/5">19. Usage, part 3</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/5/6">20. Other existing components</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/6/0">21. Focus management ☕️</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/6/1">22. The problem… 🤔</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/6/2">23. Focus management! 👍</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/6/3">24. Selecting an element</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/6/4">25. The React way</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/6/5">26. Using the ref…</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/7/0">27. More focus management! 🐶</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/7/1">28. The problem… 🤔</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/7/2">29. Our new friend, ref</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/7/3">30. Set "page" focus via ref</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/7/4">31. 🔥 New ref syntax</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/7/5">32. The createRef() method</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/8/0">33. Using Fragment components 🍰</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/8/1">34. What are Fragments?</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/8/2">35. Wrapping your content with a div…</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/8/3">36. …may lead to invalid HTML 😱</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/8/4">37. Our new friend React.Fragment</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/8/5">38. The result 👍</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/9/0">39. React's accessibility linter 🛀</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/9/1">40. eslint-plugin-jsx-a11y</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/9/2">41. Code editor a11y linting? 🤔</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/9/3">42. 1. Install ESLint Plugin</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/9/4">43. 2. Install ESLint &amp;&amp; eslint-plugin-jsx-a11y</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/9/5">44. 3. Update the .eslintrc file</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/10/0">45. Writing semantic HTML in React ⌨️</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/10/1">46. 
            
          </a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/10/2">47. React Components are ES6 Classes</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/10/3">48. In other words…</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/11/0">49. Demo! 📺</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/11/1">50. Demo Highlights 📱</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/12">51. Bonus! 💥</a></li><li><a href="https://svinkle.github.io/creating-accessible-react-apps-talk/#/13">52. Thanks! 🙂</a></li></ul><div class="slide-number" style="display: none;"></div><div class="speaker-notes" data-prevent-swipe="" tabindex="0"></div><div class="pause-overlay"></div><div id="aria-status-div" aria-live="polite" aria-atomic="true" style="position: absolute; height: 1px; width: 1px; overflow: hidden; clip: rect(1px, 1px, 1px, 1px);">
        Creating Accessible React Apps
        
          
            
              Balram Singh • @erbalramsingh
            
            
              
                
              
            
            
              
                
              
              
                
              
              
                
              
            
          
        
        
      </div></div>

  <script src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/head.min.js"></script>
  <script src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/reveal.js"></script>
  <script src="https://github.com/balramsinghindia/creating-accessible-websites-in-react16/blob/master/prism.js"></script>
  <script>
  Prism.plugins.NormalizeWhitespace.setDefaults({
  'remove-trailing': true,
  'remove-indent': true,
  'left-trim': true,
  'right-trim': true,
  'break-lines': 52,
  //'indent': 2,
  'remove-initial-line-feed': true
  //'tabs-to-spaces': 2,
  //'spaces-to-tabs': 2
});
</script>

  <script>
  // More info about config & dependencies:
// - https://github.com/hakimel/reveal.js#configuration
// - https://github.com/hakimel/reveal.js#dependencies
Reveal.initialize({
  dependencies: [
    {
      src: 'plugin/markdown/marked.js'
    },
    {
      src: 'plugin/markdown/markdown.js'
    },
    {
      src: 'plugin/notes/notes.js',
      async: true
    },
    {
      src: 'plugin/accessibility/helper.js',
      async: true,
      condition: function() {
        return !!document.body.classList;
      }
    },
    {
      src: 'plugin/title-footer/title-footer.js',
      async: true,
      callback: function() {
        title_footer.initialize(
          'Creating Accessible React Apps • <a href="https://twitter.com/erbalramsingh">Balram Singh</a>'
        );
      }
    }
  ]
});
</script>




</body></html>

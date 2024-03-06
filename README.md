
# Horisean Project Refactoring

this document pertains to week one challenge for HTML,CSS and Git. Source code found in "source code subfolder" cloned from UCF bootcampp repository 

# Mission

refactor the site to allow for better accessibility functions and organize sematic structure.

## mock up 

<p>
<img src="/assets/images/mockup.png>" alt="mockup">
</p>
<p>
<img src="/assets/images/mockup2.png>" alt="mockup2">
</p>
<p>
<img src="/assets/images/mockup3.png>" alt="mockup3">
</p>

## Changes

* added title to <title> element 
```html
<title>Horisean Solutions</title>
```

* added <nav> to html structure 
 ```html
<nav 
class="header">
        <h1>Hori<span class="seo">seo</span>n</h1>
        <div>
            <ul>
                <li>
                    <a href="#search-engine-optimization">Search Engine Optimization</a>
                </li>
                <li>
                    <a href="#online-reputation-management">Online Reputation Management</a>
                </li>
                <li>
                    <a href="#social-media-marketing">Social Media Marketing</a>
                </li>
            </ul>
        </div>
</nav>
```
* added id categorization to "search engine optimization" to allow navigation to work 
```html
  <div id="search-engine-optimization" class="search-engine-optimization">
            <img src="./assets/images/search-engine-optimization.jpg" alt="picture of SEO notepad" class="float-left" />
            <h2>Search Engine Optimization</h2>
            <p>
                The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
            </p>
```

* added "alt" feature to site in order to better accessibility when pictures do not load
```html
 <div class="hero"></div>
    <div class="content">
        <div id="search-engine-optimization" class="search-engine-optimization">
            <img src="./assets/images/search-engine-optimization.jpg" alt="picture of SEO notepad" class="float-left" />
            <h2>Search Engine Optimization</h2>
            <p>
                The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
            </p>
        </div>
        <div id="online-reputation-management" class="online-reputation-management">
            <img src="./assets/images/online-reputation-management.jpg" alt="picture of bar graph on computer screen" class="float-right" />
            <h2>Online Reputation Management</h2>
            <p>
                The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
            </p>
        </div>
        <div id="social-media-marketing" class="social-media-marketing">
            <img src="./assets/images/social-media-marketing.jpg" alt="picture of social media brainstoring" class="float-left" />
            <h2>Social Media Marketing</h2>
            <p>
                Social media continues to have a sizable influence on buying habits. Social media marketing helps you determine which platforms are suited to your brand, using analytics to find the right markets and increase your lead generation.
            </p>
        </div>
    </div>
</div>
```

* separated code and created aside and footer html structures 
```html
 <aside>
 class="benefits">
        <div class="benefit-lead">
            <h3>Lead Generation</h3>
            <img src="./assets/images/lead-generation.png" alt="picture of digital funnel" />
            <p>
                Inbound strategies for lead generation require less work for your business, bringing customers directly to your website.
            </p>
        </div>
        <div class="benefit-brand">
            <h3>Brand Awareness</h3>
            <img src="./assets/images/brand-awareness.png" alt="picture of lightbulb"/>
            <p>
                Users find your business through paid and organic searches, increasing the search ranking and visibility for your business.
            </p>
        </div>
        <div class="benefit-cost">
            <h3>Cost Management</h3>
            <img src="./assets/images/cost-management.png" alt="picture of coins"/>
            <p>
                As the search ranking for your business increases, your advertising costs decrease, and you no longer need to advertise your page.
            </p>
        </div>
</aside>
<footer 
 class="footer">
    <h2>Made with ❤️️ by Horiseon</h2>
    <p>
        &copy; 2024 Horiseon Social Solution Services, Inc.
    </p>
 </footer>
```

* in the style sheet i consolidated the benefits styling by separating them by a comma and condensing into one rule.
```css
}
.benefit-lead ,.benefit-brand,.benefit-cost{
    margin-bottom: 32px;
    color: #ffffff;
}
```

* i also changed color of the seo to make the brand objective more recognizeable 
```css

.header h1 .seo {
    color: orange;
}
```
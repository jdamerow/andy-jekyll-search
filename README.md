# Andy - A Lunr Search Generator

This mini plugin provides a generator for Jekyll pages that generators the necessary files to add a [Lunr.js](http://lunrjs.com/) search to your site. 
Since GitHub pages disable most Jekyll plugins, I wrote this little generator to programmatically add all posts to the Lunr index. The result of the generator are two files: `search-index.js` and `catalog.json` that can be used to search the site through Lunr, and display the search results. The basic idea of Andy is that you don't need this plugin on the GitHub pages servers. The plugin generates files locally that you then check in to your GitHub pages repository. As an example see the [DigInG Course Book](https://github.com/diging/course-book).

Note: this is a very rough first implementation, and this solution might not necessarily scale very well.

## Installation

Simply copy the two files in the lib folder `andy_generator.rb` and `search-index.js` into the `_plugin` folder of your Jekyll project.

After you start up Jekyll, you should then find the files `search-index.js` and `catalog.json` in `/assets/js`.

## Usage

You can now use Lunr.js as described on their webpage. You can find two templates for a very simple search interface in `templates`:
 - `andy_search.js`: add this javascript to your Jekyll site. It queries the Lunr index and adds the results to a list.
 - `search_page.html`: this is a very simple search results page.
 - 
 
The javascript in `andy_search.js` requires a search input field with a search button with specific ids:
```
<div id="search_div">
  Search: <input type="text" id="search_box">
  <a data-href="{{site.baseurl}}/search.html" id="search_button"><i class="fa fa-search"></i></a>
</div>
```



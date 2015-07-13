# Andy - A Lunr Search Generator

This mini plugin provides a generator for Jekyll pages that generators the necessary files to add a [Lunr.js](http://lunrjs.com/) search to your site. 
Since GitHub pages disable most Jekyll plugins, I wrote this little generator to programmatically add all posts to the Lunr index. The result are two files: `search-index.js` and `catalog.json` that can be used to search the site through Lunr, and display the search results.

Note: this is a very rough first implementation, and this solution might not necessarily scale very well.

## Installation

Simply copy the two files in the lib folder `andy_generator.rb` and `search-index.js` into the `_plugin` folder of your Jekyll project.

After you start up Jekyll, you should then find the files `search-index.js` and `catalog.json` in `/assets/js`.

## Usage

You can now use Lunr.js as described on their webpage. You can find two templates for a very simple search interface in `templates`.



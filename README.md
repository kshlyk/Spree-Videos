Spree Videos
===========

Display YouTube video(s) on your product page.

* Thumbnails from YouTube
* Clickable thumbnails to easily switch between videos
* Easily add/remove/edit videos through the spree admin
* Versions available for Spree 0.7 & 1.x

Example
=======
There is no deface override included by default to include the videos in your product page. To add videos to your product page:

	# products/show.html.erb
	<%= render 'video', :product => @product %>
	
If you are using Twitter Bootstrap, you can easily add title tooltips to your video thumbnails:"
	
	# javascripts/store/your.coffeescript
	$('#video-thumbnails > a').tooltip()

Installation
============

	bundle exec rails g spree_videos:install
	
	# auto run via the install generator, but in case you didn't run it
	bundle exec rake db:migrate
	
Configuration
=============

You can specify configuration options that get passed through to the JS dynamic youtube video switcher & the html5 embed. Take a look at `config/initializers/spree_videos.rb` for example configuration.

You can easily customize the display of the thumbnails / player:
	
	// stylesheets/store/videos.css.less
	
	#product-videos {
	
		#video-player {
			// player holder
		}
	
		#video-thumbnails {
			// thumbnail holder
	
			a {
				// thumbnails 
	
				display: block;
				float: left;
	
				&:hover { }
				
				&:first-child { }
				
				&:last-child { }
			}
		}
	}

Contributors
============
* Mark Linn, @markalinn
* Michael Bianco, @iloveitaly
* Aleksey, @alekseydem
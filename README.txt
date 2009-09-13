	Original Source : Pavel Tzonkov <pavelc@users.sourceforge.net>
	Source Link : http://gscripts.net/free-php-scripts/Anti_Spam_Scripts/Image_Validator/details.html
	
	CodeIgniter library created by : 
		Mohammad Amzad Hossain
		http://tohin.wordpress.com
		
	
	License: Have Fun 
	
	# How To Use In CodeIgniter 
	
		// First Store Some fonts in fonts folder 
		// You can choose a font_name by overriding default value or this 
		// will randomly select a font.
		
	
		// In Controller 
		
			$this->load->library('antispam');
			$configs = array(
					'img_path' => './captcha/',
					'img_url' => base_url() . 'captcha/',
					'img_height' => '50',
				);			
			$captcha = $this->antispam->get_antispam_image($configs);
			
		// $captcha is an array exmaple
		//  array('word' => 'sfsdf', 'time' => time , 'image' => '<img .... ');
		
		
		// In View Print the $captcha['image'] to show captcha image.
		
		
	// Future Extension 
	
		Generated Captcha images always stored in captcha folder which is memory consuming
		unless you clear them out manually. 
		
		Looking for a feasible idea to delete them all.
		
		
Available Parameters FOR Configs: 

	'img_url' 		=>  Image URL 
	'img_path'		=> Image PATH
	'img_width'		=> Image Width
	'img_height' 	=> Image Height

	'font_name'		=> Font Name example Test.ttp
	'font_path' 	=> FONT PATH
	
	'font_size'		=> 	15
	
	'char_set' 		=> "ABCDEFGHJKLMNPQRSTUVWXYZ2345689";
	'char_length' 	=>	integer captcha word length in character
	
	'char_color' 	=> 
						Example :   "#880000,#008800,#000088,#888800,#880088,#008888,#000000";  
						This colors will be randomly use for character coloring.
	
	
	
	'line_count'	=>	10;		Number of lines to Create Noise	
	'line_color'	=> 
						Example: "#DD6666,#66DD66,#6666DD,#DDDD66,#DD66DD,#66DDDD,#666666"
						This colors will be randomly use for line coloring.
	
	 
	'bg_color'		=>	'#FFFFFF';		Captcha Image Background Color

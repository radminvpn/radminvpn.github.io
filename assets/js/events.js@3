$(function(){
	function createFunctionWithTimeout(callback, opt_timeout) 
	{
		var called = false;
		function fn() { if (!called) { called = true; callback(); } }
		setTimeout(fn, opt_timeout || 1000);
		return fn;
	}

	/* New events */
	$(document).on('click', '.buttonDownload', function(event) {
		event.preventDefault();
		var url = $(this).attr('href');
		var _href = url.replace(/^.*\/download\//, '');
		    _href = _href.replace(/^.*files\//, '');
		gtag('event', 'my_file_download', {'event_category':_href, 'event_callback': createFunctionWithTimeout(function(){document.location = url;}) });
	});	
	
	$(document).on('click', 'a[href*="discord.gg"]', 
	function(event) 
	{
		event.preventDefault(); 
		var url = $(this).attr('href'); 
		gtag('event', 'my_go_out', {'event_category':'Discord', 'event_label': url, 'event_callback': createFunctionWithTimeout(function(){document.location = url;}) });
	});
	$(document).on('click', 'a[href*="discord.com"]', 
	function(event) 
	{
		event.preventDefault(); 
		var url = $(this).attr('href'); 
		gtag('event', 'my_go_out', {'event_category':'Discord', 'event_label': url, 'event_callback': createFunctionWithTimeout(function(){document.location = url;}) });
	});	
	$(document).on('click', 'a[href*="radmin-club.com"]', 
	function(event) 
	{
		event.preventDefault(); 
		var url = $(this).attr('href'); 
		gtag('event', 'my_go_out', {'event_category':'Radmin Club', 'event_label': url, 'event_callback': createFunctionWithTimeout(function(){document.location = url;}) });
	});
	$(document).on('click', 'a[href*="www.radmin.com"]', 
	function(event) 
	{
		event.preventDefault(); 
		var url = $(this).attr('href'); 
		gtag('event', 'my_go_out', {'event_category':'Radmin', 'event_label': url, 'event_callback': createFunctionWithTimeout(function(){document.location = url;}) });
	});	
});
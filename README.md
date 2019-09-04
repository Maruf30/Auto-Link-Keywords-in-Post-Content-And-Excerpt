# Auto-Link-Keywords-in-Post-Content-And-Excerpt


// auto link keywords in post content and excerpt
function wcs_auto_link_keywords( $text ) {
    $replace = array(
        'wordpress' => '<a href="http://www.wordpress.org">wordpress</a>',
        'google' => '<a href="http://www.google.com">excerpt</a>',
        'facebook' => '<a href="http://www.facebook.com">function</a>'
    );
    $text = str_replace( array_keys($replace), $replace, $text );
    return $text;
}
add_filter( 'the_content', 'wcs_auto_link_keywords' );
add_filter( 'the_excerpt', 'wcs_auto_link_keywords' );





Disable Code All :- Scripts:-- 

woocommerce disable updated:-

add_filter( 'auto_update_plugin', '__return_false' );

-----------**********----------------
-----------**********----------------
-----------**********----------------
-----------**********----------------
-----------**********----------------
-----------**********----------------
-----------**********----------------

// Disable Elementor and Elementor Pro Updates
function disable_elementor_updates( $value ) {
    if ( isset($value) && is_object($value) ) {
        // Disable Elementor update
        if ( isset( $value->response['elementor/elementor.php'] ) ) {
            unset( $value->response['elementor/elementor.php'] );
        }
        // Disable Elementor Pro update
        if ( isset( $value->response['elementor-pro/elementor-pro.php'] ) ) {
            unset( $value->response['elementor-pro/elementor-pro.php'] );
        }
    }
    return $value;
}
add_filter( 'site_transient_update_plugins', 'disable_elementor_updates' );
 
// Disable Elementor Kit and Widgets
add_action( 'wp', 'disable_elementor_kits' );
 
function disable_elementor_kits() {
    // Disable Elementor widgets and templates
    if ( class_exists( 'Elementor\Plugin' ) ) {
        remove_action( 'elementor/widgets/widgets_registered', [ 'Elementor\Plugin', 'add_widget' ] );
        // Optionally remove Elementor front-end styles and scripts
        wp_dequeue_style( 'elementor-frontend' );
        wp_dequeue_script( 'elementor-frontend' );
    }
}

-----------**********----------------
-----------**********----------------
-----------**********----------------
-----------**********----------------
-----------**********----------------
-----------**********----------------
-----------**********----------------



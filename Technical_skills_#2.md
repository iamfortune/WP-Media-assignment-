
Please write a helper plugin that will prevent these notices from being displayed.

- to solve the issue of notices, the helper function below can help 



add_action( 'admin_init', function() {
    $container  = apply_filters( 'rocket_container', null );
    $subscriber = $container->get( 'admin_cache_subscriber' );
​
    remove_action( 'admin_notices', [ $subscriber, 'notice_advanced_cache_permissions' ] );
    remove_action( 'admin_notices', [ $subscriber, 'notice_advanced_cache_content_not_ours' ] );
} );
# Install Laravel Passport Package
#Install Passport Via Composer
php artisan passport:install
# Using HasApiTokens, Notifiable on User Model
use Illuminate\Notifications\Notifiable;
use Laravel\Passport\HasApiTokens;
# Update Auth config
'api' => [
    'driver' => 'passport',
    'provider' => 'users',
],
# Update AuthServiceProvider on boot() method
$this->registerPolicies();
Passport::routes();
# Using UUIDS
php artisan passport:install --uuids

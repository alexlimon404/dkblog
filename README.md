test blog
+--------+-----------+--------------------------------+------------------------+------------------------------------------------------------------------+--------------+
| Domain | Method    | URI                            | Name                   | Action                                                                 | Middleware   |
+--------+-----------+--------------------------------+------------------------+------------------------------------------------------------------------+--------------+
|        | GET|HEAD  | /                              |                        | Closure                                                                | web          |
|        | GET|HEAD  | admin                          | admin.index            | App\Http\Controllers\Admin\DashboardController@dashboard               | web,auth     |
|        | GET|HEAD  | admin/category                 | admin.category.index   | App\Http\Controllers\Admin\CategoryController@index                    | web,auth     |
|        | POST      | admin/category                 | admin.category.store   | App\Http\Controllers\Admin\CategoryController@store                    | web,auth     |
|        | GET|HEAD  | admin/category/create          | admin.category.create  | App\Http\Controllers\Admin\CategoryController@create                   | web,auth     |
|        | GET|HEAD  | admin/category/{category}      | admin.category.show    | App\Http\Controllers\Admin\CategoryController@show                     | web,auth     |
|        | PUT|PATCH | admin/category/{category}      | admin.category.update  | App\Http\Controllers\Admin\CategoryController@update                   | web,auth     |
|        | DELETE    | admin/category/{category}      | admin.category.destroy | App\Http\Controllers\Admin\CategoryController@destroy                  | web,auth     |
|        | GET|HEAD  | admin/category/{category}/edit | admin.category.edit    | App\Http\Controllers\Admin\CategoryController@edit                     | web,auth     |
|        | GET|HEAD  | api/user                       |                        | Closure                                                                | api,auth:api |
|        | GET|HEAD  | home                           | home                   | App\Http\Controllers\HomeController@index                              | web,auth     |
|        | GET|HEAD  | login                          | login                  | App\Http\Controllers\Auth\LoginController@showLoginForm                | web,guest    |
|        | POST      | login                          |                        | App\Http\Controllers\Auth\LoginController@login                        | web,guest    |
|        | POST      | logout                         | logout                 | App\Http\Controllers\Auth\LoginController@logout                       | web          |
|        | POST      | password/email                 | password.email         | App\Http\Controllers\Auth\ForgotPasswordController@sendResetLinkEmail  | web,guest    |
|        | GET|HEAD  | password/reset                 | password.request       | App\Http\Controllers\Auth\ForgotPasswordController@showLinkRequestForm | web,guest    |
|        | POST      | password/reset                 | password.update        | App\Http\Controllers\Auth\ResetPasswordController@reset                | web,guest    |
|        | GET|HEAD  | password/reset/{token}         | password.reset         | App\Http\Controllers\Auth\ResetPasswordController@showResetForm        | web,guest    |
|        | GET|HEAD  | register                       | register               | App\Http\Controllers\Auth\RegisterController@showRegistrationForm      | web,guest    |
|        | POST      | register                       |                        | App\Http\Controllers\Auth\RegisterController@register                  | web,guest    |
+--------+-----------+--------------------------------+------------------------+------------------------------------------------------------------------+--------------+

# Changelog

## v0.6.0 (released at 10/06/2015)

* Scan 2D barcode using new syntax `on :scan, with: 'BINDING_QR_CODE' ` instead of `on :event, with: 'BINDING_QR_CODE' ` in previous version #55
  Which will fix can not using `on :event, with: "scan" ` problem
* Click menu support new syntax `on :click, with: 'BOOK_LUNCH' `, but `on :event, with: 'BOOK_LUNCH' ` still supported. perfer `on :click` because it running faster and more nature expression.
* Fix refresh token not working problem under ruby 2.0.0 #54
* New department_update, user_batchdelete, convert_to_openid API

## v0.5.0 (released at 9/25/2015)

* Only relay on activesupport on run time, so will greatly improve wechat cli startup time
* Add rails generator support `rails g wechat:install`
* Add batch job support for enterprise account like batch create user/department, both API, callback responder and CLI
* Add material management API and CLI
* Add tag API and CLI for enterprise account
* Add QR code scene function for public account

## v0.4.2 (released at 9/7/2015)

* Fix wrong number of arguments at Wechat::Responder.on by using arity #47
* Fix can not access wechat method after using instance level context.
* Fix skip_verify_ssl parameter error. 

## v0.4.1 (released at 9/6/2015)

* Limit news articles collection to 10, close #5
* Resolve the conflict with gem "responders" by @seamon #45

## v0.4.0 (released at 9/5/2015)

* Enable the verify SSL for enterprise mode by default, as security is more importent than speed, but still can switch off by configure
* Support scancode_push/scancode_waitmsg event.
* New API method can get wechat server IP list
* New API to query/create department/media/material
* Fix can not read token_file in mingw bug, which introduce at #43

## v0.3.0 (released at 8/30/2015)

* New user group management API
* Allow transfer to customer service on fallback. #42
* Read and write access_token properly using file locking, #43

## v0.2.0 (released at 8/27/2015)

* Add wechat enterprise account support
* Make responder execute in action context, by @lazing #15
* jsapi_ticket support, by @feitian124 #27
* Rename gems to wechat and ambitious to being #1 gems about development wechat. thanks Xiaoning transfer this gem name.
* Original gem `wechat-rails` author skinnyworm trasfer to Eric-Guo as maintainer

## v0.1.1

* Initial release from [wechat-rails](https://github.com/skinnyworm/wechat-rails).

# Waitlisted::ReservationApi

All URIs are relative to *https://www.waitlisted.co/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activate_reservation**](ReservationApi.md#activate_reservation) | **POST** /reservations/activate | 
[**create_reservation**](ReservationApi.md#create_reservation) | **POST** /reservations | 
[**delete_reservation**](ReservationApi.md#delete_reservation) | **DELETE** /reservations | 
[**get_reservation**](ReservationApi.md#get_reservation) | **GET** /reservations | 


# **activate_reservation**
> ReservationsResponse activate_reservation(body)



Activate a reservation.

### Example
```ruby
# load the gem
require 'waitlisted'
# setup authorization
Waitlisted.configure do |config|
  # Configure API key authorization: api_key
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = Waitlisted::ReservationApi.new

body = Waitlisted::ReservationRequest.new # ReservationRequest | Reservation Data


begin
  result = api_instance.activate_reservation(body)
  p result
rescue Waitlisted::ApiError => e
  puts "Exception when calling ReservationApi->activate_reservation: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ReservationRequest**](ReservationRequest.md)| Reservation Data | 

### Return type

[**ReservationsResponse**](ReservationsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **create_reservation**
> ReservationsResponse create_reservation(body)



Creates a new reservation.

### Example
```ruby
# load the gem
require 'waitlisted'

api_instance = Waitlisted::ReservationApi.new

body = Waitlisted::Reservation.new # Reservation | Reservation Data


begin
  result = api_instance.create_reservation(body)
  p result
rescue Waitlisted::ApiError => e
  puts "Exception when calling ReservationApi->create_reservation: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Reservation**](Reservation.md)| Reservation Data | 

### Return type

[**ReservationsResponse**](ReservationsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **delete_reservation**
> delete_reservation(body)



Delete a reservation.

### Example
```ruby
# load the gem
require 'waitlisted'
# setup authorization
Waitlisted.configure do |config|
  # Configure API key authorization: api_key
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = Waitlisted::ReservationApi.new

body = Waitlisted::ReservationRequest.new # ReservationRequest | Reservation Data


begin
  api_instance.delete_reservation(body)
rescue Waitlisted::ApiError => e
  puts "Exception when calling ReservationApi->delete_reservation: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ReservationRequest**](ReservationRequest.md)| Reservation Data | 

### Return type

nil (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **get_reservation**
> ReservationsResponse get_reservation(email)



Get a reservation.

### Example
```ruby
# load the gem
require 'waitlisted'

api_instance = Waitlisted::ReservationApi.new

email = "email_example" # String | Email address


begin
  result = api_instance.get_reservation(email)
  p result
rescue Waitlisted::ApiError => e
  puts "Exception when calling ReservationApi->get_reservation: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **String**| Email address | 

### Return type

[**ReservationsResponse**](ReservationsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json




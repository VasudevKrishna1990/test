cmake_minimum_required(VERSION 3.12)
project(SwiggyZomato VERSION 1.0.0)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17")
add_library(backEnd
common.hpp
deliveryChargeCalculationStrategy.hpp
deliveryMetaData.hpp
deliveryMgr.cpp
deliveryMgr.hpp
deliveryPartner.hpp
deliveryPartnerMgr.hpp
deliveryPartnerMgr.cpp
dish.hpp
dishAddOn.hpp
foodMgr.cpp
foodMgr.hpp
ideliveryPartnerMatchingStrategy.hpp
inotificationSender.hpp
ipartner.hpp
locBasedDeliveryChargeCalculationStrategy.hpp
locBasedDeliveryPartnerMatchingStrategy.hpp
menu.hpp
notificationMgr.cpp
notificationMgr.hpp
order.hpp
orderMgr.cpp
orderMgr.hpp
pushNotificationSender.hpp
restaurant.hpp
restaurantMgr.cpp
restaurantMgr.hpp
restaurantOwner.hpp
smsNotificationSender.hpp
strategyMgr.cpp
strategyMgr.hpp
user.hpp
userMgr.cpp
userMgr.hpp)

add_executable(SwiggyZomato swiggy_zomato.cpp)
target_link_libraries(SwiggyZomato PRIVATE backEnd)
# sasai-assignment-response
1) changed LOGGER to static context in com.econetwireless.utils.formatters.MobileNumberUtils
2) PartnerCodeValidatorImpl constructor no such thing as this(super); by default super constructor is called by java
3) changed @PreInsert to @PrePersist in com.econetwireless.epay.domain.SubscriberRequest
4) .persist and .update dont exist, used .save instead in EnquiriesServiceImpl and CreditsServiceImpl of package com.econetwireless.epay.business.services.impl
5) updated econet-utils.pom.xml to resolve "javax.jws cannot be resolved, javax.xml cannot be resolved" added the following dependencies 
	jakarta.xml.ws-api
	jaxws-rt
6) changed Request to request in com.econetwireless.epay.domain.SubscriberRequest named query
7) ResponseCode enum  //code= code was causing the instance variable nt to be initialised changed to this.code = code;
8) added  @PathVariable("partnerCode")  to enquireAirtimeBalance method in com.econetwireless.epay.api.rest.resources.EpayResource

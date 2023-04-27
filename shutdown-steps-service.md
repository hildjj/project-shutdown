# Service Sunsetting Process

Services can be especially tricky to sunset because it may not always be easy to determine who the customers are. These often require special handling that is context sensitive.

## Planning Obsolecense

Services should have some means to pass along potentially "Out of Band" or meta data that is available for customers. This may include an optional "notice" field in a JSON repsonse, or a `WARNING` header in the repsonse. Customers should be informed to pay attention to these fields as they will contain information important to the service being provided. (If your service does not currently implement these fields, you're strongly encouraged to add them if possible.)

Services almost never "go to zero". Some usage will almost always be present. It's important to set a proper minimum threshold and rule regarding when a service is "idle enough" to disable. (e.g. "once usage reaches an average of 100 RpS over 24 hours", or "Once usage reaches 10% of peak usage for October 2023").

## Communication

Again, communication is critical, particularly if your service provides something that is consumed and distributed for larger functions (e.g. you run a database of local network IDs that is used as part of an AGPS service, or you host a list of vulnerabilities for a given system that is used as part of a larger security monitoring system.) You may have only a small number of customers, but those customers may have tremendous reach.

Complicating matters, those larger customers may not have publically exposed means to contact internal teams, or the contact you had last year may no longer work on that specific team. While you should make some reasonable effort to communicate in good faith with those customers, friction will be inevitable. You may wish to introduce "service reliability concerns" in order to gain their attention early.

At the end of the day, they're people too, and they also don't want to lose their weekends and evenings doing emergency work if they don't have to.


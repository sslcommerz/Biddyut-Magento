
Magento 2 Biddyut Shipping (Sslwireless_Biddyut &  Sslwireless_Address)
=======================================

Goals:
=======================================
- Biddyut/iPost(A Technology Driven Logistics & Delivery Company Bangladesh/Kurdistan Magento 2.x
- Custom Shipping Module For Magento 2 Between Magento 2 Store & Carrier Site .
- Shipping Price Calculate According To Biddyut/iPost Rate Via API To Your Magento 2x Store That Finaly Show Shipping Cost.
- Order Details With Previous Shipping Cost Submit To Biddyut/iPost Via API.
- Logistics Collect Product From Pickup Location & Delivery To Destination/Customer .
- Customer Address Customized as Country->Region/State/Division->City->Township/Zone

Tested: Magento 2.2.3


install:
=======================================
-- More Details please check doc folder

# magento2-Biddyut- Sslwireless_Biddyut
# magento2-address- Sslwireless_Address



## magento2-Biddyut- Sslwireless_Biddyut
=======================================
 -Shipping Charge Calculator via API
 -Dependency module  SSLWireless Address(https://github.com/sslcommerz)






## magento2-address- Sslwireless_Address
============

Make city and township as dropdown

The module is working with magento 2.1.x, if you are using magento 2.2.x, you need rename 2 files
app\code\Sslwireless\Address\view\base\ui_component\customer_form_22.xml
app\code\Sslwireless\Address\view\frontend\templates\address\edit22.phtml

After installed, pls go to admin > customer > import address and use my sample csv in data folder to import. The order to import is regions > cities > townships (if you dont use township, you can ignore it)

Address template configuration (Stores > Configuration > Customer Configuration > Address template) - use this or change element sort order depend on your purpose

Text

{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}
{{depend company}}{{var company}}{{/depend}}
{{if street1}}{{var street1}}
{{/if}}
{{depend street2}}{{var street2}}{{/depend}}
{{depend street3}}{{var street3}}{{/depend}}
{{depend street4}}{{var street4}}{{/depend}}
{{if city}}{{var city}}, {{/if}}{{if township}}{{var township}}, {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}
{{var country}}
{{depend telephone}}T: {{var telephone}}{{/depend}}
{{depend fax}}F: {{var fax}}{{/depend}}
{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}

==================================
Text One Line

{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var township}}, {{var region}}, {{var postcode}}, {{var country}}

==================================
HTML

{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend firstname}}<br />{{/depend}}
{{depend company}}{{var company}}<br />{{/depend}}
{{if street1}}{{var street1}}<br />{{/if}}
{{depend street2}}{{var street2}}<br />{{/depend}}
{{depend street3}}{{var street3}}<br />{{/depend}}
{{depend street4}}{{var street4}}<br />{{/depend}}
{{if city}}{{var city}}, {{/if}}{{if township}}{{var township}}, {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}<br />
{{var country}}<br />
{{depend telephone}}T: <a href="tel:{{var telephone}}">{{var telephone}}</a>{{/depend}}
{{depend fax}}<br />F: {{var fax}}{{/depend}}
{{depend vat_id}}<br />VAT: {{var vat_id}}{{/depend}}

==================================

PDF

{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}|
{{depend company}}{{var company}}|{{/depend}}
{{if street1}}{{var street1}}|{{/if}}
{{depend street2}}{{var street2}}|{{/depend}}
{{depend street3}}{{var street3}}|{{/depend}}
{{depend street4}}{{var street4}}|{{/depend}}
{{if city}}{{var city}}, {{/if}}{{if township}}{{var township}}, {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}|
{{var country}}|
{{depend telephone}}T: {{var telephone}}|{{/depend}}
{{depend fax}}F: {{var fax}}|{{/depend}}|
{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}|






Refarance:
https://cedcommerce.com/magento-2-module-creator/shipping-module
https://github.com/cedcommerce/magento-2-sample-module
https://ranasohel.me/2015/11/28/how-to-add-custom-field-to-shipping-address-form-in-magento-2-onepage-checkout/
https://devdocs.magento.com/guides/v2.2/extension-dev-guide/events-and-observers.html
https://www.mageplaza.com/magento-2-module-development/magento-2-events.html
https://marketplace.magento.com/maurisource-shipstation-liverate.html
https://www.magecloud.net/marketplace/extension/shipping-agent-for-magento/
https://www.iwdagency.com/extensions/order-manager-m2.html
https://magehit.com/blog/how-to-use-rest-api-in-magento-2/
http://www.webnexs.com/blog/kb/get-value-custom-attribute-magento-2-rest-api/
https://github.com/baddwin/magento2-ongkir
https://github.com/netresearch/dhl-module-shipping-m2
https://github.com/sohelrana09/magento2-module-checkoutadditionalfield
https://github.com/vincent2090311/magento2-address
https://github.com/sohelrana09/module-auto-invoice-shipment



Development Team:
=======================================
 * @Biddyut(A technology driven Logistics & delivery company Bangladesh) Magento 2.x
 * @Package       Biddyut Limited
 * @Developer     Abdul Matin <matinict@gmail.com>
 * @Author        Sslwireless(https://github.com/sslcommerz)
 * @Dependency    SSLWireless Address(https://github.com/sslcommerz)

---

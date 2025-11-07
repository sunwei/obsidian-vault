
{

"mcpServers": {

"aupro": {

"command": "aupro",

"args": ["serve"],
"env": {

"AUPRO_MOCK_TEAM": "1",

"AUPRO_ENV": "dev",

"AUPRO_API_KEY": "AIzaSyAwpdQp3BHdpKcSmWo5aW9-WYtyr_PsLdQ"

}

}

}

}

SELECT Id,
    Name,
    pse__Opportunity__r.Opportunity_Contract_Value__c,
    pse__Opportunity__r.Contract_Type__c,
    pse__Opportunity__r.CurrencyIsoCode,
    pse__Opportunity__r.Region__c,
    pse__Opportunity__r.Market__c
FROM pse__Proj__c
WHERE Id = 'a17UZ00001NxoBC'
    LIMIT 1


SELECT Id, Opportunity__c, Delivery_Approver__c, Delivery_Approver__r.Name, Demand_Approver__c, Demand_Approver__r.Name, Legal_Approver__c, Legal_Approver__r.Name, Finance_Approver__c, Finance_Approver__r.Name FROM Deal_Review__c where Opportunity__c = ''



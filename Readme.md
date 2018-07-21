=================== Instructions to Run this Demo ===========================================
1 - Download the "SalesforceOrgConnector-Salesforce" public Repository.
2 - Deploy the ANT script package in your Org.
3 - Upload the custom setting data with following Commands.

 Org_Connector_Config__c orgConfig = new Org_Connector_Config__c();
        orgConfig.SetupOwnerId = '00eC00000016HQP';
        orgConfig.Base_URL_Login__c = 'https://login.salesforce.com';
        orgConfig.Base_URL_Test__c = 'https://test.salesforce.com';
        orgConfig.Client_Id_URL__c = 'response_type=code&client_id=';
        orgConfig.Client_Secret_Key__c = '8925104254922037428';
        orgConfig.Connection_Type_Self__c = 'Self';
        orgConfig.Consumer_Key__c = '3MVG9U_dUptXGpYIWl6U3CZVSnm328FAYkPepRbR.ssNcbdf35_nwe0VM9AhU5imA3lDtAiuRKQriLZ4IBPKR'; 
        orgConfig.Login_Hint__c  = 'login_hint=';
        orgConfig.Oath_Token_Url__c = '.salesforce.com/services/oauth2/token';
        orgConfig.OAuth_URL__c = '/services/oauth2/authorize';
        orgConfig.OrgType_Production_developer__c = 'Production/Developer';
        orgConfig.Prompt_Encoded__c = 'prompt=login%20consent';
        orgConfig.Redirect_URI__c = 'redirect_uri=';
        orgConfig.Redirect_URL__c = 'https://orgconnector.herokuapp.com/createConnection?cs=hello' ;
        orgConfig.Self_Connection__c = 'Self Connection';
        orgConfig.State_URI__c = 'state='; 
        insert orgConfig;
        
        Org_Connector_Config_Validation__c configValidation = new Org_Connector_Config_Validation__c();
        configValidation.Duplicate_External_Connection__c = 'Connection name already exist,'; 
        configValidation.Duplicate_Local_Connection__c = 'Self Connection already exist.';
        configValidation.Invalid_Connection_Name__c ='Enter valid connection name';
        configValidation.Local_Connection_Absent__c = 'Create Self Connection to continue';
        configValidation.OrgType_Not_Selected__c = 'Select org type';
        configValidation.Username_length_error__c = 'Connection Name can have at max 60 characters' ;
        configValidation.SetupOwnerId = '00eC00000016HQP';
        insert configValidation;
        
  4 - Create your own three Connected App, Replace Client Id, Client Secret key in the Apex controller, which are hardcoded.
  5 - Now setup a Java-Heroku Project.
  6 - Download the "SalesforceOrgConnector-Java" public Repository.
  7 - Setup Maven in your machin.
  8 - Import the downloaded project as a maven project in eclipse.
  9 - Create Heroku Application.
  10 - Upload this package in that Heroku Application.
  11 - Few adjustment needs to done on the Java side. Make sure to set correct java path in the project -> Pom.xml as per your system installation directory.
  12 - Replace Consumere Key, client secret key, redirect url with your connected app configuration.
  13 - Create Remote Site setting with your Heroku App end point.
  14 - Set "OAuth Demo" as your logged in App.
  15 - Now run the all the demo with the tab name "CreateConnection1", "CreateConnection2", "CreateConnection3", "Retrieve Org Data - OAuth".
  16 - In case any issue reach out to my personal mail id. "rajeev.161988@gmail.com" or can reach out to my twitter log in "rajeevjain16".
 

# SqlClient_issue_1418

IIS Site Configration

Site configuration in applicationHost.config

    <site name="SqlClientTest" id="23">
        <application path="/" applicationPool="SqlClientTest">
            <virtualDirectory path="/" physicalPath="L:\WebApplication1\" />
        </application>
        <application path="/t" applicationPool="SqlClientTest">
            <virtualDirectory path="/" physicalPath="L:\WebApplication1\" />
        </application>
        <bindings>
            <binding protocol="http" bindingInformation="*:8780:" />
        </bindings>
    </site>


Test web request to URLs: 
- http://localhost:8780/t/api/values
- http://localhost:8780/api/values
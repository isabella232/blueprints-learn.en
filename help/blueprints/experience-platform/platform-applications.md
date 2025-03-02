---
title: Adobe Experience Platform & Applications architecture diagram
description: This architecture diagram shows how Adobe Experience Platform relates to other Adobe Experience Cloud applications and application services.
solution: Experience Platform, Campaign, Analytics, Target, Customer Journey Analytics, Journey Orchestration, Offer Decisioning, Real-time Customer Data Platform
kt: 7199
thumbnail:
exl-id: 9b12cd7a-5e5f-443a-91a1-44273cdabc2d
---
# Adobe Experience Platform & Applications

## Adobe Experience Platform & Applications architecture diagram

This architecture diagram shows how Adobe Experience Platform relates to Adobe Experience Cloud applications and application services.

<img src="assets/aep+apps_vertical.svg" alt="Experience Platform & Applications" style="border:1px solid #4a4a4a; width:90%;" />

>[!VIDEO](https://video.tv.adobe.com/v/32456/?quality=12&learn=on)

## Adobe Experience Platform & Applications detailed architecture diagram

<img src="assets/aep+apps_horizontal.svg" alt="Experience Platform & Applications" style="border:1px solid #4a4a4a; width:90%;" />

## Adobe Experience Platform & Experience Cloud Application Integrations

<table class="relative-table wrapped" style="width: 100%;" >
   <colgroup>
    <col style="width: 16.0202%;"/>
    <col style="width: 29.3423%;"/>
    <col style="width: 33.5582%;"/>
    <col style="width: 21.0793%;"/>
  </colgroup>
  <tbody>
    <tr>
      <th>Application</th>
      <th>Experience Platform to Application</th>
      <th>Application to Experience Platform</th>
      <th>Related Blueprints</th>
    </tr>
    <tr>
      <td colspan="1">Ad Cloud</td>
      <td colspan="1">
        <ul>
          <li>Audiences defined in Real-time Customer Data Platform can be shared to Ad Cloud for targeting via Audience Manager.</li>
        </ul>
      </td>
      <td colspan="1">No current integration</td>
      <td colspan="1">
        <ul>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/audience-activation/anonymous.html?lang=en">Anonymous Audience Activation</a>
          </li>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/audience-activation/online-offline.html?lang=en">Online/Offline Audience Activation</a>
          </li>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/audience-activation/platform-and-applications.html?lang=en">Activation with Experience Platform and Applications</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Analytics</td>
      <td>No current integration</td>
      <td>
        <ul>
          <li>Data collected by Analytics can be sent to Experience Platform data lake and profile store. <a href="https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=en">Analytics Data Connector</a>
          </li>
        </ul>
      </td>
      <td>
        <ul>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/architecture-overview/platform-data-flow.html?lang=en">Experience Platform Data flows</a>
          </li>
        </ul>
        <p>
          <br/>
        </p>
      </td>
    </tr>
    <tr>
      <td>Audience Manager</td>
      <td>
        <ul>
          <li>Audiences defined in Real-time Customer Data Platform can be shared to Audience Manager for activation to 3rd party cookie destinations.</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Data collected and evaluated audience membership can be shared to Experience Platform data lake and profile store. <a href="https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/audience-manager.html?lang=en">Audience Manager Source Connector</a>
          </li>
        </ul>
      </td>
      <td>
        <ul>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/audience-activation/anonymous.html?lang=en">Anonymous Audience Activation</a>
          </li>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/audience-activation/online-offline.html?lang=en">Online/Offline Audience Activation</a>
          </li>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/audience-activation/platform-and-applications.html?lang=en">Activation with Experience Platform and Applications</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td colspan="1">Campaign Classic</td>
      <td colspan="1">
        <ul>
          <li>Audiences defined in Real-time Customer Data Platform can be shared to Campaign Classic as the audience to initiate campaigns.</li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>Interaction and campaign data collected by Campaign can be ingested to Experience Platform as a data source for further use in audience building via Real-time Customer Data Platform and analysis via Customer Journey Analytics and Experience Platform Query Service and Data Science Workspace.</li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/customer-journeys/batch-messaging.html?lang=en">Batch Messaging</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td colspan="1">Campaign Standard</td>
      <td colspan="1">
        <ul>
          <li>Audiences defined in Real-time Customer Data Platform can be shared to Campaign Standard as the audience to initiate campaigns.</li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>Interaction and campaign data collected by Campaign can be ingested to Experience Platform as a data source for further use in audience building via Real-time Customer Data Platform and analysis via Customer Journey Analytics and Experience Platform Query Service and Data Science Workspace.</li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/customer-journeys/batch-messaging.html?lang=en">Batch Messaging</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td colspan="1">Customer Journey Analytics</td>
      <td colspan="1">
        <ul>
          <li>Data collected and ingested into Experience Platform data lake is made available for processing into Customer Journey Analytics. </li>
        </ul>
      </td>
      <td colspan="1">No current integration available. The ability to share audience results to Experience Platform from Customer Journey Analytics is on the roadmap.</td>
      <td colspan="1">
        <ul>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/customer-journey-analytics/overview.html?lang=en">Customer Journey Analytics</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td colspan="1">Experience Manager</td>
      <td colspan="1">
        <ul>
          <li>The Experience Platform profile can be directly accessed server side to power personalized experiences delivered through Experience Manager. Note that personalization activities are most commonly delivered via Experience Manager through the Target integration. </li>
        </ul>
      </td>
      <td colspan="1">No current integration, behaviors and interactions performed on Experience Manager sites are collected directly via the Experience Platform Web and Mobile SDK.</td>
      <td colspan="1">
        <ul>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/audience-activation/online-offline.html?lang=en">Online/Offline Audience Activation</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td colspan="1">Journey Optimizer</td>
      <td colspan="1">
        <ul>
          <li>Data events and profiles ingested into Experience Platform are made available to Journey Optimizer to initiate and power journeys in Journey Optimizer.</li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>Interaction and campaign data produced by Journey Optimizer is collected into Experience Platform for further use in audience building via Real-time Customer Data Platform and analysis via Customer Journey Analytics, Experience Platform Query Service and Data Science Workspace.</li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/customer-journeys/journey-optimizer.html?lang=en">Journey Optimizer</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td colspan="1">Magento</td>
      <td colspan="1">No current integration</td>
      <td colspan="1">No current integration</td>
      <td colspan="1">No current integration</td>
    </tr>
    <tr>
      <td colspan="1">Marketo</td>
      <td colspan="1">
        <ul>
          <li>Audiences defined in Real-time Customer Data Platform can be shared to Marketo as the audience to initiate Marketo campaigns and update Marketo objects.</li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>Marketo accounts, contacts, and opportunity data, along with Interaction and campaign data produced by Marketo is ingested into Experience Platform for further use in audience building via B2B-CDP and analysis via Customer Journey Analytics, Experience Platform Query Service and Data Science Workspace. <a href="https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo.html?lang=en">Marketo Engage Connector</a>
          </li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>B2B Activation - in development</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td colspan="1">Real-time CDP</td>
      <td colspan="1">
        <ul>
          <li>Data ingested and collected into Experience Platform is the data source for assembling real-time customer profiles that power the Real-time Customer Data Platform.</li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>Audience and Profile metrics are sent to the Experience Platform data lake to power profile insight reporting dashboards.</li>
          <li>The Audience and Profile data in the data lake can be used for further insights via Query Service, Data Science Workspace, and Customer Journey Analytics.</li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/audience-activation/online-offline.html?lang=en">Online/Offline Audience Activation</a>
          </li>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/audience-activation/platform-and-applications.html?lang=en">Activation with Experience Platform and Applications</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td colspan="1">Target</td>
      <td colspan="1">
        <ul>
          <li>Audiences defined in Real-time Customer Data Platform can be shared to Target and used in personalization and targeting experiences delivered by Target. </li>
          <li>Direct Experience Edge integration with Target for real-time segment membership and profile attribute access is on the roadmap.</li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>Data collected for Target experiences and interactions can be collected to Experience Platform via the Experience Platform Web SDK. This data can be used in audience building via the Real-time Customer Data Platform and for analysis via Customer Journey Analytics,  Experience Platform Query Service and Data Science Workspace.</li>
        </ul>
      </td>
      <td colspan="1">
        <ul>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/audience-activation/online-offline.html?lang=en">Online/Offline Audience Activation</a>
          </li>
          <li>
            <a href="https://experienceleague.adobe.com/docs/blueprints-learn/architecture/audience-activation/platform-and-applications.html?lang=en">Activation with Experience Platform and Applications</a>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

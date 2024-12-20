<h1> Rapid Deployment DataEase Community Edition </h1>

<h2> Service Description </h2>

<p>DataEase is an open source data visualization analysis tool that helps users quickly analyze data and gain insight into business trends to achieve business improvement and optimization.
DataEase supports rich data source connections, you can quickly create charts by dragging and dropping, and you can easily share them with others. For more information, see <a href = "https://dataease.io/docs/v2/">DataEase website </a>. </p>

<h2> Service Architecture </h2>

<p>DataEase community edition service is deployed on a stand-alone ecs instance. </p>

<p><img src="architecture_ecs_single.png" width="600" height="400" align="bottom"/></p>

<h2> Billing instructions </h2>

<p> The DataEase Community Edition service itself is free of charge. <br />
When a user deploys a built service, the resource costs are mainly related:
-The type of the selected ECS instance
-Disk Capacity
-Internet bandwidth </p>

<p> Billing methods include:
-Pay-As-You-Go (hours)
-Package year and package month </p>

<p> Estimated costs can be seen in real time before deployment. </p>

<h2> Permissions required for RAM accounts </h2>

<p> The DataEase Community Edition service needs to access and create resources such as ECS and VPC. If you use a RAM user to create a service instance, you need to add the corresponding resource permissions to the account of the RAM user before creating the service instance. For more information about how to add RAM permissions, see <a href = "https://help.aliyun.com/document_detail/121945.html"> Authorize RAM users </a>. The required permissions are shown in the following table:</p>

<table>
<thead>
<tr>
<th> Permission policy name </th>
<th> Remarks </th>
</tr>
</thead>
<tbody>
<tr>
<td>AliyunECSFullAccess</td>
<td> Permissions to manage ECS </td>
</tr>
<tr>
<td>AliyunVPCFullAccess</td>
<td> Permissions for managing VPC networks </td>
</tr>
<tr>
<td>AliyunROSFullAccess</td>
<td> Manage permissions for Resource Orchestration Services (ROS) </td>
</tr>
<tr>
<td>AliyunComputeNestUserFullAccess</td>
<td> Manage user-side permissions for the compute nest service (ComputeNest) </td>
</tr>
<tr>
<td>AliyunComputeNestSupplierFullAccess</td>
<td> Manage service provider-side permissions for computing nest services (ComputeNest) |</td>
</tr>
</tbody>
</table>

<h2> Service instance deployment process </h2>

<h3> Deployment parameters </h3>

<table>
<thead>
<tr>
<th> Parameter group </th>
<th> Parameter item </th>
<th> Description </th>
</tr>
</thead>
<tbody>
<tr>
<td> Service instance </td>
<td> Service instance name </td>
<td> must be no more than 64 characters in length and must start with an English letter. It can contain numbers, English letters, dashes (-), and underscores (_). </td>
</tr>
<tr>
<td></td>
<td> Region </td>
<td> The region where the service instance is deployed. </td>
</tr>
<tr>
<td></td>
<td> Payment type </td>
<td> The billing type of the resource: Pay-As-You-Go and Subscription. </td>
</tr>
<tr>
<td>ECS instance configuration </td>
<td> Instance type </td>
<td>ECS instance specifications. </td>
</tr>
<tr>
<td></td>
<td> Instance password </td>
<td> is 8-30 in length and must contain three items (uppercase letters, lowercase letters, numbers, special symbols in ()'~!@#$%^& *-+ =|{}[]:;' <>,.?/). </td>
</tr>
<tr>
<td> Network configuration </td>
<td> Availability Zone </td>
<td> The zone where the ECS instance is located. </td>
</tr>
<tr>
<td></td>
<td> VPC instance ID</td>
<td> The ID of the VPC where the ECS instance is located. </td>
</tr>
<tr>
<td></td>
<td> Switch instance ID</td>
<td> The ID of the VSwitch where the ECS instance is located. </td>
</tr>
</tbody>
</table>

<h3> Deployment steps </h3>

<ol>
<li> Click <a href = "https://computenest.console.aliyun.com/service/instance/create/cn-hangzhou?type=user&ServiceName=DataEase社区版"> Deployment Link </a> to go to the Service Instance Deployment page.
<img src="img.png" alt="img.png" /></li>
<li> according to the interface prompt to configure parameters, select ECS instance type and set parameters such as available area. after the configuration is completed, click next: confirm the order.
<img src="img_1.png" alt="img_1.png" /></li>
<li> After confirming that there is no problem with the order, click Create Now, and the service instance enters the creation process.
<img src="img_2.png" alt="img_2.png" /></li>
<li> After the service instance is created, go to the service instance details page to obtain the access address of the service instance.
<img src="img_4.png" alt="img_4.png" /></li>
<li> click the access address, enter the default account number: admin, and the default password: DataEase @ 123456 to access.
<img src="img_5.png" alt="img<em>5.png" />
<img src="img_6.png" alt="img</em>6.png" /></li>
</ol>

# 弹性伸缩实例<a name="ZH-CN_TOPIC_0120434955"></a>

<a name="table195929912148"></a>
<table><thead align="left"><tr id="row65927971413"><th class="cellrowborder" valign="top" width="47%" id="mcps1.1.5.1.1"><p id="p135221579017"><a name="p135221579017"></a><a name="p135221579017"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="13%" id="mcps1.1.5.1.2"><p id="p87863593711"><a name="p87863593711"></a><a name="p87863593711"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="16%" id="mcps1.1.5.1.3"><p id="p17522185717013"><a name="p17522185717013"></a><a name="p17522185717013"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="24%" id="mcps1.1.5.1.4"><p id="p1841555914555"><a name="p1841555914555"></a><a name="p1841555914555"></a>授权作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row1059211912142"><td class="cellrowborder" valign="top" width="47%" headers="mcps1.1.5.1.1 "><p id="p12592109161413"><a name="p12592109161413"></a><a name="p12592109161413"></a>GET /autoscaling-api/v1/{project_id}/scaling_group_instance/{scaling_group_id}/list</p>
</td>
<td class="cellrowborder" valign="top" width="13%" headers="mcps1.1.5.1.2 "><p id="p14210743158"><a name="p14210743158"></a><a name="p14210743158"></a>查询弹性伸缩组中的实例列表</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.3 "><p id="p135921795142"><a name="p135921795142"></a><a name="p135921795142"></a>as:instances:list</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.4 "><a name="ul159418416586"></a><a name="ul159418416586"></a><ul id="ul159418416586"><li>支持：<a name="ul12943144113582"></a><a name="ul12943144113582"></a><ul id="ul12943144113582"><li>项目(Project)</li><li>企业项目(Enterprise Project)</li></ul>
</li></ul>
<a name="ul14945174175813"></a><a name="ul14945174175813"></a><ul id="ul14945174175813"><li>不支持：无</li></ul>
</td>
</tr>
<tr id="row195927915143"><td class="cellrowborder" valign="top" width="47%" headers="mcps1.1.5.1.1 "><p id="p859219915140"><a name="p859219915140"></a><a name="p859219915140"></a>DELETE /autoscaling-api/v1/{project_id}/scaling_group_instance/{instance_id}</p>
</td>
<td class="cellrowborder" valign="top" width="13%" headers="mcps1.1.5.1.2 "><p id="p19210043159"><a name="p19210043159"></a><a name="p19210043159"></a>移出弹性伸缩组实例</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.3 "><p id="p1059249141411"><a name="p1059249141411"></a><a name="p1059249141411"></a>as:instances:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.4 "><a name="ul1985675217116"></a><a name="ul1985675217116"></a><ul id="ul1985675217116"><li>支持：<a name="ul685845211117"></a><a name="ul685845211117"></a><ul id="ul685845211117"><li>项目(Project)</li><li>企业项目(Enterprise Project)</li></ul>
</li></ul>
<a name="ul17859105211114"></a><a name="ul17859105211114"></a><ul id="ul17859105211114"><li>不支持：无</li></ul>
</td>
</tr>
<tr id="row55926921417"><td class="cellrowborder" valign="top" width="47%" headers="mcps1.1.5.1.1 "><p id="p159219901417"><a name="p159219901417"></a><a name="p159219901417"></a>POST /autoscaling-api/v1/{project_id}/scaling_group_instance/{scaling_group_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="13%" headers="mcps1.1.5.1.2 "><p id="p8210134318511"><a name="p8210134318511"></a><a name="p8210134318511"></a>批量操作实例</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.3 "><p id="p5592090148"><a name="p5592090148"></a><a name="p5592090148"></a>as:instances:batchAction</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.4 "><a name="ul19673454131111"></a><a name="ul19673454131111"></a><ul id="ul19673454131111"><li>支持：<a name="ul1467414544117"></a><a name="ul1467414544117"></a><ul id="ul1467414544117"><li>项目(Project)</li><li>企业项目(Enterprise Project)</li></ul>
</li></ul>
<a name="ul166751547118"></a><a name="ul166751547118"></a><ul id="ul166751547118"><li>不支持：无</li></ul>
</td>
</tr>
</tbody>
</table>


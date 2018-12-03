# 配额<a name="ZH-CN_TOPIC_0120460558"></a>

<a name="table136899111019"></a>
<table><thead align="left"><tr id="row76812917100"><th class="cellrowborder" valign="top" width="45%" id="mcps1.1.5.1.1"><p id="p135221579017"><a name="p135221579017"></a><a name="p135221579017"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="15%" id="mcps1.1.5.1.2"><p id="p1745194914208"><a name="p1745194914208"></a><a name="p1745194914208"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="16%" id="mcps1.1.5.1.3"><p id="p17522185717013"><a name="p17522185717013"></a><a name="p17522185717013"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="24%" id="mcps1.1.5.1.4"><p id="p197010343178"><a name="p197010343178"></a><a name="p197010343178"></a>授权作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row3682093107"><td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.5.1.1 "><p id="p106810921012"><a name="p106810921012"></a><a name="p106810921012"></a>GET /autoscaling-api/v1/{project_id}/quotas</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.5.1.2 "><p id="p18112181072314"><a name="p18112181072314"></a><a name="p18112181072314"></a>查询配额</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.3 "><p id="p76899181011"><a name="p76899181011"></a><a name="p76899181011"></a>as:quotas:get</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.4 "><a name="ul7919182815165"></a><a name="ul7919182815165"></a><ul id="ul7919182815165"><li>支持：<p id="p129223283164"><a name="p129223283164"></a><a name="p129223283164"></a>项目(Project)</p>
</li></ul>
<a name="ul992522819168"></a><a name="ul992522819168"></a><ul id="ul992522819168"><li>不支持：<p id="p4926142811616"><a name="p4926142811616"></a><a name="p4926142811616"></a>企业项目(Enterprise Project)</p>
</li></ul>
</td>
</tr>
<tr id="row868149161012"><td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.5.1.1 "><p id="p196810941019"><a name="p196810941019"></a><a name="p196810941019"></a>GET /autoscaling-api/v1/{project_id}/quotas/{scaling_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.5.1.2 "><p id="p111221072312"><a name="p111221072312"></a><a name="p111221072312"></a>查询弹性伸缩策略和伸缩实例配额</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.3 "><p id="p36817981011"><a name="p36817981011"></a><a name="p36817981011"></a>as:quotas:get</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.4 "><a name="ul6814438192415"></a><a name="ul6814438192415"></a><ul id="ul6814438192415"><li>支持：<p id="p11814138172415"><a name="p11814138172415"></a><a name="p11814138172415"></a>项目(Project)</p>
</li></ul>
<a name="ul15814238122410"></a><a name="ul15814238122410"></a><ul id="ul15814238122410"><li>不支持：<p id="p2081453815243"><a name="p2081453815243"></a><a name="p2081453815243"></a>企业项目(Enterprise Project)</p>
</li></ul>
</td>
</tr>
</tbody>
</table>


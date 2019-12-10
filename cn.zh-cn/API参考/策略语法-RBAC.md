# 策略语法：RBAC<a name="zh-cn_topic_201905307"></a>

策略结构包括：策略版本号（Version）、策略授权语句（Statement）和策略依赖（Depends）。

**图 1**  策略结构<a name="fig1397664112403"></a>  
![](figures/策略结构-3.jpg "策略结构-3")

## 策略语法<a name="section186518419401"></a>

如下以AS服务的“AutoScaling Administraor”为例，说明RBAC策略语法组成。

![](figures/策略语法RBAC.png)

```
{
        "Version": "1.0",
        "Statement": [
                {
                        "Effect": "Allow",
                        "Action": [
                                "as:*:*",
                                "evs:*:get",
                                "evs:*:list",
                                "vpc:*:get",
                                "vpc:*:list",
                                "ims:*:get*",
                                "ims:*:list*",
                                "ecs:*:get",
                                "ecs:*:list",
                                "eps:*:list"
                        ]
                }
        ],
        "Depends": [
                {
                        "catalog": "BASE",
                        "display_name": "Server Administrator"
                },
                {
                        "catalog": "ELB",
                        "display_name": "ELB Administrator"
                }，
                {
                        "catalog": "CES",
                        "display_name": "CES Administrator"
                }，
                {
                        "catalog": "BASE",
                        "display_name": "Tenant Guest"
                }
        ]
}
```

**表 1**  参数说明

<a name="table686894111405"></a>
<table><thead align="left"><tr id="row8977194116407"><th class="cellrowborder" colspan="2" valign="top" id="mcps1.2.5.1.1"><p id="p39781241114018"><a name="p39781241114018"></a><a name="p39781241114018"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" id="mcps1.2.5.1.2"><p id="p1297854111403"><a name="p1297854111403"></a><a name="p1297854111403"></a>含义</p>
</th>
<th class="cellrowborder" valign="top" id="mcps1.2.5.1.3"><p id="p1997820417408"><a name="p1997820417408"></a><a name="p1997820417408"></a>值</p>
</th>
</tr>
</thead>
<tbody><tr id="row2978204118404"><td class="cellrowborder" colspan="2" valign="top" headers="mcps1.2.5.1.1 "><p id="p169788418405"><a name="p169788418405"></a><a name="p169788418405"></a>Version</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p0978154118407"><a name="p0978154118407"></a><a name="p0978154118407"></a>策略的版本</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p18978041204015"><a name="p18978041204015"></a><a name="p18978041204015"></a>固定为“1.0”</p>
</td>
</tr>
<tr id="row19978194174010"><td class="cellrowborder" rowspan="2" valign="top" width="17.17171717171717%" headers="mcps1.2.5.1.1 "><p id="p2978134194016"><a name="p2978134194016"></a><a name="p2978134194016"></a>Statement</p>
</td>
<td class="cellrowborder" valign="top" width="17.17171717171717%" headers="mcps1.2.5.1.1 "><p id="p5978241124017"><a name="p5978241124017"></a><a name="p5978241124017"></a>Action</p>
</td>
<td class="cellrowborder" valign="top" width="28.28282828282828%" headers="mcps1.2.5.1.2 "><p id="p197884124015"><a name="p197884124015"></a><a name="p197884124015"></a>定义对AS的具体操作。</p>
</td>
<td class="cellrowborder" valign="top" width="37.37373737373737%" headers="mcps1.2.5.1.3 "><p id="p1697818417400"><a name="p1697818417400"></a><a name="p1697818417400"></a>格式为：服务名:资源类型:操作</p>
<p id="p1497814418409"><a name="p1497814418409"></a><a name="p1497814418409"></a>"AS:*:*"，表示对AS的所有操作，其中AS为服务名称；“*”为通配符，表示对所有的资源类型可以执行所有操作。</p>
</td>
</tr>
<tr id="row397894115403"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p12978194117405"><a name="p12978194117405"></a><a name="p12978194117405"></a>Effect</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1497864111402"><a name="p1497864111402"></a><a name="p1497864111402"></a>定义Action中所包含的具体操作是否允许执行。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><a name="ul2978204144018"></a><a name="ul2978204144018"></a><ul id="ul2978204144018"><li>Allow：允许执行。</li><li>Deny：不允许执行。</li></ul>
</td>
</tr>
<tr id="row8979114154018"><td class="cellrowborder" rowspan="2" valign="top" width="17.17171717171717%" headers="mcps1.2.5.1.1 "><p id="p1597964154011"><a name="p1597964154011"></a><a name="p1597964154011"></a>Depends</p>
</td>
<td class="cellrowborder" valign="top" width="17.17171717171717%" headers="mcps1.2.5.1.1 "><p id="p2979154164017"><a name="p2979154164017"></a><a name="p2979154164017"></a>catalog</p>
</td>
<td class="cellrowborder" valign="top" width="28.28282828282828%" headers="mcps1.2.5.1.2 "><p id="p1797954114015"><a name="p1797954114015"></a><a name="p1797954114015"></a>依赖的策略的所属服务。</p>
</td>
<td class="cellrowborder" valign="top" width="37.37373737373737%" headers="mcps1.2.5.1.3 "><p id="p13979741144010"><a name="p13979741144010"></a><a name="p13979741144010"></a>服务名称</p>
<p id="p2979134114409"><a name="p2979134114409"></a><a name="p2979134114409"></a>例如：ELB</p>
</td>
</tr>
<tr id="row69791441184017"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p129791941124012"><a name="p129791941124012"></a><a name="p129791941124012"></a>display_name</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1297964114407"><a name="p1297964114407"></a><a name="p1297964114407"></a>依赖的策略的名称。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p89791741154019"><a name="p89791741154019"></a><a name="p89791741154019"></a>权限名称</p>
<p id="p997913418405"><a name="p997913418405"></a><a name="p997913418405"></a>例如：ELB Administrator</p>
</td>
</tr>
</tbody>
</table>


# stata_dta
可运行statadta合集



*====================lalonde.dta
use https://friosavila.github.io/playingwithstata/drdid/lalonde.dta, clear

*这个数据是用于评估培训计划是否提高了个人收入，特别是在应用DID和drdid等方法时非常常用。
*	re表示收入
*	treated	是否接受培训（处理变量）


*=====================wagepan_twfeweights.dta
use "https://raw.githubusercontent.com/chaisemartinPackages/twowayfeweights/main/wagepan_twfeweights.dta", clear

* 用于演示和测试关于双向固定效应权重（Two-way Fixed Effects Weights）分析的面板数据。
/* 
核心变量解释
变量名	类型	说明
nr	float	人员编号（person identifier），唯一标识一个个体
year	float	年份，从1980年到1987年
black	float	是否为黑人，=1 表示是黑人，=0 或缺失表示不是
exper	float	劳动力市场工作经验，通常指年数
hisp	float	是否为西班牙裔，=1 表示是西班牙裔
hours	float	年度工作小时数
married	float	婚姻状况，=1 表示已婚

职业类别（哑变量，binary）
这些变量表示个体所属的职业类别，=1 表示属于该职业类别，否则为0。

变量名	说明
occ1	专业、技术及相关工作（Professional, Technical and kindred）
occ2	经理、官员和业主（Managers, Officials and Proprietors）
occ3	销售人员（Sales Workers）
occ4	文员及相关（Clerical and kindred）
occ5	工匠、工头及相关（Craftsmen, Foremen and kindred）
occ6	操作工及相关（Operatives and kindred）
occ7	工人和农民（Laborers and farmers）
occ8	农场工人和工头（Farm Laborers and Foreman）
occ9	服务人员（Service Workers）

教育与工会状态
变量名	说明
educ	受教育年数（years of schooling）
union	是否加入工会，=1 表示加入

工资变量
变量名	说明
lwage	工资的对数（log(wage)），用于回归等分析更符合正态分布

年份哑变量
变量名	说明
d81-d87	分别对应1981年至1987年，=1 表示该行数据对应该年份

经验平方项
变量名	说明
expersq	工作经验的平方（exper²），用于捕捉非线性经验效应

差分变量
变量名	说明
diff_lwage	工资对数的差分（可能是某个时间段的变化）
diff_union	工会状态的差分（是否加入或退出工会）

*/


*=================================state_policy_effect.dta
use https://github.com/joshbleiberg/stacked_event/raw/main/state_policy_effect.dta, clear



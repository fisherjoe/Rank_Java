# Rank_Java
功能：从一个无序列表中分析树形结构并输出

		
		//造数据
		List<HashMap<String, Object>> demoData = new ArrayList<HashMap<String, Object>>();
		for(int i = 0; i < 20; i++){
			HashMap<String, Object> item = new HashMap<String, Object>();
			item.put("name", "name" + i);
			item.put("id", String.valueOf(i + 1));
			String pid = null;
			if(i % 5 == 0){
				pid = "0";
			}else{
				pid = String.valueOf(random(i + 1));
			}
			item.put("pid", pid);
			demoData.add(item);
		}
		
		//调用方式
		RankFactory RF = new RankFactory(demoData, "pid", "id");
		List resultData = RF.rank();
		System.out.print(resultData);
		
		输出demo数据：
[{
    id = 1,
    children = [{
        id = 2,
        children = [{
            id = 13,
            children = [{
                id = 18,
                children = [],
                pid = 13,
                name = name17
            }],
            pid = 2,
            name = name12
        },
        {
            id = 14,
            children = [{
                id = 17,
                children = [],
                pid = 14,
                name = name16
            }],
            pid = 2,
            name = name13
        }],
        pid = 1,
        name = name1
    },
    {
        id = 4,
        children = [{
            id = 5,
            children = [{
                id = 7,
                children = [],
                pid = 5,
                name = name6
            }],
            pid = 4,
            name = name4
        }],
        pid = 1,
        name = name3
    },
    {
        id = 8,
        children = [{
            id = 12,
            children = [],
            pid = 8,
            name = name11
        }],
        pid = 1,
        name = name7
    }],
    pid = 0,
    name = name0
},
{
    id = 3,
    children = [],
    pid = 0,
    name = name2
},
{
    id = 6,
    children = [{
        id = 10,
        children = [],
        pid = 6,
        name = name9
    }],
    pid = 0,
    name = name5
},
{
    id = 9,
    children = [{
        id = 15,
        children = [{
            id = 19,
            pid = 15,
            name = name18
        }],
        pid = 9,
        name = name14
    }],
    pid = 0,
    name = name8
},
{
    id = 11,
    children = [],
    pid = 0,
    name = name10
},
{
    id = 16,
    children = [],
    pid = 0,
    name = name15
},
{
    id = 20,
    pid = 0,
    name = name19
}]

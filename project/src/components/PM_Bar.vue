DesignPage.vue
<template>
    <div class="mybackground"></div>
    <div class="main">
        <div id="PM_BarGraph" class="PM_BarGraphChart"></div>
        <div class="title">
            <p class="my_title">故宫博物院</p>
            <p class="content">
                
            </p>
        </div>
    </div>
</template>


<script>
export default {
    // 图表名称
    name: 'PM_BarGraph',
    methods: {
        myEcharts() {
            const PM_BarGraphChart = this.$echarts.init(
                document.getElementById('PM_BarGraph'),
                null,
                {
                    renderer: 'canvas',
                    useDirtyRect: false
                });
            const colorArray = [
                "#002fa7",
                "#12264f",
                "#206864",
                "#3d8386",
                "#32788a",
                "#5da39d",
                "#6ca8af",
                "#88bfb8",
                "#a4c9cc",
                "#a2d2e2"
            ];
            const option = {
                xAxis: {
                    data: ['旧石器', '新石器', '夏', '商', '周', '春秋', '战国', '秦', '汉', '三国', '魏晋南北朝', '隋', '唐', '五代十国', '宋', '元', '明', '清', '民国', '现当代', '未知'],

                    axisLabel: {
                        interval: 0,  // 设置为0/表示全部显示
                    }
                },
                yAxis: {},
                dataGroupId: '',
                animationDurationUpdate: 500,
                series: {
                    type: 'bar',
                    id: 'sales',
                    data: [
                        {value: 44, groupId: '旧石器时代_1', itemStyle: {color: colorArray[0]}},
                        {value: 909, groupId: '新石器时代_1', itemStyle: {color: colorArray[1]}},
                        {value: 244, groupId: '夏_1', itemStyle: {color: colorArray[2]}},
                        {value: 25946, groupId: '商_1', itemStyle: {color: colorArray[3]}},
                        {value: 2136, groupId: '周_1', itemStyle: {color: colorArray[4]}},
                        {value: 711, groupId: '春秋_1', itemStyle: {color: colorArray[5]}},
                        {value: 10818, groupId: '战国_1', itemStyle: {color: colorArray[6]}},
                        {value: 807, groupId: '秦_1', itemStyle: {color: colorArray[7]}},
                        {value: 24296, groupId: '汉_1', itemStyle: {color: colorArray[8]}},
                        {value: 129, groupId: '三国_1', itemStyle: {color: colorArray[9]}},
                        {value: 987, groupId: '魏晋南北朝_1', itemStyle: {color: colorArray[0]}},
                        {value: 956, groupId: '隋_1', itemStyle: {color: colorArray[1]}},
                        {value: 9173, groupId: '唐_1', itemStyle: {color: colorArray[2]}},
                        {value: 113, groupId: '五代十国_1', itemStyle: {color: colorArray[3]}},
                        {value: 17434, groupId: '宋_1', itemStyle: {color: colorArray[4]}},
                        {value: 5170, groupId: '元_1', itemStyle: {color: colorArray[5]}},
                        {value: 53019, groupId: '明_1', itemStyle: {color: colorArray[6]}},
                        {value: 1049126, groupId: '清_1', itemStyle: {color: colorArray[7]}},
                        {value: 4623, groupId: '民国_1', itemStyle: {color: colorArray[8]}},
                        {value: 705, groupId: '现当代_1', itemStyle: {color: colorArray[9]}},
                        {value: 609213, groupId: '未知_1', itemStyle: {color: colorArray[0]}},
                    ],
                    universalTransition: {
                        enabled: true,
                        divideShape: 'clone'
                    },
                    itemStyle: {}
                }
            };
            const drilldownData = [
                {
                    dataGroupId: '旧石器时代_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 0], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 0], ['文具', 0], ['未知', 0], ['武备仪仗', 0], ['法书', 0], ['漆器', 0], ['玉石器', 44], ['珍宝', 0], ['珐琅器', 0], ['生活用具', 0], ['碑帖', 0], ['织绣', 0], ['绘画', 0], ['金银器', 0], ['钟表仪器', 0], ['铜器', 0], ['铭刻', 0], ['陶瓷', 0], ['雕刻工艺', 0], ['雕塑', 0]]
                },
                {
                    dataGroupId: '新石器时代_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 0], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 0], ['文具', 0], ['未知', 0], ['武备仪仗', 0], ['法书', 0], ['漆器', 0], ['玉石器', 559], ['珍宝', 0], [' 珐琅器', 0], ['生活用具', 0], ['碑帖', 0], ['织绣', 0], ['绘画', 0], ['金银器', 0], ['钟表仪器', 0], ['铜器', 0], ['铭刻', 0], ['陶瓷', 348], ['雕刻工艺', 2], ['雕塑', 0]]
                },
                {
                    dataGroupId: '夏_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 0], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 0], ['文具', 0], ['未知', 0], ['武备仪仗', 0], ['法书', 0], ['漆器', 0], ['玉石器', 0], ['珍宝', 0], ['珐琅器', 1], ['生活用具', 0], ['碑帖', 0], ['织绣', 0], ['绘画', 0], ['金银器', 0], ['钟表仪器', 0], ['铜器', 11], ['铭刻', 15], ['陶瓷', 217], ['雕刻 工艺', 0], ['雕塑', 0]]
                },
                {
                    dataGroupId: '商_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 0], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 0], ['文具', 1], ['未知', 0], ['武备仪仗', 0], ['法书', 0], ['漆器', 0], ['玉石器', 1355], ['珍宝', 0], ['珐琅器', 0], ['生活用具', 1], ['碑帖', 0], ['织绣', 0], ['绘画', 0], ['金银器', 0], ['钟表仪器', 0], ['铜器', 2472], ['铭刻', 21288], ['陶瓷', 331], ['雕刻工艺', 498], ['雕塑', 0]]
                },
                {
                    dataGroupId: '周_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 0], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 0], ['文具', 3], ['未知', 0], ['武备仪仗', 0], ['法书', 0], ['漆器', 0], ['玉石器', 682], ['珍宝', 4], ['珐琅器', 0], ['生活用具', 0], ['碑帖', 1], ['织绣', 0], ['绘画', 1], ['金银器', 0], ['钟表仪器', 0], ['铜器', 1360], ['铭刻', 23], ['陶瓷', 32], ['雕刻工艺', 17], ['雕塑', 13]]
                },
                {
                    dataGroupId: '春秋_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 0], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 0], ['文具', 0], ['未知', 0], ['武备仪仗', 0], ['法书', 0], ['漆器', 0], ['玉石器', 67], ['珍宝', 0], ['珐琅器', 0], ['生活用具', 0], ['碑帖', 0], ['织绣', 0], ['绘画', 0], ['金银器', 0], ['钟表仪器', 0], ['铜器', 641], ['铭刻', 0], ['陶瓷', 3], ['雕刻工艺', 0], ['雕塑', 0]]
                },
                {
                    dataGroupId: '战国_1',
                    data: [['其他工艺', 118], ['其他文物', 0], ['其它', 0], ['古建藏品', 128], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 0], ['文具', 5], ['未知', 0], ['武备仪仗', 0], ['法书', 0], ['漆器', 23], ['玉石器', 1408], ['珍宝', 0], [' 珐琅器', 0], ['生活用具', 0], ['碑帖', 0], ['织绣', 0], ['绘画', 0], ['金银器', 1], ['钟表仪器', 33], ['铜器', 3856], ['铭刻', 4940], ['陶瓷', 178], ['雕刻工艺', 49], ['雕塑', 79]]
                },
                {
                    dataGroupId: '秦_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 2], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 0], ['文具', 0], ['未知', 0], ['武备仪仗', 0], ['法书', 0], ['漆器', 0], ['玉石器', 7], ['珍宝', 0], ['珐琅器', 0], ['生活用具', 0], ['碑帖', 0], ['织绣', 0], ['绘画', 0], ['金银器', 0], ['钟表仪器', 2], ['铜器', 15], ['铭刻', 770], ['陶瓷', 2], ['雕刻工艺', 0], ['雕塑', 9]]
                },
                {
                    dataGroupId: '汉_1',
                    data: [['其他工艺', 81], ['其他文物', 0], ['其它', 0], ['古建藏品', 238], ['古籍文献', 0], ['外国文物', 0], [' 宗教文物', 0], ['帝后玺册', 0], ['文具', 55], ['未知', 0], ['武备仪仗', 0], ['法书', 0], ['漆器', 45], ['玉石器', 1168], ['珍宝', 1], ['珐琅器', 0], ['生活用具', 2], ['碑帖', 6], ['织绣', 47], ['绘画', 0], ['金银器', 21], ['钟表仪器', 7], ['铜器', 5808], ['铭刻', 14269], ['陶瓷', 1116], ['雕刻工艺', 50], ['雕塑', 1382]]
                },
                {
                    dataGroupId: '三国_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 0], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 0], ['文具', 0], ['未知', 0], ['武备仪仗', 0], ['法书', 1], ['漆器', 0], ['玉石器', 0], ['珍宝', 0], ['珐琅器', 0], ['生活用具', 0], ['碑帖', 1], ['织绣', 0], ['绘画', 0], ['金银器', 0], ['钟表仪器', 0], ['铜器', 18], ['铭刻', 101], ['陶瓷', 7], ['雕刻工艺', 0], ['雕塑', 1]]
                },
                {
                    dataGroupId: '魏晋南北朝_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 0], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 0], ['文具', 4], ['未知', 0], ['武备仪仗', 0], ['法书', 5], ['漆器', 0], ['玉石器', 62], ['珍宝', 0], ['珐琅器', 0], ['生活用具', 0], ['碑帖', 1], ['织绣', 3], ['绘画', 0], ['金银器', 1], ['钟表仪器', 0], ['铜器', 54], ['铭刻', 292], ['陶瓷', 522], ['雕刻工艺', 0], ['雕塑', 43]]
                },
                {
                    dataGroupId: '隋_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 0], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 0], ['文具', 0], ['未知', 0], ['武备仪仗', 0], ['法书', 9], ['漆器', 0], ['玉石器', 5], ['珍宝', 0], ['珐琅器', 0], ['生活用具', 0], ['碑帖', 0], ['织绣', 1], ['绘画', 2], ['金银器', 0], ['钟表仪器', 0], ['铜器', 72], ['铭刻', 30], ['陶瓷', 368], ['雕刻 工艺', 0], ['雕塑', 469]]
                },
                {
                    dataGroupId: '唐_1',
                    data: [['其他工艺', 24], ['其他文物', 0], ['其它', 0], ['古建藏品', 6], ['古籍文献', 0], ['外国文物', 0], ['宗 教文物', 60], ['帝后玺册', 0], ['文具', 64], ['未知', 0], ['武备仪仗', 6], ['法书', 113], ['漆器', 0], ['玉石器', 201], ['珍宝', 0], ['珐 琅器', 0], ['生活用具', 2], ['碑帖', 12], ['织绣', 20], ['绘画', 40], ['金银器', 6], ['钟表仪器', 6], ['铜器', 2641], ['铭刻', 300], ['陶 瓷', 2649], ['雕刻工艺', 27], ['雕塑', 2996]]
                },
                {
                    dataGroupId: '五代十国_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 0], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 9], ['帝后玺册', 0], ['文具', 0], ['未知', 0], ['武备仪仗', 0], ['法书', 0], ['漆器', 0], ['玉石器', 0], ['珍宝', 0], ['珐琅 器', 0], ['生活用具', 0], ['碑帖', 0], ['织绣', 0], ['绘画', 6], ['金银器', 0], ['钟表仪器', 0], ['铜器', 61], ['铭刻', 0], ['陶瓷', 36], ['雕刻工艺', 0], ['雕塑', 1]]
                },
                {
                    dataGroupId: '宋_1',
                    data: [['其他工艺', 70], ['其他文物', 0], ['其它', 0], ['古建藏品', 23], ['古籍文献', 0], ['外国文物', 1], ['宗教文物', 356], ['帝后玺册', 0], ['文具', 184], ['未知', 0], ['武备仪仗', 8], ['法书', 171], ['漆器', 6], ['玉石器', 482], ['珍宝', 0], [' 珐琅器', 0], ['生活用具', 2], ['碑帖', 313], ['织绣', 95], ['绘画', 501], ['金银器', 0], ['钟表仪器', 3], ['铜器', 4797], ['铭刻', 86], ['陶瓷', 9519], ['雕刻工艺', 5], ['雕塑', 812]]
                },
                {
                    dataGroupId: '元_1',
                    data: [['其他工艺', 16], ['其他文物', 0], ['其它', 0], ['古建藏品', 14], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 93], ['帝后玺册', 0], ['文具', 107], ['未知', 0], ['武备仪仗', 3], ['法书', 267], ['漆器', 14], ['玉石器', 414], ['珍宝', 0], [' 珐琅器', 12], ['生活用具', 2], ['碑帖', 43], ['织绣', 18], ['绘画', 422], ['金银器', 20], ['钟表仪器', 47], ['铜器', 189], ['铭刻', 1459], ['陶瓷', 1953], ['雕刻工艺', 1], ['雕塑', 76]]
                },
                {
                    dataGroupId: '明_1',
                    data: [['其他工艺', 517], ['其他文物', 0], ['其它', 0], ['古建藏品', 846], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 824], ['帝后玺册', 635], ['文具', 1192], ['未知', 0], ['武备仪仗', 47], ['法书', 13492], ['漆器', 1048], ['玉石器', 5068], ['珍宝', 3], ['珐琅器', 471], ['生活用具', 239], ['碑帖', 1479], ['织绣', 5603], ['绘画', 7409], ['金银器', 17], ['钟表仪器', 20], ['铜器', 1495], ['铭刻', 393], ['陶瓷', 10104], ['雕刻工艺', 244], ['雕塑', 1873]]
                },
                {
                    dataGroupId: '清_1',
                    data: [['其他工艺', 12691], ['其他文物', 0], ['其它', 1], ['古建藏品', 3070], ['古籍文献', 6451], ['外国文物', 1543], ['宗教文物', 46958], ['帝后玺册', 4296], ['文具', 79944], ['未知', 0], ['武备仪仗', 32543], ['法书', 57702], ['漆器', 17694], ['玉石器', 19228], ['珍宝', 870], ['珐琅器', 6078], ['生活用具', 35341], ['碑帖', 8712], ['织绣', 173610], ['绘画', 41269], ['金银器', 11293], ['钟表仪器', 2635], ['铜器', 134374], ['铭刻', 3423], ['陶瓷', 338177], ['雕刻工艺', 10036], ['雕塑', 1187]]
                },
                {
                    dataGroupId: '民国_1',
                    data: [['其他工艺', 9], ['其他文物', 0], ['其它', 0], ['古建藏品', 2], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 69], ['帝后玺册', 126], ['文具', 555], ['未知', 0], ['武备仪仗', 3], ['法书', 0], ['漆器', 6], ['玉石器', 9], ['珍宝', 3], ['珐琅器', 41], ['生活用具', 1656], ['碑帖', 364], ['织绣', 190], ['绘画', 535], ['金银器', 32], ['钟表仪器', 43], ['铜器', 319], ['铭刻', 377], ['陶瓷', 202], ['雕刻工艺', 23], ['雕塑', 59]]
                },
                {
                    dataGroupId: '现当代_1',
                    data: [['其他工艺', 0], ['其他文物', 0], ['其它', 0], ['古建藏品', 0], ['古籍文献', 0], ['外国文物', 0], ['宗教文物', 0], ['帝后玺册', 3], ['文具', 0], ['未知', 0], ['武备仪仗', 0], ['法书', 36], ['漆器', 3], ['玉石器', 0], ['珍宝', 0], ['珐琅器', 0], ['生活用具', 1], ['碑帖', 1], ['织绣', 562], ['绘画', 40], ['金银器', 0], ['钟表仪器', 3], ['铜器', 1], ['铭刻', 1], ['陶瓷', 47], ['雕刻工艺', 0], ['雕塑', 7]]
                },
                {
                    dataGroupId: '未知_1',
                    data: [['其他工艺', 7], ['其他文物', 0], ['其它', 1], ['古建藏品', 6], ['古籍文献', 595012], ['外国文物', 0], ['宗教文物', 7], ['帝后玺册', 0], ['文具', 2109], ['未知', 33], ['武备仪仗', 11], ['法书', 369], ['漆器', 15], ['玉石器', 3], ['珍宝', 2], ['珐琅器', 1], ['生活用具', 536], ['碑帖', 4197], ['织绣', 984], ['绘画', 20], ['金银器', 62], ['钟表仪器', 0], ['铜器', 2], ['铭刻', 82], ['陶瓷', 5748], ['雕刻工艺', 6], ['雕塑', 0]]
                }
            ];
            PM_BarGraphChart.on('click', function (event) {
                if (event.data) {
                    const subData = drilldownData.find(function (data) {
                        return data.dataGroupId === event.data.groupId;
                    });
                    if (!subData) {
                        return;
                    }
                    PM_BarGraphChart.setOption({
                        xAxis: {
                            data: subData.data.map(function (item) {
                                    return item[0];
                                }
                            ),

                            axisLabel: {
                                fontSize: 10,
                                interval: 0,  // 设置为0/表示全部显示
                            }
                        },
                        series: {
                            type: 'bar',
                            id: 'sales',
                            dataGroupId: subData.dataGroupId,
                            data: subData.data.map(function (item) {
                                return item[1];
                            }),
                            universalTransition: {
                                enabled: true,
                                divideShape: 'clone'
                            },
                            itemStyle: {
                                color: event.data.itemStyle.color
                            }
                        },
                        graphic: [
                            {
                                type: 'text',
                                left: 50,
                                top: 20,
                                style: {
                                    text: 'Back',
                                    fontSize: 12
                                },
                                onclick: function () {
                                    PM_BarGraphChart.setOption(option);
                                }
                            }
                        ]
                    });
                }
            });
            PM_BarGraphChart.setOption(option);
        }
    },
    mounted() {
        this.myEcharts();
    }
}
</script>

<!--scoped保证样式只影响当前页面-->
<style scoped>
@import '../assets/css/font.css';


/*图表样式*/
.PM_BarGraphChart {
    /*图表宽度高度 用来设定图表展示出来的大小 一定要设置*/
    width: 1100px;
    height: 900px;
    background-size: cover;
    margin-left: 650px;
    margin-top: 0;
    margin-right: 0;
    /*margin-right: -10%;*/
    /*flex: 1;*/
    /*align-items: center;*/
}

/*标题样式*/
.title {
    /*字体样式*/
    font-family: Fengyun, serif;
    /*字体粗细*/
    font-weight: 40;
    /*字体大小*/
    font-size: 50px;

    color: rgba(2, 3, 9, 0.6);
    flex: 1;
    width: 100px;
    height: 100px;
    margin-top: 100px;
    margin-left: 100px;
    z-index: 1;
}


.main {
    z-index: 10;
    position: fixed;
    display: flex;
    flex-direction: row;
    width: 9700px;
    height: 100vh;
    left: 7900px;
    top: 0;
    /*align-items: center;*/
}
.my_title{/*字体样式*/
    font-family: Fengyun, serif;
    /*字体大小*/
    font-size: 70px;
    color: rgba(2, 3, 9, 0.6);
    flex: 1;
    width: 500px;
    height: 100px;
    margin-top: 0;
    margin-left: -40px;
    z-index: 1;
}
.content {
    /*字体样式*/
    font-family: Fengyun, serif;
    /*字体粗细*/
    font-weight: 10;
    /*字体大小*/
    font-size: 40px;
    color: rgba(2, 3, 9, 0.6);
    flex: 1;
    width: 500px;
    height: 100px;
    margin-top: 0;
    margin-left: -100px;
    z-index: 1;
}

/*背景图设置*/
.mybackground {
    z-index: -1;
    position: relative;
    background-image: url("../assets/data/bg6.png");
    width: 100%;
    min-height: 100vh;
    background-size: 100% 100%;
}

.mybackground::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: #fffcf7; /* 设置半透明背景色 */
    opacity: 0.5; /* 设置透明度，取值范围为0到1，1为完全不透明 */
}

</style>
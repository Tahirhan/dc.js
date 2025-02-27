<a name="dc"></a>

## dc : <code>object</code>
The entire dc.js library is scoped under the **dc** name space. It does not introduce
anything else into the global name space.

Most `dc` functions are designed to allow function chaining, meaning they return the current chart
instance whenever it is appropriate.  The getter forms of functions do not participate in function
chaining because they return values that are not the chart, although some,
such as [.svg](#dc.baseMixin+svg) and [.xAxis](#dc.coordinateGridMixin+xAxis),
return values that are themselves chainable d3 objects.

**Kind**: global namespace  
**Version**: 3.1.8  
**Example**  
```js
// Example chaining
chart.width(300)
     .height(300)
     .filter('sunday');
```

* [dc](#dc) : <code>object</code>
    * [.logger](#dc.logger)
        * [new logger()](#new_dc.logger_new)
        * [.enableDebugLog](#dc.logger+enableDebugLog)
        * [.warn([msg])](#dc.logger+warn) ⇒ [<code>logger</code>](#dc.logger)
        * [.warnOnce([msg])](#dc.logger+warnOnce) ⇒ [<code>logger</code>](#dc.logger)
        * [.debug([msg])](#dc.logger+debug) ⇒ [<code>logger</code>](#dc.logger)
        * [.deprecate([fn], [msg])](#dc.logger+deprecate) ⇒ <code>function</code>
        * [.annotate([fn], [msg])](#dc.logger+annotate) ⇒ <code>function</code>
    * [.config](#dc.config)
        * [new config()](#new_dc.config_new)
        * [.defaultColors([colors])](#dc.config+defaultColors) ⇒ <code>Array</code> \| [<code>config</code>](#dc.config)
    * [.pieChart](#dc.pieChart)
        * [new pieChart(parent, [chartGroup])](#new_dc.pieChart_new)
        * [.slicesCap([cap])](#dc.pieChart+slicesCap) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
        * [.externalRadiusPadding([externalRadiusPadding])](#dc.pieChart+externalRadiusPadding) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
        * [.innerRadius([innerRadius])](#dc.pieChart+innerRadius) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
        * [.radius([radius])](#dc.pieChart+radius) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
        * [.cx([cx])](#dc.pieChart+cx) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
        * [.cy([cy])](#dc.pieChart+cy) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
        * [.minAngleForLabel([minAngleForLabel])](#dc.pieChart+minAngleForLabel) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
        * [.emptyTitle([title])](#dc.pieChart+emptyTitle) ⇒ <code>String</code> \| [<code>pieChart</code>](#dc.pieChart)
        * [.externalLabels([externalLabelRadius])](#dc.pieChart+externalLabels) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
        * [.drawPaths([drawPaths])](#dc.pieChart+drawPaths) ⇒ <code>Boolean</code> \| [<code>pieChart</code>](#dc.pieChart)
    * [.sunburstChart](#dc.sunburstChart)
        * [new sunburstChart(parent, [chartGroup])](#new_dc.sunburstChart_new)
        * [.innerRadius([innerRadius])](#dc.sunburstChart+innerRadius) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
        * [.radius([radius])](#dc.sunburstChart+radius) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
        * [.cx([cx])](#dc.sunburstChart+cx) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
        * [.cy([cy])](#dc.sunburstChart+cy) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
        * [.minAngleForLabel([minAngleForLabel])](#dc.sunburstChart+minAngleForLabel) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
        * [.emptyTitle([title])](#dc.sunburstChart+emptyTitle) ⇒ <code>String</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
        * [.externalLabels([externalLabelRadius])](#dc.sunburstChart+externalLabels) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
    * [.barChart](#dc.barChart)
        * [new barChart(parent, [chartGroup])](#new_dc.barChart_new)
        * [.centerBar([centerBar])](#dc.barChart+centerBar) ⇒ <code>Boolean</code> \| [<code>barChart</code>](#dc.barChart)
        * [.barPadding([barPadding])](#dc.barChart+barPadding) ⇒ <code>Number</code> \| [<code>barChart</code>](#dc.barChart)
        * [.outerPadding([padding])](#dc.barChart+outerPadding) ⇒ <code>Number</code> \| [<code>barChart</code>](#dc.barChart)
        * [.gap([gap])](#dc.barChart+gap) ⇒ <code>Number</code> \| [<code>barChart</code>](#dc.barChart)
        * [.alwaysUseRounding([alwaysUseRounding])](#dc.barChart+alwaysUseRounding) ⇒ <code>Boolean</code> \| [<code>barChart</code>](#dc.barChart)
    * [.lineChart](#dc.lineChart)
        * [new lineChart(parent, [chartGroup])](#new_dc.lineChart_new)
        * [.curve([curve])](#dc.lineChart+curve) ⇒ <code>d3.curve</code> \| [<code>lineChart</code>](#dc.lineChart)
        * ~~[.interpolate([interpolate])](#dc.lineChart+interpolate) ⇒ <code>d3.curve</code> \| [<code>lineChart</code>](#dc.lineChart)~~
        * ~~[.tension([tension])](#dc.lineChart+tension) ⇒ <code>Number</code> \| [<code>lineChart</code>](#dc.lineChart)~~
        * [.defined([defined])](#dc.lineChart+defined) ⇒ <code>function</code> \| [<code>lineChart</code>](#dc.lineChart)
        * [.dashStyle([dashStyle])](#dc.lineChart+dashStyle) ⇒ <code>Array.&lt;Number&gt;</code> \| [<code>lineChart</code>](#dc.lineChart)
        * [.renderArea([renderArea])](#dc.lineChart+renderArea) ⇒ <code>Boolean</code> \| [<code>lineChart</code>](#dc.lineChart)
        * [.xyTipsOn([xyTipsOn])](#dc.lineChart+xyTipsOn) ⇒ <code>Boolean</code> \| [<code>lineChart</code>](#dc.lineChart)
        * [.dotRadius([dotRadius])](#dc.lineChart+dotRadius) ⇒ <code>Number</code> \| [<code>lineChart</code>](#dc.lineChart)
        * [.renderDataPoints([options])](#dc.lineChart+renderDataPoints) ⇒ <code>Object</code> \| [<code>lineChart</code>](#dc.lineChart)
    * [.dataCount](#dc.dataCount)
        * [new dataCount(parent, [chartGroup])](#new_dc.dataCount_new)
        * [.html([options])](#dc.dataCount+html) ⇒ <code>Object</code> \| [<code>dataCount</code>](#dc.dataCount)
        * [.formatNumber([formatter])](#dc.dataCount+formatNumber) ⇒ <code>function</code> \| [<code>dataCount</code>](#dc.dataCount)
    * [.dataTable](#dc.dataTable)
        * [new dataTable(parent, [chartGroup])](#new_dc.dataTable_new)
        * [.section(section)](#dc.dataTable+section) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
        * [.group(groupFunction)](#dc.dataTable+group) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
        * [.size([size])](#dc.dataTable+size) ⇒ <code>Number</code> \| [<code>dataTable</code>](#dc.dataTable)
        * [.beginSlice([beginSlice])](#dc.dataTable+beginSlice) ⇒ <code>Number</code> \| [<code>dataTable</code>](#dc.dataTable)
        * [.endSlice([endSlice])](#dc.dataTable+endSlice) ⇒ <code>Number</code> \| [<code>dataTable</code>](#dc.dataTable)
        * [.columns([columns])](#dc.dataTable+columns) ⇒ <code>Array.&lt;function()&gt;</code>
        * [.sortBy([sortBy])](#dc.dataTable+sortBy) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
        * [.order([order])](#dc.dataTable+order) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
        * [.showSections([showSections])](#dc.dataTable+showSections) ⇒ <code>Boolean</code> \| [<code>dataTable</code>](#dc.dataTable)
        * [.showGroups([showGroups])](#dc.dataTable+showGroups) ⇒ <code>Boolean</code> \| [<code>dataTable</code>](#dc.dataTable)
    * [.dataGrid](#dc.dataGrid)
        * [new dataGrid(parent, [chartGroup])](#new_dc.dataGrid_new)
        * [.section(section)](#dc.dataGrid+section) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
        * [.group(groupFunction)](#dc.dataGrid+group) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
        * [.beginSlice([beginSlice])](#dc.dataGrid+beginSlice) ⇒ <code>Number</code> \| [<code>dataGrid</code>](#dc.dataGrid)
        * [.endSlice([endSlice])](#dc.dataGrid+endSlice) ⇒ <code>Number</code> \| [<code>dataGrid</code>](#dc.dataGrid)
        * [.size([size])](#dc.dataGrid+size) ⇒ <code>Number</code> \| [<code>dataGrid</code>](#dc.dataGrid)
        * [.html([html])](#dc.dataGrid+html) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
        * [.htmlSection([htmlSection])](#dc.dataGrid+htmlSection) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
        * [.htmlGroup([htmlGroup])](#dc.dataGrid+htmlGroup) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
        * [.sortBy([sortByFunction])](#dc.dataGrid+sortBy) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
        * [.order([order])](#dc.dataGrid+order) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
    * [.bubbleChart](#dc.bubbleChart)
        * [new bubbleChart(parent, [chartGroup])](#new_dc.bubbleChart_new)
        * [.elasticRadius([elasticRadius])](#dc.bubbleChart+elasticRadius) ⇒ <code>Boolean</code> \| [<code>bubbleChart</code>](#dc.bubbleChart)
        * [.sortBubbleSize([sortBubbleSize])](#dc.bubbleChart+sortBubbleSize) ⇒ <code>Boolean</code> \| [<code>bubbleChart</code>](#dc.bubbleChart)
    * [.compositeChart](#dc.compositeChart)
        * [new compositeChart(parent, [chartGroup])](#new_dc.compositeChart_new)
        * [.useRightAxisGridLines([useRightAxisGridLines])](#dc.compositeChart+useRightAxisGridLines) ⇒ <code>Boolean</code> \| [<code>compositeChart</code>](#dc.compositeChart)
        * [.childOptions([childOptions])](#dc.compositeChart+childOptions) ⇒ <code>Object</code> \| [<code>compositeChart</code>](#dc.compositeChart)
        * [.rightYAxisLabel([rightYAxisLabel], [padding])](#dc.compositeChart+rightYAxisLabel) ⇒ <code>String</code> \| [<code>compositeChart</code>](#dc.compositeChart)
        * [.compose([subChartArray])](#dc.compositeChart+compose) ⇒ [<code>compositeChart</code>](#dc.compositeChart)
        * [.children()](#dc.compositeChart+children) ⇒ [<code>Array.&lt;baseMixin&gt;</code>](#dc.baseMixin)
        * [.shareColors([shareColors])](#dc.compositeChart+shareColors) ⇒ <code>Boolean</code> \| [<code>compositeChart</code>](#dc.compositeChart)
        * [.shareTitle([shareTitle])](#dc.compositeChart+shareTitle) ⇒ <code>Boolean</code> \| [<code>compositeChart</code>](#dc.compositeChart)
        * [.rightY([yScale])](#dc.compositeChart+rightY) ⇒ <code>d3.scale</code> \| [<code>compositeChart</code>](#dc.compositeChart)
        * [.alignYAxes([alignYAxes])](#dc.compositeChart+alignYAxes) ⇒ <code>Chart</code>
        * [.rightYAxis([rightYAxis])](#dc.compositeChart+rightYAxis) ⇒ <code>d3.axisRight</code> \| [<code>compositeChart</code>](#dc.compositeChart)
    * [.seriesChart](#dc.seriesChart)
        * [new seriesChart(parent, [chartGroup])](#new_dc.seriesChart_new)
        * [.chart([chartFunction])](#dc.seriesChart+chart) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)
        * [.seriesAccessor([accessor])](#dc.seriesChart+seriesAccessor) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)
        * [.seriesSort([sortFunction])](#dc.seriesChart+seriesSort) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)
        * [.valueSort([sortFunction])](#dc.seriesChart+valueSort) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)
    * [.geoChoroplethChart](#dc.geoChoroplethChart)
        * [new geoChoroplethChart(parent, [chartGroup])](#new_dc.geoChoroplethChart_new)
        * [.overlayGeoJson(json, name, keyAccessor)](#dc.geoChoroplethChart+overlayGeoJson) ⇒ [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)
        * [.projection([projection])](#dc.geoChoroplethChart+projection) ⇒ <code>d3.projection</code> \| [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)
        * [.geoJsons()](#dc.geoChoroplethChart+geoJsons) ⇒ <code>Array.&lt;{name:String, data: Object, accessor: function()}&gt;</code>
        * [.geoPath()](#dc.geoChoroplethChart+geoPath) ⇒ <code>d3.geoPath</code>
        * [.removeGeoJson(name)](#dc.geoChoroplethChart+removeGeoJson) ⇒ [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)
    * [.bubbleOverlay](#dc.bubbleOverlay)
        * [new bubbleOverlay(parent, [chartGroup])](#new_dc.bubbleOverlay_new)
        * [.svg([imageElement])](#dc.bubbleOverlay+svg) ⇒ [<code>bubbleOverlay</code>](#dc.bubbleOverlay)
        * [.point(name, x, y)](#dc.bubbleOverlay+point) ⇒ [<code>bubbleOverlay</code>](#dc.bubbleOverlay)
    * [.rowChart](#dc.rowChart)
        * [new rowChart(parent, [chartGroup])](#new_dc.rowChart_new)
        * [.x([scale])](#dc.rowChart+x) ⇒ <code>d3.scale</code> \| [<code>rowChart</code>](#dc.rowChart)
        * [.renderTitleLabel([renderTitleLabel])](#dc.rowChart+renderTitleLabel) ⇒ <code>Boolean</code> \| [<code>rowChart</code>](#dc.rowChart)
        * [.xAxis([xAxis])](#dc.rowChart+xAxis) ⇒ <code>d3.axis</code> \| [<code>rowChart</code>](#dc.rowChart)
        * [.fixedBarHeight([fixedBarHeight])](#dc.rowChart+fixedBarHeight) ⇒ <code>Boolean</code> \| <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
        * [.gap([gap])](#dc.rowChart+gap) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
        * [.elasticX([elasticX])](#dc.rowChart+elasticX) ⇒ <code>Boolean</code> \| [<code>rowChart</code>](#dc.rowChart)
        * [.labelOffsetX([labelOffsetX])](#dc.rowChart+labelOffsetX) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
        * [.labelOffsetY([labelOffsety])](#dc.rowChart+labelOffsetY) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
        * [.titleLabelOffsetX([titleLabelOffsetX])](#dc.rowChart+titleLabelOffsetX) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
    * [.legend](#dc.legend)
        * [new legend()](#new_dc.legend_new)
        * [.x([x])](#dc.legend+x) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
        * [.y([y])](#dc.legend+y) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
        * [.gap([gap])](#dc.legend+gap) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
        * [.itemHeight([itemHeight])](#dc.legend+itemHeight) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
        * [.horizontal([horizontal])](#dc.legend+horizontal) ⇒ <code>Boolean</code> \| [<code>legend</code>](#dc.legend)
        * [.legendWidth([legendWidth])](#dc.legend+legendWidth) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
        * [.itemWidth([itemWidth])](#dc.legend+itemWidth) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
        * [.autoItemWidth([autoItemWidth])](#dc.legend+autoItemWidth) ⇒ <code>Boolean</code> \| [<code>legend</code>](#dc.legend)
        * [.legendText([legendText])](#dc.legend+legendText) ⇒ <code>function</code> \| [<code>legend</code>](#dc.legend)
        * [.maxItems([maxItems])](#dc.legend+maxItems) ⇒ [<code>legend</code>](#dc.legend)
    * [.htmlLegend](#dc.htmlLegend)
        * [new htmlLegend()](#new_dc.htmlLegend_new)
        * [.container([container])](#dc.htmlLegend+container) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
        * [.legendItemClass([legendItemClass])](#dc.htmlLegend+legendItemClass) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
        * [.highlightSelected([highlightSelected])](#dc.htmlLegend+highlightSelected) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
        * [.horizontal([horizontal])](#dc.htmlLegend+horizontal) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
        * [.legendText([legendText])](#dc.htmlLegend+legendText) ⇒ <code>function</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
        * [.maxItems([maxItems])](#dc.htmlLegend+maxItems) ⇒ [<code>htmlLegend</code>](#dc.htmlLegend)
    * [.scatterPlot](#dc.scatterPlot)
        * [new scatterPlot(parent, [chartGroup])](#new_dc.scatterPlot_new)
        * [.emptyColor](#dc.scatterPlot+emptyColor) ⇒ <code>String</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
        * [.emptyOpacity](#dc.scatterPlot+emptyOpacity) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
        * [.nonemptyOpacity](#dc.scatterPlot+nonemptyOpacity) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
        * [.resetSvg()](#dc.scatterPlot+resetSvg) ⇒ <code>SVGElement</code>
        * [.useCanvas([useCanvas])](#dc.scatterPlot+useCanvas) ⇒ <code>Boolean</code> \| <code>d3.selection</code>
        * [.canvas([canvasElement])](#dc.scatterPlot+canvas) ⇒ <code>CanvasElement</code> \| <code>d3.selection</code>
        * [.context()](#dc.scatterPlot+context) ⇒ <code>CanvasContext</code>
        * [.existenceAccessor([accessor])](#dc.scatterPlot+existenceAccessor) ⇒ <code>function</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
        * [.symbol([type])](#dc.scatterPlot+symbol) ⇒ <code>function</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
        * [.customSymbol([customSymbol])](#dc.scatterPlot+customSymbol) ⇒ <code>String</code> \| <code>function</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
        * [.symbolSize([symbolSize])](#dc.scatterPlot+symbolSize) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
        * [.highlightedSize([highlightedSize])](#dc.scatterPlot+highlightedSize) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
        * [.excludedSize([excludedSize])](#dc.scatterPlot+excludedSize) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
        * [.excludedColor([excludedColor])](#dc.scatterPlot+excludedColor) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
        * [.excludedOpacity([excludedOpacity])](#dc.scatterPlot+excludedOpacity) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
        * [.emptySize([emptySize])](#dc.scatterPlot+emptySize) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.numberDisplay](#dc.numberDisplay)
        * [new numberDisplay(parent, [chartGroup])](#new_dc.numberDisplay_new)
        * [.html([html])](#dc.numberDisplay+html) ⇒ <code>Object</code> \| [<code>numberDisplay</code>](#dc.numberDisplay)
        * [.value()](#dc.numberDisplay+value) ⇒ <code>Number</code>
        * [.formatNumber([formatter])](#dc.numberDisplay+formatNumber) ⇒ <code>function</code> \| [<code>numberDisplay</code>](#dc.numberDisplay)
    * [.heatMap](#dc.heatMap)
        * [new heatMap(parent, [chartGroup])](#new_dc.heatMap_new)
        * [.colsLabel([labelFunction])](#dc.heatMap+colsLabel) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
        * [.rowsLabel([labelFunction])](#dc.heatMap+rowsLabel) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
        * [.rows([rows])](#dc.heatMap+rows) ⇒ <code>Array.&lt;(String\|Number)&gt;</code> \| [<code>heatMap</code>](#dc.heatMap)
        * [.rowOrdering([rowOrdering])](#dc.heatMap+rowOrdering) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
        * [.cols([cols])](#dc.heatMap+cols) ⇒ <code>Array.&lt;(String\|Number)&gt;</code> \| [<code>heatMap</code>](#dc.heatMap)
        * [.colOrdering([colOrdering])](#dc.heatMap+colOrdering) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
        * [.boxOnClick([handler])](#dc.heatMap+boxOnClick) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
        * [.xAxisOnClick([handler])](#dc.heatMap+xAxisOnClick) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
        * [.yAxisOnClick([handler])](#dc.heatMap+yAxisOnClick) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
        * [.xBorderRadius([xBorderRadius])](#dc.heatMap+xBorderRadius) ⇒ <code>Number</code> \| [<code>heatMap</code>](#dc.heatMap)
        * [.yBorderRadius([yBorderRadius])](#dc.heatMap+yBorderRadius) ⇒ <code>Number</code> \| [<code>heatMap</code>](#dc.heatMap)
    * [.boxPlot](#dc.boxPlot)
        * [new boxPlot(parent, [chartGroup])](#new_dc.boxPlot_new)
        * [.boxPadding([padding])](#dc.boxPlot+boxPadding) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
        * [.outerPadding([padding])](#dc.boxPlot+outerPadding) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
        * [.boxWidth([boxWidth])](#dc.boxPlot+boxWidth) ⇒ <code>Number</code> \| <code>function</code> \| [<code>boxPlot</code>](#dc.boxPlot)
        * [.tickFormat([tickFormat])](#dc.boxPlot+tickFormat) ⇒ <code>Number</code> \| <code>function</code> \| [<code>boxPlot</code>](#dc.boxPlot)
        * [.yRangePadding([yRangePadding])](#dc.boxPlot+yRangePadding) ⇒ <code>Number</code> \| <code>function</code> \| [<code>boxPlot</code>](#dc.boxPlot)
        * [.renderDataPoints([show])](#dc.boxPlot+renderDataPoints) ⇒ <code>Boolean</code> \| [<code>boxPlot</code>](#dc.boxPlot)
        * [.dataOpacity([opacity])](#dc.boxPlot+dataOpacity) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
        * [.dataWidthPortion([percentage])](#dc.boxPlot+dataWidthPortion) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
        * [.showOutliers([show])](#dc.boxPlot+showOutliers) ⇒ <code>Boolean</code> \| [<code>boxPlot</code>](#dc.boxPlot)
        * [.boldOutlier([show])](#dc.boxPlot+boldOutlier) ⇒ <code>Boolean</code> \| [<code>boxPlot</code>](#dc.boxPlot)
    * [.selectMenu](#dc.selectMenu)
        * [new selectMenu(parent, [chartGroup])](#new_dc.selectMenu_new)
        * [.order([order])](#dc.selectMenu+order) ⇒ <code>function</code> \| [<code>selectMenu</code>](#dc.selectMenu)
        * [.promptText([promptText])](#dc.selectMenu+promptText) ⇒ <code>String</code> \| [<code>selectMenu</code>](#dc.selectMenu)
        * [.filterDisplayed([filterDisplayed])](#dc.selectMenu+filterDisplayed) ⇒ <code>function</code> \| [<code>selectMenu</code>](#dc.selectMenu)
        * [.multiple([multiple])](#dc.selectMenu+multiple) ⇒ <code>boolean</code> \| [<code>selectMenu</code>](#dc.selectMenu)
        * [.promptValue([promptValue])](#dc.selectMenu+promptValue) ⇒ <code>\*</code> \| [<code>selectMenu</code>](#dc.selectMenu)
        * [.numberItems([numberVisible])](#dc.selectMenu+numberItems) ⇒ <code>number</code> \| [<code>selectMenu</code>](#dc.selectMenu)
    * [.textFilterWidget](#dc.textFilterWidget)
        * [new textFilterWidget(parent, [chartGroup])](#new_dc.textFilterWidget_new)
        * [.normalize](#dc.textFilterWidget+normalize) ⇒ [<code>textFilterWidget</code>](#dc.textFilterWidget) \| <code>function</code>
        * [.placeHolder](#dc.textFilterWidget+placeHolder) ⇒ [<code>textFilterWidget</code>](#dc.textFilterWidget) \| <code>string</code>
        * [.filterFunctionFactory](#dc.textFilterWidget+filterFunctionFactory) ⇒ [<code>textFilterWidget</code>](#dc.textFilterWidget) \| <code>function</code>
    * [.cboxMenu](#dc.cboxMenu)
        * [new cboxMenu(parent, [chartGroup])](#new_dc.cboxMenu_new)
        * [.order([order])](#dc.cboxMenu+order) ⇒ <code>function</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
        * [.promptText([promptText])](#dc.cboxMenu+promptText) ⇒ <code>String</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
        * [.filterDisplayed([filterDisplayed])](#dc.cboxMenu+filterDisplayed) ⇒ <code>function</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
        * [.multiple([multiple])](#dc.cboxMenu+multiple) ⇒ <code>Boolean</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
        * [.promptValue([promptValue])](#dc.cboxMenu+promptValue) ⇒ <code>\*</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
    * [.baseMixin](#dc.baseMixin) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.height([height])](#dc.baseMixin+height) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.width([width])](#dc.baseMixin+width) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.minWidth([minWidth])](#dc.baseMixin+minWidth) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.minHeight([minHeight])](#dc.baseMixin+minHeight) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.useViewBoxResizing([useViewBoxResizing])](#dc.baseMixin+useViewBoxResizing) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.dimension([dimension])](#dc.baseMixin+dimension) ⇒ <code>crossfilter.dimension</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.data([callback])](#dc.baseMixin+data) ⇒ <code>\*</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.group([group], [name])](#dc.baseMixin+group) ⇒ <code>crossfilter.group</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.ordering([orderFunction])](#dc.baseMixin+ordering) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.filterAll()](#dc.baseMixin+filterAll) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.select(sel)](#dc.baseMixin+select) ⇒ <code>d3.selection</code>
        * [.selectAll(sel)](#dc.baseMixin+selectAll) ⇒ <code>d3.selection</code>
        * [.anchor([parent], [chartGroup])](#dc.baseMixin+anchor) ⇒ <code>String</code> \| <code>node</code> \| <code>d3.selection</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.anchorName()](#dc.baseMixin+anchorName) ⇒ <code>String</code>
        * [.root([rootElement])](#dc.baseMixin+root) ⇒ <code>HTMLElement</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.svg([svgElement])](#dc.baseMixin+svg) ⇒ <code>SVGElement</code> \| <code>d3.selection</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.resetSvg()](#dc.baseMixin+resetSvg) ⇒ <code>SVGElement</code>
        * [.filterPrinter([filterPrinterFunction])](#dc.baseMixin+filterPrinter) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.controlsUseVisibility([controlsUseVisibility])](#dc.baseMixin+controlsUseVisibility) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.turnOnControls()](#dc.baseMixin+turnOnControls) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.turnOffControls()](#dc.baseMixin+turnOffControls) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.transitionDuration([duration])](#dc.baseMixin+transitionDuration) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.transitionDelay([delay])](#dc.baseMixin+transitionDelay) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.render()](#dc.baseMixin+render) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.redraw()](#dc.baseMixin+redraw) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.commitHandler(commitHandler)](#dc.baseMixin+commitHandler) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.redrawGroup()](#dc.baseMixin+redrawGroup) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.renderGroup()](#dc.baseMixin+renderGroup) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.hasFilterHandler([hasFilterHandler])](#dc.baseMixin+hasFilterHandler) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.hasFilter([filter])](#dc.baseMixin+hasFilter) ⇒ <code>Boolean</code>
        * [.removeFilterHandler([removeFilterHandler])](#dc.baseMixin+removeFilterHandler) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.addFilterHandler([addFilterHandler])](#dc.baseMixin+addFilterHandler) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.resetFilterHandler([resetFilterHandler])](#dc.baseMixin+resetFilterHandler) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.replaceFilter([filter])](#dc.baseMixin+replaceFilter) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.filter([filter])](#dc.baseMixin+filter) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.filters()](#dc.baseMixin+filters) ⇒ <code>Array.&lt;\*&gt;</code>
        * [.onClick(datum)](#dc.baseMixin+onClick) ⇒ <code>undefined</code>
        * [.filterHandler([filterHandler])](#dc.baseMixin+filterHandler) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.keyAccessor([keyAccessor])](#dc.baseMixin+keyAccessor) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.valueAccessor([valueAccessor])](#dc.baseMixin+valueAccessor) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.label([labelFunction], [enableLabels])](#dc.baseMixin+label) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.renderLabel([renderLabel])](#dc.baseMixin+renderLabel) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.title([titleFunction])](#dc.baseMixin+title) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.renderTitle([renderTitle])](#dc.baseMixin+renderTitle) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * ~~[.renderlet(renderletFunction)](#dc.baseMixin+renderlet) ⇒ [<code>baseMixin</code>](#dc.baseMixin)~~
        * [.chartGroup([chartGroup])](#dc.baseMixin+chartGroup) ⇒ <code>String</code> \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.expireCache()](#dc.baseMixin+expireCache) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.legend([legend])](#dc.baseMixin+legend) ⇒ [<code>legend</code>](#dc.legend) \| [<code>baseMixin</code>](#dc.baseMixin)
        * [.chartID()](#dc.baseMixin+chartID) ⇒ <code>String</code>
        * [.options(opts)](#dc.baseMixin+options) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
        * [.on(event, listener)](#dc.baseMixin+on) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.marginMixin](#dc.marginMixin) ⇒ [<code>marginMixin</code>](#dc.marginMixin)
        * [.margins([margins])](#dc.marginMixin+margins) ⇒ <code>Object</code> \| [<code>marginMixin</code>](#dc.marginMixin)
    * [.colorMixin](#dc.colorMixin) ⇒ [<code>colorMixin</code>](#dc.colorMixin)
        * [.colors([colorScale])](#dc.colorMixin+colors) ⇒ <code>d3.scale</code> \| [<code>colorMixin</code>](#dc.colorMixin)
        * [.ordinalColors(r)](#dc.colorMixin+ordinalColors) ⇒ [<code>colorMixin</code>](#dc.colorMixin)
        * [.linearColors(r)](#dc.colorMixin+linearColors) ⇒ [<code>colorMixin</code>](#dc.colorMixin)
        * [.colorAccessor([colorAccessor])](#dc.colorMixin+colorAccessor) ⇒ <code>function</code> \| [<code>colorMixin</code>](#dc.colorMixin)
        * [.colorDomain([domain])](#dc.colorMixin+colorDomain) ⇒ <code>Array.&lt;String&gt;</code> \| [<code>colorMixin</code>](#dc.colorMixin)
        * [.calculateColorDomain()](#dc.colorMixin+calculateColorDomain) ⇒ [<code>colorMixin</code>](#dc.colorMixin)
        * [.getColor(d, [i])](#dc.colorMixin+getColor) ⇒ <code>String</code>
        * [.colorCalculator([colorCalculator])](#dc.colorMixin+colorCalculator) ⇒ <code>function</code> \| [<code>colorMixin</code>](#dc.colorMixin)
    * [.coordinateGridMixin](#dc.coordinateGridMixin) ⇒ [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.rescale()](#dc.coordinateGridMixin+rescale) ⇒ [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.rangeChart([rangeChart])](#dc.coordinateGridMixin+rangeChart) ⇒ [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.zoomScale([extent])](#dc.coordinateGridMixin+zoomScale) ⇒ <code>Array.&lt;(Number\|Date)&gt;</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.zoomOutRestrict([zoomOutRestrict])](#dc.coordinateGridMixin+zoomOutRestrict) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.g([gElement])](#dc.coordinateGridMixin+g) ⇒ <code>SVGElement</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.mouseZoomable([mouseZoomable])](#dc.coordinateGridMixin+mouseZoomable) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.chartBodyG([chartBodyG])](#dc.coordinateGridMixin+chartBodyG) ⇒ <code>SVGElement</code>
        * [.x([xScale])](#dc.coordinateGridMixin+x) ⇒ <code>d3.scale</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.xUnits([xUnits])](#dc.coordinateGridMixin+xUnits) ⇒ <code>function</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.xAxis([xAxis])](#dc.coordinateGridMixin+xAxis) ⇒ <code>d3.axis</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.elasticX([elasticX])](#dc.coordinateGridMixin+elasticX) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.xAxisPadding([padding])](#dc.coordinateGridMixin+xAxisPadding) ⇒ <code>Number</code> \| <code>String</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.xAxisPaddingUnit([unit])](#dc.coordinateGridMixin+xAxisPaddingUnit) ⇒ <code>String</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.xUnitCount()](#dc.coordinateGridMixin+xUnitCount) ⇒ <code>Number</code>
        * [.useRightYAxis([useRightYAxis])](#dc.coordinateGridMixin+useRightYAxis) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.isOrdinal()](#dc.coordinateGridMixin+isOrdinal) ⇒ <code>Boolean</code>
        * [.xAxisLabel([labelText], [padding])](#dc.coordinateGridMixin+xAxisLabel) ⇒ <code>String</code>
        * [.yAxisLabel([labelText], [padding])](#dc.coordinateGridMixin+yAxisLabel) ⇒ <code>String</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.y([yScale])](#dc.coordinateGridMixin+y) ⇒ <code>d3.scale</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.yAxis([yAxis])](#dc.coordinateGridMixin+yAxis) ⇒ <code>d3.axisLeft</code> \| <code>d3.axisRight</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.elasticY([elasticY])](#dc.coordinateGridMixin+elasticY) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.renderHorizontalGridLines([renderHorizontalGridLines])](#dc.coordinateGridMixin+renderHorizontalGridLines) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.renderVerticalGridLines([renderVerticalGridLines])](#dc.coordinateGridMixin+renderVerticalGridLines) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.xAxisMin()](#dc.coordinateGridMixin+xAxisMin) ⇒ <code>\*</code>
        * [.xAxisMax()](#dc.coordinateGridMixin+xAxisMax) ⇒ <code>\*</code>
        * [.yAxisMin()](#dc.coordinateGridMixin+yAxisMin) ⇒ <code>\*</code>
        * [.yAxisMax()](#dc.coordinateGridMixin+yAxisMax) ⇒ <code>\*</code>
        * [.yAxisPadding([padding])](#dc.coordinateGridMixin+yAxisPadding) ⇒ <code>Number</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.round([round])](#dc.coordinateGridMixin+round) ⇒ <code>function</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.brush([_])](#dc.coordinateGridMixin+brush) ⇒ <code>d3.brush</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.clipPadding([padding])](#dc.coordinateGridMixin+clipPadding) ⇒ <code>Number</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.focus([range], [noRaiseEvents])](#dc.coordinateGridMixin+focus) ⇒ <code>undefined</code>
        * [.brushOn([brushOn])](#dc.coordinateGridMixin+brushOn) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
        * [.parentBrushOn([brushOn])](#dc.coordinateGridMixin+parentBrushOn) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.stackMixin](#dc.stackMixin) ⇒ [<code>stackMixin</code>](#dc.stackMixin)
        * [.stack(group, [name], [accessor])](#dc.stackMixin+stack) ⇒ <code>Array.&lt;{group: crossfilter.group, name: String, accessor: function()}&gt;</code> \| [<code>stackMixin</code>](#dc.stackMixin)
        * [.hidableStacks([hidableStacks])](#dc.stackMixin+hidableStacks) ⇒ <code>Boolean</code> \| [<code>stackMixin</code>](#dc.stackMixin)
        * [.hideStack(stackName)](#dc.stackMixin+hideStack) ⇒ [<code>stackMixin</code>](#dc.stackMixin)
        * [.showStack(stackName)](#dc.stackMixin+showStack) ⇒ [<code>stackMixin</code>](#dc.stackMixin)
        * [.title([stackName], [titleAccessor])](#dc.stackMixin+title) ⇒ <code>String</code> \| [<code>stackMixin</code>](#dc.stackMixin)
        * [.stackLayout([stack])](#dc.stackMixin+stackLayout) ⇒ <code>function</code> \| [<code>stackMixin</code>](#dc.stackMixin)
        * [.evadeDomainFilter([evadeDomainFilter])](#dc.stackMixin+evadeDomainFilter) ⇒ <code>Boolean</code> \| [<code>stackMixin</code>](#dc.stackMixin)
    * [.capMixin](#dc.capMixin) ⇒ [<code>capMixin</code>](#dc.capMixin)
        * [.cap([count])](#dc.capMixin+cap) ⇒ <code>Number</code> \| [<code>capMixin</code>](#dc.capMixin)
        * [.takeFront([takeFront])](#dc.capMixin+takeFront) ⇒ <code>Boolean</code> \| [<code>capMixin</code>](#dc.capMixin)
        * [.othersLabel([label])](#dc.capMixin+othersLabel) ⇒ <code>String</code> \| [<code>capMixin</code>](#dc.capMixin)
        * [.othersGrouper([grouperFunction])](#dc.capMixin+othersGrouper) ⇒ <code>function</code> \| [<code>capMixin</code>](#dc.capMixin)
    * [.bubbleMixin](#dc.bubbleMixin) ⇒ [<code>bubbleMixin</code>](#dc.bubbleMixin)
        * [.r([bubbleRadiusScale])](#dc.bubbleMixin+r) ⇒ <code>d3.scale</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
        * [.radiusValueAccessor([radiusValueAccessor])](#dc.bubbleMixin+radiusValueAccessor) ⇒ <code>function</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
        * [.minRadius([radius])](#dc.bubbleMixin+minRadius) ⇒ <code>Number</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
        * [.minRadiusWithLabel([radius])](#dc.bubbleMixin+minRadiusWithLabel) ⇒ <code>Number</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
        * [.maxBubbleRelativeSize([relativeSize])](#dc.bubbleMixin+maxBubbleRelativeSize) ⇒ <code>Number</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
    * [.disableTransitions](#dc.disableTransitions) : <code>Boolean</code>
    * [.dateFormat](#dc.dateFormat) : <code>function</code>
    * [.chartRegistry](#dc.chartRegistry) : <code>object</code>
        * [.has(chart)](#dc.chartRegistry.has) ⇒ <code>Boolean</code>
        * [.register(chart, [group])](#dc.chartRegistry.register) ⇒ <code>undefined</code>
        * [.deregister(chart, [group])](#dc.chartRegistry.deregister) ⇒ <code>undefined</code>
        * [.clear(group)](#dc.chartRegistry.clear) ⇒ <code>undefined</code>
        * [.list([group])](#dc.chartRegistry.list) ⇒ <code>Array.&lt;Object&gt;</code>
    * [.units](#dc.units) : <code>object</code>
        * [.fp](#dc.units.fp) : <code>object</code>
            * [.precision(precision)](#dc.units.fp.precision) ⇒ <code>function</code>
        * [.integers(start, end)](#dc.units.integers) ⇒ <code>Number</code>
        * [.ordinal()](#dc.units.ordinal) ⇒ <code>uncallable</code>
    * [.printers](#dc.printers) : <code>object</code>
        * [.filters(filters)](#dc.printers.filters) ⇒ <code>String</code>
        * [.filter(filter)](#dc.printers.filter) ⇒ <code>String</code>
    * [.utils](#dc.utils) : <code>object</code>
        * [.printSingleValue(filter)](#dc.utils.printSingleValue) ⇒ <code>String</code>
        * [.add(l, r, [t])](#dc.utils.add) ⇒ <code>Date</code> \| <code>Number</code>
        * [.subtract(l, r, [t])](#dc.utils.subtract) ⇒ <code>Date</code> \| <code>Number</code>
        * [.isNumber(n)](#dc.utils.isNumber) ⇒ <code>Boolean</code>
        * [.isFloat(n)](#dc.utils.isFloat) ⇒ <code>Boolean</code>
        * [.isInteger(n)](#dc.utils.isInteger) ⇒ <code>Boolean</code>
        * [.isNegligible(n)](#dc.utils.isNegligible) ⇒ <code>Boolean</code>
        * [.clamp(val, min, max)](#dc.utils.clamp) ⇒ <code>any</code>
        * [.constant(x)](#dc.utils.constant) ⇒ <code>function</code>
        * [.uniqueId()](#dc.utils.uniqueId) ⇒ <code>Number</code>
        * [.nameToId(name)](#dc.utils.nameToId) ⇒ <code>String</code>
        * [.appendOrSelect(parent, selector, tag)](#dc.utils.appendOrSelect) ⇒ <code>d3.selection</code>
        * [.safeNumber(n)](#dc.utils.safeNumber) ⇒ <code>Number</code>
        * [.arraysEqual(a1, a2)](#dc.utils.arraysEqual) ⇒ <code>Boolean</code>
    * [.filters](#dc.filters) : <code>object</code>
        * [.RangedFilter](#dc.filters.RangedFilter)
            * [new RangedFilter(low, high)](#new_dc.filters.RangedFilter_new)
        * [.TwoDimensionalFilter](#dc.filters.TwoDimensionalFilter)
            * [new TwoDimensionalFilter(filter)](#new_dc.filters.TwoDimensionalFilter_new)
        * [.RangedTwoDimensionalFilter](#dc.filters.RangedTwoDimensionalFilter)
            * [new RangedTwoDimensionalFilter(filter)](#new_dc.filters.RangedTwoDimensionalFilter_new)
        * [.HierarchyFilter](#dc.filters.HierarchyFilter)
            * [new HierarchyFilter(path)](#new_dc.filters.HierarchyFilter_new)
    * [.registerChart(chart, [group])](#dc.registerChart) ⇒ <code>undefined</code>
    * [.deregisterChart(chart, [group])](#dc.deregisterChart) ⇒ <code>undefined</code>
    * [.hasChart(chart)](#dc.hasChart) ⇒ <code>Boolean</code>
    * [.deregisterAllCharts(group)](#dc.deregisterAllCharts) ⇒ <code>undefined</code>
    * [.filterAll([group])](#dc.filterAll) ⇒ <code>undefined</code>
    * [.refocusAll([group])](#dc.refocusAll) ⇒ <code>undefined</code>
    * [.renderAll([group])](#dc.renderAll) ⇒ <code>undefined</code>
    * [.redrawAll([group])](#dc.redrawAll) ⇒ <code>undefined</code>
    * [.transition(selection, [duration], [delay], [name])](#dc.transition) ⇒ <code>d3.transition</code> \| <code>d3.selection</code>
    * [.pluck(n, [f])](#dc.pluck) ⇒ <code>function</code>

<a name="dc.logger"></a>

### dc.logger
**Kind**: static class of [<code>dc</code>](#dc)  

* [.logger](#dc.logger)
    * [new logger()](#new_dc.logger_new)
    * [.enableDebugLog](#dc.logger+enableDebugLog)
    * [.warn([msg])](#dc.logger+warn) ⇒ [<code>logger</code>](#dc.logger)
    * [.warnOnce([msg])](#dc.logger+warnOnce) ⇒ [<code>logger</code>](#dc.logger)
    * [.debug([msg])](#dc.logger+debug) ⇒ [<code>logger</code>](#dc.logger)
    * [.deprecate([fn], [msg])](#dc.logger+deprecate) ⇒ <code>function</code>
    * [.annotate([fn], [msg])](#dc.logger+annotate) ⇒ <code>function</code>

<a name="new_dc.logger_new"></a>

#### new logger()
Provides basis logging and deprecation utilities

<a name="dc.logger+enableDebugLog"></a>

#### logger.enableDebugLog
Enable debug level logging. Set to `false` by default.

**Kind**: instance property of [<code>logger</code>](#dc.logger)  
<a name="dc.logger+warn"></a>

#### logger.warn([msg]) ⇒ [<code>logger</code>](#dc.logger)
Put a warning message to console

**Kind**: instance method of [<code>logger</code>](#dc.logger)  

| Param | Type |
| --- | --- |
| [msg] | <code>String</code> | 

**Example**  
```js
dc.logger.warn('Invalid use of .tension on CurveLinear');
```
<a name="dc.logger+warnOnce"></a>

#### logger.warnOnce([msg]) ⇒ [<code>logger</code>](#dc.logger)
Put a warning message to console. It will warn only on unique messages.

**Kind**: instance method of [<code>logger</code>](#dc.logger)  

| Param | Type |
| --- | --- |
| [msg] | <code>String</code> | 

**Example**  
```js
dc.logger.warnOnce('Invalid use of .tension on CurveLinear');
```
<a name="dc.logger+debug"></a>

#### logger.debug([msg]) ⇒ [<code>logger</code>](#dc.logger)
Put a debug message to console. It is controlled by `dc.logger.enableDebugLog`

**Kind**: instance method of [<code>logger</code>](#dc.logger)  

| Param | Type |
| --- | --- |
| [msg] | <code>String</code> | 

**Example**  
```js
dc.logger.debug('Total number of slices: ' + numSlices);
```
<a name="dc.logger+deprecate"></a>

#### logger.deprecate([fn], [msg]) ⇒ <code>function</code>
Used to deprecate a function. It will return a wrapped version of the function, which will
will issue a warning when invoked. The warning will be issued only once.

**Kind**: instance method of [<code>logger</code>](#dc.logger)  

| Param | Type |
| --- | --- |
| [fn] | <code>function</code> | 
| [msg] | <code>String</code> | 

**Example**  
```js
_chart.interpolate = dc.logger.deprecate(function (interpolate) {
   if (!arguments.length) {
       return _interpolate;
   }
   _interpolate = interpolate;
   return _chart;
}, 'dc.lineChart.interpolate has been deprecated since version 3.0 use dc.lineChart.curve instead');
```
<a name="dc.logger+annotate"></a>

#### logger.annotate([fn], [msg]) ⇒ <code>function</code>
Used to provide an informational message for a function. It will return a wrapped version of
the function, which will will issue a messsage with stack when invoked. The message will be
issued only once.

**Kind**: instance method of [<code>logger</code>](#dc.logger)  

| Param | Type |
| --- | --- |
| [fn] | <code>function</code> | 
| [msg] | <code>String</code> | 

**Example**  
```js
_chart.interpolate = dc.logger.annotate(function (interpolate) {
   if (!arguments.length) {
       return _interpolate;
   }
   _interpolate = interpolate;
   return _chart;
}, 'dc.lineChart.interpolate has been annotated since version 3.0 use dc.lineChart.curve instead');
```
<a name="dc.config"></a>

### dc.config
**Kind**: static class of [<code>dc</code>](#dc)  

* [.config](#dc.config)
    * [new config()](#new_dc.config_new)
    * [.defaultColors([colors])](#dc.config+defaultColors) ⇒ <code>Array</code> \| [<code>config</code>](#dc.config)

<a name="new_dc.config_new"></a>

#### new config()
General configuration

<a name="dc.config+defaultColors"></a>

#### config.defaultColors([colors]) ⇒ <code>Array</code> \| [<code>config</code>](#dc.config)
Set the default color scheme for ordinal charts. Changing it will impact all ordinal charts.

By default it is set to a copy of
`d3.schemeCategory20c` for backward compatibility. This color scheme has been
[removed from D3v5](https://github.com/d3/d3/blob/master/CHANGES.md#changes-in-d3-50).
In DC 3.1 release it will change to a more appropriate default.

**Kind**: instance method of [<code>config</code>](#dc.config)  

| Param | Type |
| --- | --- |
| [colors] | <code>Array</code> | 

**Example**  
```js
dc.config.defaultColors(d3.schemeSet1)
```
<a name="dc.pieChart"></a>

### dc.pieChart
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>capMixin</code>](#dc.capMixin), [<code>colorMixin</code>](#dc.colorMixin), [<code>baseMixin</code>](#dc.baseMixin)  

* [.pieChart](#dc.pieChart)
    * [new pieChart(parent, [chartGroup])](#new_dc.pieChart_new)
    * [.slicesCap([cap])](#dc.pieChart+slicesCap) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
    * [.externalRadiusPadding([externalRadiusPadding])](#dc.pieChart+externalRadiusPadding) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
    * [.innerRadius([innerRadius])](#dc.pieChart+innerRadius) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
    * [.radius([radius])](#dc.pieChart+radius) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
    * [.cx([cx])](#dc.pieChart+cx) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
    * [.cy([cy])](#dc.pieChart+cy) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
    * [.minAngleForLabel([minAngleForLabel])](#dc.pieChart+minAngleForLabel) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
    * [.emptyTitle([title])](#dc.pieChart+emptyTitle) ⇒ <code>String</code> \| [<code>pieChart</code>](#dc.pieChart)
    * [.externalLabels([externalLabelRadius])](#dc.pieChart+externalLabels) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
    * [.drawPaths([drawPaths])](#dc.pieChart+drawPaths) ⇒ <code>Boolean</code> \| [<code>pieChart</code>](#dc.pieChart)

<a name="new_dc.pieChart_new"></a>

#### new pieChart(parent, [chartGroup])
The pie chart implementation is usually used to visualize a small categorical distribution.  The pie
chart uses keyAccessor to determine the slices, and valueAccessor to calculate the size of each
slice relative to the sum of all values. Slices are ordered by [ordering](#dc.baseMixin+ordering)
which defaults to sorting by key.

Examples:
- [Nasdaq 100 Index](http://dc-js.github.com/dc.js/)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a pie chart under #chart-container1 element using the default global chart group
var chart1 = dc.pieChart('#chart-container1');
// create a pie chart under #chart-container2 element using chart group A
var chart2 = dc.pieChart('#chart-container2', 'chartGroupA');
```
<a name="dc.pieChart+slicesCap"></a>

#### pieChart.slicesCap([cap]) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
Get or set the maximum number of slices the pie chart will generate. The top slices are determined by
value from high to low. Other slices exeeding the cap will be rolled up into one single *Others* slice.

**Kind**: instance method of [<code>pieChart</code>](#dc.pieChart)  

| Param | Type |
| --- | --- |
| [cap] | <code>Number</code> | 

<a name="dc.pieChart+externalRadiusPadding"></a>

#### pieChart.externalRadiusPadding([externalRadiusPadding]) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
Get or set the external radius padding of the pie chart. This will force the radius of the
pie chart to become smaller or larger depending on the value.

**Kind**: instance method of [<code>pieChart</code>](#dc.pieChart)  

| Param | Type | Default |
| --- | --- | --- |
| [externalRadiusPadding] | <code>Number</code> | <code>0</code> | 

<a name="dc.pieChart+innerRadius"></a>

#### pieChart.innerRadius([innerRadius]) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
Get or set the inner radius of the pie chart. If the inner radius is greater than 0px then the
pie chart will be rendered as a doughnut chart.

**Kind**: instance method of [<code>pieChart</code>](#dc.pieChart)  

| Param | Type | Default |
| --- | --- | --- |
| [innerRadius] | <code>Number</code> | <code>0</code> | 

<a name="dc.pieChart+radius"></a>

#### pieChart.radius([radius]) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
Get or set the outer radius. If the radius is not set, it will be half of the minimum of the
chart width and height.

**Kind**: instance method of [<code>pieChart</code>](#dc.pieChart)  

| Param | Type |
| --- | --- |
| [radius] | <code>Number</code> | 

<a name="dc.pieChart+cx"></a>

#### pieChart.cx([cx]) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
Get or set center x coordinate position. Default is center of svg.

**Kind**: instance method of [<code>pieChart</code>](#dc.pieChart)  

| Param | Type |
| --- | --- |
| [cx] | <code>Number</code> | 

<a name="dc.pieChart+cy"></a>

#### pieChart.cy([cy]) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
Get or set center y coordinate position. Default is center of svg.

**Kind**: instance method of [<code>pieChart</code>](#dc.pieChart)  

| Param | Type |
| --- | --- |
| [cy] | <code>Number</code> | 

<a name="dc.pieChart+minAngleForLabel"></a>

#### pieChart.minAngleForLabel([minAngleForLabel]) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
Get or set the minimal slice angle for label rendering. Any slice with a smaller angle will not
display a slice label.

**Kind**: instance method of [<code>pieChart</code>](#dc.pieChart)  

| Param | Type | Default |
| --- | --- | --- |
| [minAngleForLabel] | <code>Number</code> | <code>0.5</code> | 

<a name="dc.pieChart+emptyTitle"></a>

#### pieChart.emptyTitle([title]) ⇒ <code>String</code> \| [<code>pieChart</code>](#dc.pieChart)
Title to use for the only slice when there is no data.

**Kind**: instance method of [<code>pieChart</code>](#dc.pieChart)  

| Param | Type |
| --- | --- |
| [title] | <code>String</code> | 

<a name="dc.pieChart+externalLabels"></a>

#### pieChart.externalLabels([externalLabelRadius]) ⇒ <code>Number</code> \| [<code>pieChart</code>](#dc.pieChart)
Position slice labels offset from the outer edge of the chart.

The argument specifies the extra radius to be added for slice labels.

**Kind**: instance method of [<code>pieChart</code>](#dc.pieChart)  

| Param | Type |
| --- | --- |
| [externalLabelRadius] | <code>Number</code> | 

<a name="dc.pieChart+drawPaths"></a>

#### pieChart.drawPaths([drawPaths]) ⇒ <code>Boolean</code> \| [<code>pieChart</code>](#dc.pieChart)
Get or set whether to draw lines from pie slices to their labels.

**Kind**: instance method of [<code>pieChart</code>](#dc.pieChart)  

| Param | Type |
| --- | --- |
| [drawPaths] | <code>Boolean</code> | 

<a name="dc.sunburstChart"></a>

### dc.sunburstChart
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>capMixin</code>](#dc.capMixin), [<code>colorMixin</code>](#dc.colorMixin), [<code>baseMixin</code>](#dc.baseMixin)  

* [.sunburstChart](#dc.sunburstChart)
    * [new sunburstChart(parent, [chartGroup])](#new_dc.sunburstChart_new)
    * [.innerRadius([innerRadius])](#dc.sunburstChart+innerRadius) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
    * [.radius([radius])](#dc.sunburstChart+radius) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
    * [.cx([cx])](#dc.sunburstChart+cx) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
    * [.cy([cy])](#dc.sunburstChart+cy) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
    * [.minAngleForLabel([minAngleForLabel])](#dc.sunburstChart+minAngleForLabel) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
    * [.emptyTitle([title])](#dc.sunburstChart+emptyTitle) ⇒ <code>String</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
    * [.externalLabels([externalLabelRadius])](#dc.sunburstChart+externalLabels) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)

<a name="new_dc.sunburstChart_new"></a>

#### new sunburstChart(parent, [chartGroup])
The sunburst chart implementation is usually used to visualize a small tree distribution.  The sunburst
chart uses keyAccessor to determine the slices, and valueAccessor to calculate the size of each
slice relative to the sum of all values. Slices are ordered by [ordering](#dc.baseMixin+ordering) which defaults to sorting
by key.

The keys used in the sunburst chart should be arrays, representing paths in the tree.

When filtering, the sunburst chart creates instances of [HierarchyFilter](#dc.filters.HierarchyFilter).


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-3.x-api-reference/blob/master/Selections.md#selecting-elements) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a sunburst chart under #chart-container1 element using the default global chart group
var chart1 = dc.sunburstChart('#chart-container1');
// create a sunburst chart under #chart-container2 element using chart group A
var chart2 = dc.sunburstChart('#chart-container2', 'chartGroupA');
```
<a name="dc.sunburstChart+innerRadius"></a>

#### sunburstChart.innerRadius([innerRadius]) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
Get or set the inner radius of the sunburst chart. If the inner radius is greater than 0px then the
sunburst chart will be rendered as a doughnut chart. Default inner radius is 0px.

**Kind**: instance method of [<code>sunburstChart</code>](#dc.sunburstChart)  

| Param | Type | Default |
| --- | --- | --- |
| [innerRadius] | <code>Number</code> | <code>0</code> | 

<a name="dc.sunburstChart+radius"></a>

#### sunburstChart.radius([radius]) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
Get or set the outer radius. If the radius is not set, it will be half of the minimum of the
chart width and height.

**Kind**: instance method of [<code>sunburstChart</code>](#dc.sunburstChart)  

| Param | Type |
| --- | --- |
| [radius] | <code>Number</code> | 

<a name="dc.sunburstChart+cx"></a>

#### sunburstChart.cx([cx]) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
Get or set center x coordinate position. Default is center of svg.

**Kind**: instance method of [<code>sunburstChart</code>](#dc.sunburstChart)  

| Param | Type |
| --- | --- |
| [cx] | <code>Number</code> | 

<a name="dc.sunburstChart+cy"></a>

#### sunburstChart.cy([cy]) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
Get or set center y coordinate position. Default is center of svg.

**Kind**: instance method of [<code>sunburstChart</code>](#dc.sunburstChart)  

| Param | Type |
| --- | --- |
| [cy] | <code>Number</code> | 

<a name="dc.sunburstChart+minAngleForLabel"></a>

#### sunburstChart.minAngleForLabel([minAngleForLabel]) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
Get or set the minimal slice angle for label rendering. Any slice with a smaller angle will not
display a slice label.

**Kind**: instance method of [<code>sunburstChart</code>](#dc.sunburstChart)  

| Param | Type | Default |
| --- | --- | --- |
| [minAngleForLabel] | <code>Number</code> | <code>0.5</code> | 

<a name="dc.sunburstChart+emptyTitle"></a>

#### sunburstChart.emptyTitle([title]) ⇒ <code>String</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
Title to use for the only slice when there is no data.

**Kind**: instance method of [<code>sunburstChart</code>](#dc.sunburstChart)  

| Param | Type |
| --- | --- |
| [title] | <code>String</code> | 

<a name="dc.sunburstChart+externalLabels"></a>

#### sunburstChart.externalLabels([externalLabelRadius]) ⇒ <code>Number</code> \| [<code>sunburstChart</code>](#dc.sunburstChart)
Position slice labels offset from the outer edge of the chart.

The argument specifies the extra radius to be added for slice labels.

**Kind**: instance method of [<code>sunburstChart</code>](#dc.sunburstChart)  

| Param | Type |
| --- | --- |
| [externalLabelRadius] | <code>Number</code> | 

<a name="dc.barChart"></a>

### dc.barChart
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>stackMixin</code>](#dc.stackMixin), [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

* [.barChart](#dc.barChart)
    * [new barChart(parent, [chartGroup])](#new_dc.barChart_new)
    * [.centerBar([centerBar])](#dc.barChart+centerBar) ⇒ <code>Boolean</code> \| [<code>barChart</code>](#dc.barChart)
    * [.barPadding([barPadding])](#dc.barChart+barPadding) ⇒ <code>Number</code> \| [<code>barChart</code>](#dc.barChart)
    * [.outerPadding([padding])](#dc.barChart+outerPadding) ⇒ <code>Number</code> \| [<code>barChart</code>](#dc.barChart)
    * [.gap([gap])](#dc.barChart+gap) ⇒ <code>Number</code> \| [<code>barChart</code>](#dc.barChart)
    * [.alwaysUseRounding([alwaysUseRounding])](#dc.barChart+alwaysUseRounding) ⇒ <code>Boolean</code> \| [<code>barChart</code>](#dc.barChart)

<a name="new_dc.barChart_new"></a>

#### new barChart(parent, [chartGroup])
Concrete bar chart/histogram implementation.

Examples:
- [Nasdaq 100 Index](http://dc-js.github.com/dc.js/)
- [Canadian City Crime Stats](http://dc-js.github.com/dc.js/crime/index.html)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> \| [<code>compositeChart</code>](#dc.compositeChart) | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection.  If the bar chart is a sub-chart in a [Composite Chart](#dc.compositeChart) then pass in the parent composite chart instance instead. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a bar chart under #chart-container1 element using the default global chart group
var chart1 = dc.barChart('#chart-container1');
// create a bar chart under #chart-container2 element using chart group A
var chart2 = dc.barChart('#chart-container2', 'chartGroupA');
// create a sub-chart under a composite parent chart
var chart3 = dc.barChart(compositeChart);
```
<a name="dc.barChart+centerBar"></a>

#### barChart.centerBar([centerBar]) ⇒ <code>Boolean</code> \| [<code>barChart</code>](#dc.barChart)
Whether the bar chart will render each bar centered around the data position on the x-axis.

**Kind**: instance method of [<code>barChart</code>](#dc.barChart)  

| Param | Type | Default |
| --- | --- | --- |
| [centerBar] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.barChart+barPadding"></a>

#### barChart.barPadding([barPadding]) ⇒ <code>Number</code> \| [<code>barChart</code>](#dc.barChart)
Get or set the spacing between bars as a fraction of bar size. Valid values are between 0-1.
Setting this value will also remove any previously set [gap](#dc.barChart+gap). See the
[d3 docs](https://github.com/d3/d3-scale/blob/master/README.md#scaleBand)
for a visual description of how the padding is applied.

**Kind**: instance method of [<code>barChart</code>](#dc.barChart)  

| Param | Type | Default |
| --- | --- | --- |
| [barPadding] | <code>Number</code> | <code>0</code> | 

<a name="dc.barChart+outerPadding"></a>

#### barChart.outerPadding([padding]) ⇒ <code>Number</code> \| [<code>barChart</code>](#dc.barChart)
Get or set the outer padding on an ordinal bar chart. This setting has no effect on non-ordinal charts.
Will pad the width by `padding * barWidth` on each side of the chart.

**Kind**: instance method of [<code>barChart</code>](#dc.barChart)  

| Param | Type | Default |
| --- | --- | --- |
| [padding] | <code>Number</code> | <code>0.5</code> | 

<a name="dc.barChart+gap"></a>

#### barChart.gap([gap]) ⇒ <code>Number</code> \| [<code>barChart</code>](#dc.barChart)
Manually set fixed gap (in px) between bars instead of relying on the default auto-generated
gap.  By default the bar chart implementation will calculate and set the gap automatically
based on the number of data points and the length of the x axis.

**Kind**: instance method of [<code>barChart</code>](#dc.barChart)  

| Param | Type | Default |
| --- | --- | --- |
| [gap] | <code>Number</code> | <code>2</code> | 

<a name="dc.barChart+alwaysUseRounding"></a>

#### barChart.alwaysUseRounding([alwaysUseRounding]) ⇒ <code>Boolean</code> \| [<code>barChart</code>](#dc.barChart)
Set or get whether rounding is enabled when bars are centered. If false, using
rounding with centered bars will result in a warning and rounding will be ignored.  This flag
has no effect if bars are not [centered](#dc.barChart+centerBar).
When using standard d3.js rounding methods, the brush often doesn't align correctly with
centered bars since the bars are offset.  The rounding function must add an offset to
compensate, such as in the following example.

**Kind**: instance method of [<code>barChart</code>](#dc.barChart)  

| Param | Type | Default |
| --- | --- | --- |
| [alwaysUseRounding] | <code>Boolean</code> | <code>false</code> | 

**Example**  
```js
chart.round(function(n) { return Math.floor(n) + 0.5; });
```
<a name="dc.lineChart"></a>

### dc.lineChart
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>stackMixin</code>](#dc.stackMixin), [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

* [.lineChart](#dc.lineChart)
    * [new lineChart(parent, [chartGroup])](#new_dc.lineChart_new)
    * [.curve([curve])](#dc.lineChart+curve) ⇒ <code>d3.curve</code> \| [<code>lineChart</code>](#dc.lineChart)
    * ~~[.interpolate([interpolate])](#dc.lineChart+interpolate) ⇒ <code>d3.curve</code> \| [<code>lineChart</code>](#dc.lineChart)~~
    * ~~[.tension([tension])](#dc.lineChart+tension) ⇒ <code>Number</code> \| [<code>lineChart</code>](#dc.lineChart)~~
    * [.defined([defined])](#dc.lineChart+defined) ⇒ <code>function</code> \| [<code>lineChart</code>](#dc.lineChart)
    * [.dashStyle([dashStyle])](#dc.lineChart+dashStyle) ⇒ <code>Array.&lt;Number&gt;</code> \| [<code>lineChart</code>](#dc.lineChart)
    * [.renderArea([renderArea])](#dc.lineChart+renderArea) ⇒ <code>Boolean</code> \| [<code>lineChart</code>](#dc.lineChart)
    * [.xyTipsOn([xyTipsOn])](#dc.lineChart+xyTipsOn) ⇒ <code>Boolean</code> \| [<code>lineChart</code>](#dc.lineChart)
    * [.dotRadius([dotRadius])](#dc.lineChart+dotRadius) ⇒ <code>Number</code> \| [<code>lineChart</code>](#dc.lineChart)
    * [.renderDataPoints([options])](#dc.lineChart+renderDataPoints) ⇒ <code>Object</code> \| [<code>lineChart</code>](#dc.lineChart)

<a name="new_dc.lineChart_new"></a>

#### new lineChart(parent, [chartGroup])
Concrete line/area chart implementation.

Examples:
- [Nasdaq 100 Index](http://dc-js.github.com/dc.js/)
- [Canadian City Crime Stats](http://dc-js.github.com/dc.js/crime/index.html)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> \| [<code>compositeChart</code>](#dc.compositeChart) | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection.  If the line chart is a sub-chart in a [Composite Chart](#dc.compositeChart) then pass in the parent composite chart instance instead. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a line chart under #chart-container1 element using the default global chart group
var chart1 = dc.lineChart('#chart-container1');
// create a line chart under #chart-container2 element using chart group A
var chart2 = dc.lineChart('#chart-container2', 'chartGroupA');
// create a sub-chart under a composite parent chart
var chart3 = dc.lineChart(compositeChart);
```
<a name="dc.lineChart+curve"></a>

#### lineChart.curve([curve]) ⇒ <code>d3.curve</code> \| [<code>lineChart</code>](#dc.lineChart)
Gets or sets the curve factory to use for lines and areas drawn, allowing e.g. step
functions, splines, and cubic interpolation. Typically you would use one of the interpolator functions
provided by [d3 curves](https://github.com/d3/d3-shape/blob/master/README.md#curves).

Replaces the use of [interpolate](#dc.lineChart+interpolate) and [tension](#dc.lineChart+tension)
in dc.js < 3.0

This is passed to
[line.curve](https://github.com/d3/d3-shape/blob/master/README.md#line_curve) and
[area.curve](https://github.com/d3/d3-shape/blob/master/README.md#area_curve).

**Kind**: instance method of [<code>lineChart</code>](#dc.lineChart)  
**See**

- [line.curve](https://github.com/d3/d3-shape/blob/master/README.md#line_curve)
- [area.curve](https://github.com/d3/d3-shape/blob/master/README.md#area_curve)


| Param | Type | Default |
| --- | --- | --- |
| [curve] | <code>d3.curve</code> | <code>d3.curveLinear</code> | 

**Example**  
```js
// default
chart
    .curve(d3.curveLinear);
// Add tension to curves that support it
chart
    .curve(d3.curveCardinal.tension(0.5));
// You can use some specialized variation like
// https://en.wikipedia.org/wiki/Centripetal_Catmull%E2%80%93Rom_spline
chart
    .curve(d3.curveCatmullRom.alpha(0.5));
```
<a name="dc.lineChart+interpolate"></a>

#### ~~lineChart.interpolate([interpolate]) ⇒ <code>d3.curve</code> \| [<code>lineChart</code>](#dc.lineChart)~~
***Deprecated***

Gets or sets the interpolator to use for lines drawn, by string name, allowing e.g. step
functions, splines, and cubic interpolation.

Possible values are: 'linear', 'linear-closed', 'step', 'step-before', 'step-after', 'basis',
'basis-open', 'basis-closed', 'bundle', 'cardinal', 'cardinal-open', 'cardinal-closed', and
'monotone'.

This function exists for backward compatibility. Use [curve](#dc.lineChart+curve)
which is generic and provides more options.
Value set through `.curve` takes precedence over `.interpolate` and `.tension`.

**Kind**: instance method of [<code>lineChart</code>](#dc.lineChart)  
**See**: [curve](#dc.lineChart+curve)  

| Param | Type | Default |
| --- | --- | --- |
| [interpolate] | <code>d3.curve</code> | <code>d3.curveLinear</code> | 

<a name="dc.lineChart+tension"></a>

#### ~~lineChart.tension([tension]) ⇒ <code>Number</code> \| [<code>lineChart</code>](#dc.lineChart)~~
***Deprecated***

Gets or sets the tension to use for lines drawn, in the range 0 to 1.

Passed to the [d3 curve function](https://github.com/d3/d3-shape/blob/master/README.md#curves)
if it provides a `.tension` function. Example:
[curveCardinal.tension](https://github.com/d3/d3-shape/blob/master/README.md#curveCardinal_tension).

This function exists for backward compatibility. Use [curve](#dc.lineChart+curve)
which is generic and provides more options.
Value set through `.curve` takes precedence over `.interpolate` and `.tension`.

**Kind**: instance method of [<code>lineChart</code>](#dc.lineChart)  
**See**: [curve](#dc.lineChart+curve)  

| Param | Type | Default |
| --- | --- | --- |
| [tension] | <code>Number</code> | <code>0</code> | 

<a name="dc.lineChart+defined"></a>

#### lineChart.defined([defined]) ⇒ <code>function</code> \| [<code>lineChart</code>](#dc.lineChart)
Gets or sets a function that will determine discontinuities in the line which should be
skipped: the path will be broken into separate subpaths if some points are undefined.
This function is passed to
[line.defined](https://github.com/d3/d3-shape/blob/master/README.md#line_defined)

Note: crossfilter will sometimes coerce nulls to 0, so you may need to carefully write
custom reduce functions to get this to work, depending on your data. See
[this GitHub comment](https://github.com/dc-js/dc.js/issues/615#issuecomment-49089248)
for more details and an example.

**Kind**: instance method of [<code>lineChart</code>](#dc.lineChart)  
**See**: [line.defined](https://github.com/d3/d3-shape/blob/master/README.md#line_defined)  

| Param | Type |
| --- | --- |
| [defined] | <code>function</code> | 

<a name="dc.lineChart+dashStyle"></a>

#### lineChart.dashStyle([dashStyle]) ⇒ <code>Array.&lt;Number&gt;</code> \| [<code>lineChart</code>](#dc.lineChart)
Set the line's d3 dashstyle. This value becomes the 'stroke-dasharray' of line. Defaults to empty
array (solid line).

**Kind**: instance method of [<code>lineChart</code>](#dc.lineChart)  
**See**: [stroke-dasharray](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/stroke-dasharray)  

| Param | Type | Default |
| --- | --- | --- |
| [dashStyle] | <code>Array.&lt;Number&gt;</code> | <code>[]</code> | 

**Example**  
```js
// create a Dash Dot Dot Dot
chart.dashStyle([3,1,1,1]);
```
<a name="dc.lineChart+renderArea"></a>

#### lineChart.renderArea([renderArea]) ⇒ <code>Boolean</code> \| [<code>lineChart</code>](#dc.lineChart)
Get or set render area flag. If the flag is set to true then the chart will render the area
beneath each line and the line chart effectively becomes an area chart.

**Kind**: instance method of [<code>lineChart</code>](#dc.lineChart)  

| Param | Type | Default |
| --- | --- | --- |
| [renderArea] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.lineChart+xyTipsOn"></a>

#### lineChart.xyTipsOn([xyTipsOn]) ⇒ <code>Boolean</code> \| [<code>lineChart</code>](#dc.lineChart)
Turn on/off the mouseover behavior of an individual data point which renders a circle and x/y axis
dashed lines back to each respective axis.  This is ignored if the chart
[brush](#dc.coordinateGridMixin+brushOn) is on

**Kind**: instance method of [<code>lineChart</code>](#dc.lineChart)  

| Param | Type | Default |
| --- | --- | --- |
| [xyTipsOn] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.lineChart+dotRadius"></a>

#### lineChart.dotRadius([dotRadius]) ⇒ <code>Number</code> \| [<code>lineChart</code>](#dc.lineChart)
Get or set the radius (in px) for dots displayed on the data points.

**Kind**: instance method of [<code>lineChart</code>](#dc.lineChart)  

| Param | Type | Default |
| --- | --- | --- |
| [dotRadius] | <code>Number</code> | <code>5</code> | 

<a name="dc.lineChart+renderDataPoints"></a>

#### lineChart.renderDataPoints([options]) ⇒ <code>Object</code> \| [<code>lineChart</code>](#dc.lineChart)
Always show individual dots for each datapoint.

If `options` is falsy, it disables data point rendering. If no `options` are provided, the
current `options` values are instead returned.

**Kind**: instance method of [<code>lineChart</code>](#dc.lineChart)  

| Param | Type | Default |
| --- | --- | --- |
| [options] | <code>Object</code> | <code>{fillOpacity: 0.8, strokeOpacity: 0.0, radius: 2}</code> | 

**Example**  
```js
chart.renderDataPoints({radius: 2, fillOpacity: 0.8, strokeOpacity: 0.0})
```
<a name="dc.dataCount"></a>

### dc.dataCount
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>baseMixin</code>](#dc.baseMixin)  

* [.dataCount](#dc.dataCount)
    * [new dataCount(parent, [chartGroup])](#new_dc.dataCount_new)
    * [.html([options])](#dc.dataCount+html) ⇒ <code>Object</code> \| [<code>dataCount</code>](#dc.dataCount)
    * [.formatNumber([formatter])](#dc.dataCount+formatNumber) ⇒ <code>function</code> \| [<code>dataCount</code>](#dc.dataCount)

<a name="new_dc.dataCount_new"></a>

#### new dataCount(parent, [chartGroup])
The data count widget is a simple widget designed to display the number of records selected by the
current filters out of the total number of records in the data set. Once created the data count widget
will automatically update the text content of child elements with the following classes:

* `.total-count` - total number of records
* `.filter-count` - number of records matched by the current filters

Note: this widget works best for the specific case of showing the number of records out of a
total. If you want a more general-purpose numeric display, please use the
[numberDisplay](#dc.numberDisplay) widget instead.

Examples:
- [Nasdaq 100 Index](http://dc-js.github.com/dc.js/)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
var ndx = crossfilter(data);
var all = ndx.groupAll();

dc.dataCount('.dc-data-count')
    .crossfilter(ndx)
    .groupAll(all);
```
<a name="dc.dataCount+html"></a>

#### dataCount.html([options]) ⇒ <code>Object</code> \| [<code>dataCount</code>](#dc.dataCount)
Gets or sets an optional object specifying HTML templates to use depending how many items are
selected. The text `%total-count` will replaced with the total number of records, and the text
`%filter-count` will be replaced with the number of selected records.
- all: HTML template to use if all items are selected
- some: HTML template to use if not all items are selected

**Kind**: instance method of [<code>dataCount</code>](#dc.dataCount)  

| Param | Type |
| --- | --- |
| [options] | <code>Object</code> | 

**Example**  
```js
counter.html({
     some: '%filter-count out of %total-count records selected',
     all: 'All records selected. Click on charts to apply filters'
})
```
<a name="dc.dataCount+formatNumber"></a>

#### dataCount.formatNumber([formatter]) ⇒ <code>function</code> \| [<code>dataCount</code>](#dc.dataCount)
Gets or sets an optional function to format the filter count and total count.

**Kind**: instance method of [<code>dataCount</code>](#dc.dataCount)  
**See**: [d3.format](https://github.com/d3/d3-format/blob/master/README.md#format)  

| Param | Type | Default |
| --- | --- | --- |
| [formatter] | <code>function</code> | <code>d3.format(&#x27;.2g&#x27;)</code> | 

**Example**  
```js
counter.formatNumber(d3.format('.2g'))
```
<a name="dc.dataTable"></a>

### dc.dataTable
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>baseMixin</code>](#dc.baseMixin)  

* [.dataTable](#dc.dataTable)
    * [new dataTable(parent, [chartGroup])](#new_dc.dataTable_new)
    * [.section(section)](#dc.dataTable+section) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
    * [.group(groupFunction)](#dc.dataTable+group) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
    * [.size([size])](#dc.dataTable+size) ⇒ <code>Number</code> \| [<code>dataTable</code>](#dc.dataTable)
    * [.beginSlice([beginSlice])](#dc.dataTable+beginSlice) ⇒ <code>Number</code> \| [<code>dataTable</code>](#dc.dataTable)
    * [.endSlice([endSlice])](#dc.dataTable+endSlice) ⇒ <code>Number</code> \| [<code>dataTable</code>](#dc.dataTable)
    * [.columns([columns])](#dc.dataTable+columns) ⇒ <code>Array.&lt;function()&gt;</code>
    * [.sortBy([sortBy])](#dc.dataTable+sortBy) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
    * [.order([order])](#dc.dataTable+order) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
    * [.showSections([showSections])](#dc.dataTable+showSections) ⇒ <code>Boolean</code> \| [<code>dataTable</code>](#dc.dataTable)
    * [.showGroups([showGroups])](#dc.dataTable+showGroups) ⇒ <code>Boolean</code> \| [<code>dataTable</code>](#dc.dataTable)

<a name="new_dc.dataTable_new"></a>

#### new dataTable(parent, [chartGroup])
The data table is a simple widget designed to list crossfilter focused data set (rows being
filtered) in a good old tabular fashion.

An interesting feature of the data table is that you can pass a crossfilter group to the
`dimension`, if you want to show aggregated data instead of raw data rows. This requires no
special code as long as you specify the [order](#dc.dataTable+order) as `d3.descending`,
since the data table will use `dimension.top()` to fetch the data in that case, and the method is
equally supported on the crossfilter group as the crossfilter dimension.

If you want to display aggregated data in ascending order, you will need to wrap the group
in a [fake dimension](https://github.com/dc-js/dc.js/wiki/FAQ#fake-dimensions) to support the
`.bottom()` method. See the example linked below for more details.

Note: Formerly the data table (and data grid chart) used the [group](#dc.dataTable+group) attribute as a
keying function for [nesting](https://github.com/d3/d3-collection/blob/master/README.md#nest) the data
together in sections.  This was confusing so it has been renamed to `section`, although `group` still works.

Examples:
- [Nasdaq 100 Index](http://dc-js.github.com/dc.js/)
- [dataTable on a crossfilter group](http://dc-js.github.io/dc.js/examples/table-on-aggregated-data.html)
([source](https://github.com/dc-js/dc.js/blob/develop/web/examples/table-on-aggregated-data.html))


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

<a name="dc.dataTable+section"></a>

#### dataTable.section(section) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
Get or set the section function for the data table. The section function takes a data row and
returns the key to specify to [d3.nest](https://github.com/d3/d3-collection/blob/master/README.md#nest)
to split rows into sections. By default there will be only one section with no name.

Set [showSections](#dc.dataTable+showSections) to false to hide the section headers

**Kind**: instance method of [<code>dataTable</code>](#dc.dataTable)  

| Param | Type | Description |
| --- | --- | --- |
| section | <code>function</code> | Function taking a row of data and returning the nest key. |

**Example**  
```js
// section rows by the value of their field
chart
    .section(function(d) { return d.field; })
```
<a name="dc.dataTable+group"></a>

#### dataTable.group(groupFunction) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
Backward-compatible synonym for [section](#dc.dataTable+section).

**Kind**: instance method of [<code>dataTable</code>](#dc.dataTable)  

| Param | Type | Description |
| --- | --- | --- |
| groupFunction | <code>function</code> | Function taking a row of data and returning the nest key. |

<a name="dc.dataTable+size"></a>

#### dataTable.size([size]) ⇒ <code>Number</code> \| [<code>dataTable</code>](#dc.dataTable)
Get or set the table size which determines the number of rows displayed by the widget.

**Kind**: instance method of [<code>dataTable</code>](#dc.dataTable)  

| Param | Type | Default |
| --- | --- | --- |
| [size] | <code>Number</code> | <code>25</code> | 

<a name="dc.dataTable+beginSlice"></a>

#### dataTable.beginSlice([beginSlice]) ⇒ <code>Number</code> \| [<code>dataTable</code>](#dc.dataTable)
Get or set the index of the beginning slice which determines which entries get displayed
by the widget. Useful when implementing pagination.

Note: the sortBy function will determine how the rows are ordered for pagination purposes.
See the [table pagination example](http://dc-js.github.io/dc.js/examples/table-pagination.html)
to see how to implement the pagination user interface using `beginSlice` and `endSlice`.

**Kind**: instance method of [<code>dataTable</code>](#dc.dataTable)  

| Param | Type | Default |
| --- | --- | --- |
| [beginSlice] | <code>Number</code> | <code>0</code> | 

<a name="dc.dataTable+endSlice"></a>

#### dataTable.endSlice([endSlice]) ⇒ <code>Number</code> \| [<code>dataTable</code>](#dc.dataTable)
Get or set the index of the end slice which determines which entries get displayed by the
widget. Useful when implementing pagination. See [`beginSlice`](#dc.dataTable+beginSlice) for more information.

**Kind**: instance method of [<code>dataTable</code>](#dc.dataTable)  

| Param | Type |
| --- | --- |
| [endSlice] | <code>Number</code> \| <code>undefined</code> | 

<a name="dc.dataTable+columns"></a>

#### dataTable.columns([columns]) ⇒ <code>Array.&lt;function()&gt;</code>
Get or set column functions. The data table widget supports several methods of specifying the
columns to display.

The original method uses an array of functions to generate dynamic columns. Column functions
are simple javascript functions with only one input argument `d` which represents a row in
the data set. The return value of these functions will be used to generate the content for
each cell. However, this method requires the HTML for the table to have a fixed set of column
headers.

<pre><code>chart.columns([
    function(d) { return d.date; },
    function(d) { return d.open; },
    function(d) { return d.close; },
    function(d) { return numberFormat(d.close - d.open); },
    function(d) { return d.volume; }
]);
</code></pre>

In the second method, you can list the columns to read from the data without specifying it as
a function, except where necessary (ie, computed columns).  Note the data element name is
capitalized when displayed in the table header. You can also mix in functions as necessary,
using the third `{label, format}` form, as shown below.

<pre><code>chart.columns([
    "date",    // d["date"], ie, a field accessor; capitalized automatically
    "open",    // ...
    "close",   // ...
    {
        label: "Change",
        format: function (d) {
            return numberFormat(d.close - d.open);
        }
    },
    "volume"   // d["volume"], ie, a field accessor; capitalized automatically
]);
</code></pre>

In the third example, we specify all fields using the `{label, format}` method:
<pre><code>chart.columns([
    {
        label: "Date",
        format: function (d) { return d.date; }
    },
    {
        label: "Open",
        format: function (d) { return numberFormat(d.open); }
    },
    {
        label: "Close",
        format: function (d) { return numberFormat(d.close); }
    },
    {
        label: "Change",
        format: function (d) { return numberFormat(d.close - d.open); }
    },
    {
        label: "Volume",
        format: function (d) { return d.volume; }
    }
]);
</code></pre>

You may wish to override the dataTable functions `_doColumnHeaderCapitalize` and
`_doColumnHeaderFnToString`, which are used internally to translate the column information or
function into a displayed header. The first one is used on the "string" column specifier; the
second is used to transform a stringified function into something displayable. For the Stock
example, the function for Change becomes the table header **d.close - d.open**.

Finally, you can even specify a completely different form of column definition. To do this,
override `_chart._doColumnHeaderFormat` and `_chart._doColumnValueFormat` Be aware that
fields without numberFormat specification will be displayed just as they are stored in the
data, unformatted.

**Kind**: instance method of [<code>dataTable</code>](#dc.dataTable)  
**Returns**: <code>Array.&lt;function()&gt;</code> - |dc.dataTable}  

| Param | Type | Default |
| --- | --- | --- |
| [columns] | <code>Array.&lt;function()&gt;</code> | <code>[]</code> | 

<a name="dc.dataTable+sortBy"></a>

#### dataTable.sortBy([sortBy]) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
Get or set sort-by function. This function works as a value accessor at row level and returns a
particular field to be sorted by.

**Kind**: instance method of [<code>dataTable</code>](#dc.dataTable)  

| Param | Type | Default |
| --- | --- | --- |
| [sortBy] | <code>function</code> | <code>identity function</code> | 

**Example**  
```js
chart.sortBy(function(d) {
    return d.date;
});
```
<a name="dc.dataTable+order"></a>

#### dataTable.order([order]) ⇒ <code>function</code> \| [<code>dataTable</code>](#dc.dataTable)
Get or set sort order. If the order is `d3.ascending`, the data table will use
`dimension().bottom()` to fetch the data; otherwise it will use `dimension().top()`

**Kind**: instance method of [<code>dataTable</code>](#dc.dataTable)  
**See**

- [d3.ascending](https://github.com/d3/d3-array/blob/master/README.md#ascending)
- [d3.descending](https://github.com/d3/d3-array/blob/master/README.md#descending)


| Param | Type | Default |
| --- | --- | --- |
| [order] | <code>function</code> | <code>d3.ascending</code> | 

**Example**  
```js
chart.order(d3.descending);
```
<a name="dc.dataTable+showSections"></a>

#### dataTable.showSections([showSections]) ⇒ <code>Boolean</code> \| [<code>dataTable</code>](#dc.dataTable)
Get or set if section header rows will be shown.

**Kind**: instance method of [<code>dataTable</code>](#dc.dataTable)  

| Param | Type | Default |
| --- | --- | --- |
| [showSections] | <code>Boolean</code> | <code>true</code> | 

**Example**  
```js
chart
    .section([value], [name])
    .showSections(true|false);
```
<a name="dc.dataTable+showGroups"></a>

#### dataTable.showGroups([showGroups]) ⇒ <code>Boolean</code> \| [<code>dataTable</code>](#dc.dataTable)
Backward-compatible synonym for [showSections](#dc.dataTable+showSections).

**Kind**: instance method of [<code>dataTable</code>](#dc.dataTable)  

| Param | Type | Default |
| --- | --- | --- |
| [showGroups] | <code>Boolean</code> | <code>true</code> | 

<a name="dc.dataGrid"></a>

### dc.dataGrid
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>baseMixin</code>](#dc.baseMixin)  

* [.dataGrid](#dc.dataGrid)
    * [new dataGrid(parent, [chartGroup])](#new_dc.dataGrid_new)
    * [.section(section)](#dc.dataGrid+section) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
    * [.group(groupFunction)](#dc.dataGrid+group) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
    * [.beginSlice([beginSlice])](#dc.dataGrid+beginSlice) ⇒ <code>Number</code> \| [<code>dataGrid</code>](#dc.dataGrid)
    * [.endSlice([endSlice])](#dc.dataGrid+endSlice) ⇒ <code>Number</code> \| [<code>dataGrid</code>](#dc.dataGrid)
    * [.size([size])](#dc.dataGrid+size) ⇒ <code>Number</code> \| [<code>dataGrid</code>](#dc.dataGrid)
    * [.html([html])](#dc.dataGrid+html) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
    * [.htmlSection([htmlSection])](#dc.dataGrid+htmlSection) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
    * [.htmlGroup([htmlGroup])](#dc.dataGrid+htmlGroup) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
    * [.sortBy([sortByFunction])](#dc.dataGrid+sortBy) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
    * [.order([order])](#dc.dataGrid+order) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)

<a name="new_dc.dataGrid_new"></a>

#### new dataGrid(parent, [chartGroup])
Data grid is a simple widget designed to list the filtered records, providing
a simple way to define how the items are displayed.


Note: Formerly the data grid chart (and data table) used the [group](#dc.dataGrid+group) attribute as a
keying function for [nesting](https://github.com/d3/d3-collection/blob/master/README.md#nest) the data
together in sections.  This was confusing so it has been renamed to `section`, although `group` still works.

Examples:
- [List of members of the european parliament](http://europarl.me/dc.js/web/ep/index.html)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

<a name="dc.dataGrid+section"></a>

#### dataGrid.section(section) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
Get or set the section function for the data grid. The section function takes a data row and
returns the key to specify to [d3.nest](https://github.com/d3/d3-collection/blob/master/README.md#nest)
to split rows into sections.

Do not pass in a crossfilter section as this will not work.

**Kind**: instance method of [<code>dataGrid</code>](#dc.dataGrid)  

| Param | Type | Description |
| --- | --- | --- |
| section | <code>function</code> | Function taking a row of data and returning the nest key. |

**Example**  
```js
// section rows by the value of their field
chart
    .section(function(d) { return d.field; })
```
<a name="dc.dataGrid+group"></a>

#### dataGrid.group(groupFunction) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
Backward-compatible synonym for [section](#dc.dataGrid+section).

**Kind**: instance method of [<code>dataGrid</code>](#dc.dataGrid)  

| Param | Type | Description |
| --- | --- | --- |
| groupFunction | <code>function</code> | Function taking a row of data and returning the nest key. |

<a name="dc.dataGrid+beginSlice"></a>

#### dataGrid.beginSlice([beginSlice]) ⇒ <code>Number</code> \| [<code>dataGrid</code>](#dc.dataGrid)
Get or set the index of the beginning slice which determines which entries get displayed by the widget.
Useful when implementing pagination.

**Kind**: instance method of [<code>dataGrid</code>](#dc.dataGrid)  

| Param | Type | Default |
| --- | --- | --- |
| [beginSlice] | <code>Number</code> | <code>0</code> | 

<a name="dc.dataGrid+endSlice"></a>

#### dataGrid.endSlice([endSlice]) ⇒ <code>Number</code> \| [<code>dataGrid</code>](#dc.dataGrid)
Get or set the index of the end slice which determines which entries get displayed by the widget.
Useful when implementing pagination.

**Kind**: instance method of [<code>dataGrid</code>](#dc.dataGrid)  

| Param | Type |
| --- | --- |
| [endSlice] | <code>Number</code> | 

<a name="dc.dataGrid+size"></a>

#### dataGrid.size([size]) ⇒ <code>Number</code> \| [<code>dataGrid</code>](#dc.dataGrid)
Get or set the grid size which determines the number of items displayed by the widget.

**Kind**: instance method of [<code>dataGrid</code>](#dc.dataGrid)  

| Param | Type | Default |
| --- | --- | --- |
| [size] | <code>Number</code> | <code>999</code> | 

<a name="dc.dataGrid+html"></a>

#### dataGrid.html([html]) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
Get or set the function that formats an item. The data grid widget uses a
function to generate dynamic html. Use your favourite templating engine or
generate the string directly.

**Kind**: instance method of [<code>dataGrid</code>](#dc.dataGrid)  

| Param | Type |
| --- | --- |
| [html] | <code>function</code> | 

**Example**  
```js
chart.html(function (d) { return '<div class='item '+data.exampleCategory+''>'+data.exampleString+'</div>';});
```
<a name="dc.dataGrid+htmlSection"></a>

#### dataGrid.htmlSection([htmlSection]) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
Get or set the function that formats a section label.

**Kind**: instance method of [<code>dataGrid</code>](#dc.dataGrid)  

| Param | Type |
| --- | --- |
| [htmlSection] | <code>function</code> | 

**Example**  
```js
chart.htmlSection (function (d) { return '<h2>'.d.key . 'with ' . d.values.length .' items</h2>'});
```
<a name="dc.dataGrid+htmlGroup"></a>

#### dataGrid.htmlGroup([htmlGroup]) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
Backward-compatible synonym for [htmlSection](#dc.dataGrid+htmlSection).

**Kind**: instance method of [<code>dataGrid</code>](#dc.dataGrid)  

| Param | Type |
| --- | --- |
| [htmlGroup] | <code>function</code> | 

<a name="dc.dataGrid+sortBy"></a>

#### dataGrid.sortBy([sortByFunction]) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
Get or set sort-by function. This function works as a value accessor at the item
level and returns a particular field to be sorted.

**Kind**: instance method of [<code>dataGrid</code>](#dc.dataGrid)  

| Param | Type |
| --- | --- |
| [sortByFunction] | <code>function</code> | 

**Example**  
```js
chart.sortBy(function(d) {
    return d.date;
});
```
<a name="dc.dataGrid+order"></a>

#### dataGrid.order([order]) ⇒ <code>function</code> \| [<code>dataGrid</code>](#dc.dataGrid)
Get or set sort the order function.

**Kind**: instance method of [<code>dataGrid</code>](#dc.dataGrid)  
**See**

- [d3.ascending](https://github.com/d3/d3-array/blob/master/README.md#ascending)
- [d3.descending](https://github.com/d3/d3-array/blob/master/README.md#descending)


| Param | Type | Default |
| --- | --- | --- |
| [order] | <code>function</code> | <code>d3.ascending</code> | 

**Example**  
```js
chart.order(d3.descending);
```
<a name="dc.bubbleChart"></a>

### dc.bubbleChart
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>bubbleMixin</code>](#dc.bubbleMixin), [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

* [.bubbleChart](#dc.bubbleChart)
    * [new bubbleChart(parent, [chartGroup])](#new_dc.bubbleChart_new)
    * [.elasticRadius([elasticRadius])](#dc.bubbleChart+elasticRadius) ⇒ <code>Boolean</code> \| [<code>bubbleChart</code>](#dc.bubbleChart)
    * [.sortBubbleSize([sortBubbleSize])](#dc.bubbleChart+sortBubbleSize) ⇒ <code>Boolean</code> \| [<code>bubbleChart</code>](#dc.bubbleChart)

<a name="new_dc.bubbleChart_new"></a>

#### new bubbleChart(parent, [chartGroup])
A concrete implementation of a general purpose bubble chart that allows data visualization using the
following dimensions:
- x axis position
- y axis position
- bubble radius
- color

Examples:
- [Nasdaq 100 Index](http://dc-js.github.com/dc.js/)
- [US Venture Capital Landscape 2011](http://dc-js.github.com/dc.js/vc/index.html)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a bubble chart under #chart-container1 element using the default global chart group
var bubbleChart1 = dc.bubbleChart('#chart-container1');
// create a bubble chart under #chart-container2 element using chart group A
var bubbleChart2 = dc.bubbleChart('#chart-container2', 'chartGroupA');
```
<a name="dc.bubbleChart+elasticRadius"></a>

#### bubbleChart.elasticRadius([elasticRadius]) ⇒ <code>Boolean</code> \| [<code>bubbleChart</code>](#dc.bubbleChart)
Turn on or off the elastic bubble radius feature, or return the value of the flag. If this
feature is turned on, then bubble radii will be automatically rescaled to fit the chart better.

**Kind**: instance method of [<code>bubbleChart</code>](#dc.bubbleChart)  

| Param | Type | Default |
| --- | --- | --- |
| [elasticRadius] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.bubbleChart+sortBubbleSize"></a>

#### bubbleChart.sortBubbleSize([sortBubbleSize]) ⇒ <code>Boolean</code> \| [<code>bubbleChart</code>](#dc.bubbleChart)
Turn on or off the bubble sorting feature, or return the value of the flag. If enabled,
bubbles will be sorted by their radius, with smaller bubbles in front.

**Kind**: instance method of [<code>bubbleChart</code>](#dc.bubbleChart)  

| Param | Type | Default |
| --- | --- | --- |
| [sortBubbleSize] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.compositeChart"></a>

### dc.compositeChart
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

* [.compositeChart](#dc.compositeChart)
    * [new compositeChart(parent, [chartGroup])](#new_dc.compositeChart_new)
    * [.useRightAxisGridLines([useRightAxisGridLines])](#dc.compositeChart+useRightAxisGridLines) ⇒ <code>Boolean</code> \| [<code>compositeChart</code>](#dc.compositeChart)
    * [.childOptions([childOptions])](#dc.compositeChart+childOptions) ⇒ <code>Object</code> \| [<code>compositeChart</code>](#dc.compositeChart)
    * [.rightYAxisLabel([rightYAxisLabel], [padding])](#dc.compositeChart+rightYAxisLabel) ⇒ <code>String</code> \| [<code>compositeChart</code>](#dc.compositeChart)
    * [.compose([subChartArray])](#dc.compositeChart+compose) ⇒ [<code>compositeChart</code>](#dc.compositeChart)
    * [.children()](#dc.compositeChart+children) ⇒ [<code>Array.&lt;baseMixin&gt;</code>](#dc.baseMixin)
    * [.shareColors([shareColors])](#dc.compositeChart+shareColors) ⇒ <code>Boolean</code> \| [<code>compositeChart</code>](#dc.compositeChart)
    * [.shareTitle([shareTitle])](#dc.compositeChart+shareTitle) ⇒ <code>Boolean</code> \| [<code>compositeChart</code>](#dc.compositeChart)
    * [.rightY([yScale])](#dc.compositeChart+rightY) ⇒ <code>d3.scale</code> \| [<code>compositeChart</code>](#dc.compositeChart)
    * [.alignYAxes([alignYAxes])](#dc.compositeChart+alignYAxes) ⇒ <code>Chart</code>
    * [.rightYAxis([rightYAxis])](#dc.compositeChart+rightYAxis) ⇒ <code>d3.axisRight</code> \| [<code>compositeChart</code>](#dc.compositeChart)

<a name="new_dc.compositeChart_new"></a>

#### new compositeChart(parent, [chartGroup])
Composite charts are a special kind of chart that render multiple charts on the same Coordinate
Grid. You can overlay (compose) different bar/line/area charts in a single composite chart to
achieve some quite flexible charting effects.


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a composite chart under #chart-container1 element using the default global chart group
var compositeChart1 = dc.compositeChart('#chart-container1');
// create a composite chart under #chart-container2 element using chart group A
var compositeChart2 = dc.compositeChart('#chart-container2', 'chartGroupA');
```
<a name="dc.compositeChart+useRightAxisGridLines"></a>

#### compositeChart.useRightAxisGridLines([useRightAxisGridLines]) ⇒ <code>Boolean</code> \| [<code>compositeChart</code>](#dc.compositeChart)
Get or set whether to draw gridlines from the right y axis.  Drawing from the left y axis is the
default behavior. This option is only respected when subcharts with both left and right y-axes
are present.

**Kind**: instance method of [<code>compositeChart</code>](#dc.compositeChart)  

| Param | Type | Default |
| --- | --- | --- |
| [useRightAxisGridLines] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.compositeChart+childOptions"></a>

#### compositeChart.childOptions([childOptions]) ⇒ <code>Object</code> \| [<code>compositeChart</code>](#dc.compositeChart)
Get or set chart-specific options for all child charts. This is equivalent to calling
[.options](#dc.baseMixin+options) on each child chart.

**Kind**: instance method of [<code>compositeChart</code>](#dc.compositeChart)  

| Param | Type |
| --- | --- |
| [childOptions] | <code>Object</code> | 

<a name="dc.compositeChart+rightYAxisLabel"></a>

#### compositeChart.rightYAxisLabel([rightYAxisLabel], [padding]) ⇒ <code>String</code> \| [<code>compositeChart</code>](#dc.compositeChart)
Set or get the right y axis label.

**Kind**: instance method of [<code>compositeChart</code>](#dc.compositeChart)  

| Param | Type |
| --- | --- |
| [rightYAxisLabel] | <code>String</code> | 
| [padding] | <code>Number</code> | 

<a name="dc.compositeChart+compose"></a>

#### compositeChart.compose([subChartArray]) ⇒ [<code>compositeChart</code>](#dc.compositeChart)
Combine the given charts into one single composite coordinate grid chart.

**Kind**: instance method of [<code>compositeChart</code>](#dc.compositeChart)  

| Param | Type |
| --- | --- |
| [subChartArray] | <code>Array.&lt;Chart&gt;</code> | 

**Example**  
```js
moveChart.compose([
    // when creating sub-chart you need to pass in the parent chart
    dc.lineChart(moveChart)
        .group(indexAvgByMonthGroup) // if group is missing then parent's group will be used
        .valueAccessor(function (d){return d.value.avg;})
        // most of the normal functions will continue to work in a composed chart
        .renderArea(true)
        .stack(monthlyMoveGroup, function (d){return d.value;})
        .title(function (d){
            var value = d.value.avg?d.value.avg:d.value;
            if(isNaN(value)) value = 0;
            return dateFormat(d.key) + '\n' + numberFormat(value);
        }),
    dc.barChart(moveChart)
        .group(volumeByMonthGroup)
        .centerBar(true)
]);
```
<a name="dc.compositeChart+children"></a>

#### compositeChart.children() ⇒ [<code>Array.&lt;baseMixin&gt;</code>](#dc.baseMixin)
Returns the child charts which are composed into the composite chart.

**Kind**: instance method of [<code>compositeChart</code>](#dc.compositeChart)  
<a name="dc.compositeChart+shareColors"></a>

#### compositeChart.shareColors([shareColors]) ⇒ <code>Boolean</code> \| [<code>compositeChart</code>](#dc.compositeChart)
Get or set color sharing for the chart. If set, the [.colors()](#dc.colorMixin+colors) value from this chart
will be shared with composed children. Additionally if the child chart implements
Stackable and has not set a custom .colorAccessor, then it will generate a color
specific to its order in the composition.

**Kind**: instance method of [<code>compositeChart</code>](#dc.compositeChart)  

| Param | Type | Default |
| --- | --- | --- |
| [shareColors] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.compositeChart+shareTitle"></a>

#### compositeChart.shareTitle([shareTitle]) ⇒ <code>Boolean</code> \| [<code>compositeChart</code>](#dc.compositeChart)
Get or set title sharing for the chart. If set, the [.title()](#dc.baseMixin+title) value from
this chart will be shared with composed children.

Note: currently you must call this before `compose` or the child will still get the parent's
`title` function!

**Kind**: instance method of [<code>compositeChart</code>](#dc.compositeChart)  

| Param | Type | Default |
| --- | --- | --- |
| [shareTitle] | <code>Boolean</code> | <code>true</code> | 

<a name="dc.compositeChart+rightY"></a>

#### compositeChart.rightY([yScale]) ⇒ <code>d3.scale</code> \| [<code>compositeChart</code>](#dc.compositeChart)
Get or set the y scale for the right axis. The right y scale is typically automatically
generated by the chart implementation.

**Kind**: instance method of [<code>compositeChart</code>](#dc.compositeChart)  
**See**: [d3.scale](https://github.com/d3/d3-scale/blob/master/README.md)  

| Param | Type |
| --- | --- |
| [yScale] | <code>d3.scale</code> | 

<a name="dc.compositeChart+alignYAxes"></a>

#### compositeChart.alignYAxes([alignYAxes]) ⇒ <code>Chart</code>
Get or set alignment between left and right y axes. A line connecting '0' on both y axis
will be parallel to x axis. This only has effect when [elasticY](#dc.coordinateGridMixin+elasticY) is true.

**Kind**: instance method of [<code>compositeChart</code>](#dc.compositeChart)  

| Param | Type | Default |
| --- | --- | --- |
| [alignYAxes] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.compositeChart+rightYAxis"></a>

#### compositeChart.rightYAxis([rightYAxis]) ⇒ <code>d3.axisRight</code> \| [<code>compositeChart</code>](#dc.compositeChart)
Set or get the right y axis used by the composite chart. This function is most useful when y
axis customization is required. The y axis in dc.js is an instance of a
[d3.axisRight](https://github.com/d3/d3-axis/blob/master/README.md#axisRight) therefore it supports any valid
d3 axis manipulation.

**Caution**: The right y axis is usually generated internally by dc; resetting it may cause
unexpected results.  Note also that when used as a getter, this function is not chainable: it
returns the axis, not the chart,
{@link https://github.com/dc-js/dc.js/wiki/FAQ#why-does-everything-break-after-a-call-to-xaxis-or-yaxis
so attempting to call chart functions after calling `.yAxis()` will fail}.

**Kind**: instance method of [<code>compositeChart</code>](#dc.compositeChart)  
**See**: [https://github.com/d3/d3-axis/blob/master/README.md#axisRight](https://github.com/d3/d3-axis/blob/master/README.md#axisRight)  

| Param | Type |
| --- | --- |
| [rightYAxis] | <code>d3.axisRight</code> | 

**Example**  
```js
// customize y axis tick format
chart.rightYAxis().tickFormat(function (v) {return v + '%';});
// customize y axis tick values
chart.rightYAxis().tickValues([0, 100, 200, 300]);
```
<a name="dc.seriesChart"></a>

### dc.seriesChart
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>compositeChart</code>](#dc.compositeChart)  

* [.seriesChart](#dc.seriesChart)
    * [new seriesChart(parent, [chartGroup])](#new_dc.seriesChart_new)
    * [.chart([chartFunction])](#dc.seriesChart+chart) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)
    * [.seriesAccessor([accessor])](#dc.seriesChart+seriesAccessor) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)
    * [.seriesSort([sortFunction])](#dc.seriesChart+seriesSort) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)
    * [.valueSort([sortFunction])](#dc.seriesChart+valueSort) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)

<a name="new_dc.seriesChart_new"></a>

#### new seriesChart(parent, [chartGroup])
A series chart is a chart that shows multiple series of data overlaid on one chart, where the
series is specified in the data. It is a specialization of Composite Chart and inherits all
composite features other than recomposing the chart.

Examples:
- [Series Chart](http://dc-js.github.io/dc.js/examples/series.html)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a series chart under #chart-container1 element using the default global chart group
var seriesChart1 = dc.seriesChart("#chart-container1");
// create a series chart under #chart-container2 element using chart group A
var seriesChart2 = dc.seriesChart("#chart-container2", "chartGroupA");
```
<a name="dc.seriesChart+chart"></a>

#### seriesChart.chart([chartFunction]) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)
Get or set the chart function, which generates the child charts.

**Kind**: instance method of [<code>seriesChart</code>](#dc.seriesChart)  

| Param | Type | Default |
| --- | --- | --- |
| [chartFunction] | <code>function</code> | <code>dc.lineChart</code> | 

**Example**  
```js
// put curve on the line charts used for the series
chart.chart(function(c) { return dc.lineChart(c).curve(d3.curveBasis); })
// do a scatter series chart
chart.chart(dc.scatterPlot)
```
<a name="dc.seriesChart+seriesAccessor"></a>

#### seriesChart.seriesAccessor([accessor]) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)
**mandatory**

Get or set accessor function for the displayed series. Given a datum, this function
should return the series that datum belongs to.

**Kind**: instance method of [<code>seriesChart</code>](#dc.seriesChart)  

| Param | Type |
| --- | --- |
| [accessor] | <code>function</code> | 

**Example**  
```js
// simple series accessor
chart.seriesAccessor(function(d) { return "Expt: " + d.key[0]; })
```
<a name="dc.seriesChart+seriesSort"></a>

#### seriesChart.seriesSort([sortFunction]) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)
Get or set a function to sort the list of series by, given series values.

**Kind**: instance method of [<code>seriesChart</code>](#dc.seriesChart)  
**See**

- [d3.ascending](https://github.com/d3/d3-array/blob/master/README.md#ascending)
- [d3.descending](https://github.com/d3/d3-array/blob/master/README.md#descending)


| Param | Type | Default |
| --- | --- | --- |
| [sortFunction] | <code>function</code> | <code>d3.ascending</code> | 

**Example**  
```js
chart.seriesSort(d3.descending);
```
<a name="dc.seriesChart+valueSort"></a>

#### seriesChart.valueSort([sortFunction]) ⇒ <code>function</code> \| [<code>seriesChart</code>](#dc.seriesChart)
Get or set a function to sort each series values by. By default this is the key accessor which,
for example, will ensure a lineChart series connects its points in increasing key/x order,
rather than haphazardly.

**Kind**: instance method of [<code>seriesChart</code>](#dc.seriesChart)  
**See**

- [d3.ascending](https://github.com/d3/d3-array/blob/master/README.md#ascending)
- [d3.descending](https://github.com/d3/d3-array/blob/master/README.md#descending)


| Param | Type |
| --- | --- |
| [sortFunction] | <code>function</code> | 

**Example**  
```js
// Default value sort
_chart.valueSort(function keySort (a, b) {
    return d3.ascending(_chart.keyAccessor()(a), _chart.keyAccessor()(b));
});
```
<a name="dc.geoChoroplethChart"></a>

### dc.geoChoroplethChart
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>colorMixin</code>](#dc.colorMixin), [<code>baseMixin</code>](#dc.baseMixin)  

* [.geoChoroplethChart](#dc.geoChoroplethChart)
    * [new geoChoroplethChart(parent, [chartGroup])](#new_dc.geoChoroplethChart_new)
    * [.overlayGeoJson(json, name, keyAccessor)](#dc.geoChoroplethChart+overlayGeoJson) ⇒ [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)
    * [.projection([projection])](#dc.geoChoroplethChart+projection) ⇒ <code>d3.projection</code> \| [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)
    * [.geoJsons()](#dc.geoChoroplethChart+geoJsons) ⇒ <code>Array.&lt;{name:String, data: Object, accessor: function()}&gt;</code>
    * [.geoPath()](#dc.geoChoroplethChart+geoPath) ⇒ <code>d3.geoPath</code>
    * [.removeGeoJson(name)](#dc.geoChoroplethChart+removeGeoJson) ⇒ [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)

<a name="new_dc.geoChoroplethChart_new"></a>

#### new geoChoroplethChart(parent, [chartGroup])
The geo choropleth chart is designed as an easy way to create a crossfilter driven choropleth map
from GeoJson data. This chart implementation was inspired by
[the great d3 choropleth example](http://bl.ocks.org/4060606).

Examples:
- [US Venture Capital Landscape 2011](http://dc-js.github.com/dc.js/vc/index.html)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a choropleth chart under '#us-chart' element using the default global chart group
var chart1 = dc.geoChoroplethChart('#us-chart');
// create a choropleth chart under '#us-chart2' element using chart group A
var chart2 = dc.compositeChart('#us-chart2', 'chartGroupA');
```
<a name="dc.geoChoroplethChart+overlayGeoJson"></a>

#### geoChoroplethChart.overlayGeoJson(json, name, keyAccessor) ⇒ [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)
**mandatory**

Use this function to insert a new GeoJson map layer. This function can be invoked multiple times
if you have multiple GeoJson data layers to render on top of each other. If you overlay multiple
layers with the same name the new overlay will override the existing one.

**Kind**: instance method of [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)  
**See**

- [GeoJSON](http://geojson.org/)
- [TopoJSON](https://github.com/topojson/topojson/wiki)
- [topojson.feature](https://github.com/topojson/topojson-1.x-api-reference/blob/master/API-Reference.md#wiki-feature)


| Param | Type | Description |
| --- | --- | --- |
| json | <code>geoJson</code> | a geojson feed |
| name | <code>String</code> | name of the layer |
| keyAccessor | <code>function</code> | accessor function used to extract 'key' from the GeoJson data. The key extracted by this function should match the keys returned by the crossfilter groups. |

**Example**  
```js
// insert a layer for rendering US states
chart.overlayGeoJson(statesJson.features, 'state', function(d) {
     return d.properties.name;
});
```
<a name="dc.geoChoroplethChart+projection"></a>

#### geoChoroplethChart.projection([projection]) ⇒ <code>d3.projection</code> \| [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)
Gets or sets a custom geo projection function. See the available
[d3 geo projection functions](https://github.com/d3/d3-geo/blob/master/README.md#projections).

Starting version 3.0 it has been deprecated to rely on the default projection being
[d3.geoAlbersUsa()](https://github.com/d3/d3-geo/blob/master/README.md#geoAlbersUsa). Please
set it explicitly. {@link https://bl.ocks.org/mbostock/5557726
Considering that `null` is also a valid value for projection}, if you need
projection to be `null` please set it explicitly to `null`.

**Kind**: instance method of [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)  
**See**

- [d3.projection](https://github.com/d3/d3-geo/blob/master/README.md#projections)
- [d3-geo-projection](https://github.com/d3/d3-geo-projection)


| Param | Type | Default |
| --- | --- | --- |
| [projection] | <code>d3.projection</code> | <code>d3.geoAlbersUsa()</code> | 

<a name="dc.geoChoroplethChart+geoJsons"></a>

#### geoChoroplethChart.geoJsons() ⇒ <code>Array.&lt;{name:String, data: Object, accessor: function()}&gt;</code>
Returns all GeoJson layers currently registered with this chart. The returned array is a
reference to this chart's internal data structure, so any modification to this array will also
modify this chart's internal registration.

**Kind**: instance method of [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)  
<a name="dc.geoChoroplethChart+geoPath"></a>

#### geoChoroplethChart.geoPath() ⇒ <code>d3.geoPath</code>
Returns the [d3.geoPath](https://github.com/d3/d3-geo/blob/master/README.md#paths) object used to
render the projection and features.  Can be useful for figuring out the bounding box of the
feature set and thus a way to calculate scale and translation for the projection.

**Kind**: instance method of [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)  
**See**: [d3.geoPath](https://github.com/d3/d3-geo/blob/master/README.md#paths)  
<a name="dc.geoChoroplethChart+removeGeoJson"></a>

#### geoChoroplethChart.removeGeoJson(name) ⇒ [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)
Remove a GeoJson layer from this chart by name

**Kind**: instance method of [<code>geoChoroplethChart</code>](#dc.geoChoroplethChart)  

| Param | Type |
| --- | --- |
| name | <code>String</code> | 

<a name="dc.bubbleOverlay"></a>

### dc.bubbleOverlay
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>bubbleMixin</code>](#dc.bubbleMixin), [<code>baseMixin</code>](#dc.baseMixin)  

* [.bubbleOverlay](#dc.bubbleOverlay)
    * [new bubbleOverlay(parent, [chartGroup])](#new_dc.bubbleOverlay_new)
    * [.svg([imageElement])](#dc.bubbleOverlay+svg) ⇒ [<code>bubbleOverlay</code>](#dc.bubbleOverlay)
    * [.point(name, x, y)](#dc.bubbleOverlay+point) ⇒ [<code>bubbleOverlay</code>](#dc.bubbleOverlay)

<a name="new_dc.bubbleOverlay_new"></a>

#### new bubbleOverlay(parent, [chartGroup])
The bubble overlay chart is quite different from the typical bubble chart. With the bubble overlay
chart you can arbitrarily place bubbles on an existing svg or bitmap image, thus changing the
typical x and y positioning while retaining the capability to visualize data using bubble radius
and coloring.

Examples:
- [Canadian City Crime Stats](http://dc-js.github.com/dc.js/crime/index.html)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a bubble overlay chart on top of the '#chart-container1 svg' element using the default global chart group
var bubbleChart1 = dc.bubbleOverlayChart('#chart-container1').svg(d3.select('#chart-container1 svg'));
// create a bubble overlay chart on top of the '#chart-container2 svg' element using chart group A
var bubbleChart2 = dc.compositeChart('#chart-container2', 'chartGroupA').svg(d3.select('#chart-container2 svg'));
```
<a name="dc.bubbleOverlay+svg"></a>

#### bubbleOverlay.svg([imageElement]) ⇒ [<code>bubbleOverlay</code>](#dc.bubbleOverlay)
**mandatory**

Set the underlying svg image element. Unlike other dc charts this chart will not generate a svg
element; therefore the bubble overlay chart will not work if this function is not invoked. If the
underlying image is a bitmap, then an empty svg will need to be created on top of the image.

**Kind**: instance method of [<code>bubbleOverlay</code>](#dc.bubbleOverlay)  

| Param | Type |
| --- | --- |
| [imageElement] | <code>SVGElement</code> \| <code>d3.selection</code> | 

**Example**  
```js
// set up underlying svg element
chart.svg(d3.select('#chart svg'));
```
<a name="dc.bubbleOverlay+point"></a>

#### bubbleOverlay.point(name, x, y) ⇒ [<code>bubbleOverlay</code>](#dc.bubbleOverlay)
**mandatory**

Set up a data point on the overlay. The name of a data point should match a specific 'key' among
data groups generated using keyAccessor.  If a match is found (point name <-> data group key)
then a bubble will be generated at the position specified by the function. x and y
value specified here are relative to the underlying svg.

**Kind**: instance method of [<code>bubbleOverlay</code>](#dc.bubbleOverlay)  

| Param | Type |
| --- | --- |
| name | <code>String</code> | 
| x | <code>Number</code> | 
| y | <code>Number</code> | 

<a name="dc.rowChart"></a>

### dc.rowChart
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>capMixin</code>](#dc.capMixin), [<code>marginMixin</code>](#dc.marginMixin), [<code>colorMixin</code>](#dc.colorMixin), [<code>baseMixin</code>](#dc.baseMixin)  

* [.rowChart](#dc.rowChart)
    * [new rowChart(parent, [chartGroup])](#new_dc.rowChart_new)
    * [.x([scale])](#dc.rowChart+x) ⇒ <code>d3.scale</code> \| [<code>rowChart</code>](#dc.rowChart)
    * [.renderTitleLabel([renderTitleLabel])](#dc.rowChart+renderTitleLabel) ⇒ <code>Boolean</code> \| [<code>rowChart</code>](#dc.rowChart)
    * [.xAxis([xAxis])](#dc.rowChart+xAxis) ⇒ <code>d3.axis</code> \| [<code>rowChart</code>](#dc.rowChart)
    * [.fixedBarHeight([fixedBarHeight])](#dc.rowChart+fixedBarHeight) ⇒ <code>Boolean</code> \| <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
    * [.gap([gap])](#dc.rowChart+gap) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
    * [.elasticX([elasticX])](#dc.rowChart+elasticX) ⇒ <code>Boolean</code> \| [<code>rowChart</code>](#dc.rowChart)
    * [.labelOffsetX([labelOffsetX])](#dc.rowChart+labelOffsetX) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
    * [.labelOffsetY([labelOffsety])](#dc.rowChart+labelOffsetY) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
    * [.titleLabelOffsetX([titleLabelOffsetX])](#dc.rowChart+titleLabelOffsetX) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)

<a name="new_dc.rowChart_new"></a>

#### new rowChart(parent, [chartGroup])
Concrete row chart implementation.

Examples:
- [Nasdaq 100 Index](http://dc-js.github.com/dc.js/)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a row chart under #chart-container1 element using the default global chart group
var chart1 = dc.rowChart('#chart-container1');
// create a row chart under #chart-container2 element using chart group A
var chart2 = dc.rowChart('#chart-container2', 'chartGroupA');
```
<a name="dc.rowChart+x"></a>

#### rowChart.x([scale]) ⇒ <code>d3.scale</code> \| [<code>rowChart</code>](#dc.rowChart)
Gets or sets the x scale. The x scale can be any d3
[d3.scale](https://github.com/d3/d3-scale/blob/master/README.md).

**Kind**: instance method of [<code>rowChart</code>](#dc.rowChart)  
**See**: [d3.scale](https://github.com/d3/d3-scale/blob/master/README.md)  

| Param | Type |
| --- | --- |
| [scale] | <code>d3.scale</code> | 

<a name="dc.rowChart+renderTitleLabel"></a>

#### rowChart.renderTitleLabel([renderTitleLabel]) ⇒ <code>Boolean</code> \| [<code>rowChart</code>](#dc.rowChart)
Turn on/off Title label rendering (values) using SVG style of text-anchor 'end'.

**Kind**: instance method of [<code>rowChart</code>](#dc.rowChart)  

| Param | Type | Default |
| --- | --- | --- |
| [renderTitleLabel] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.rowChart+xAxis"></a>

#### rowChart.xAxis([xAxis]) ⇒ <code>d3.axis</code> \| [<code>rowChart</code>](#dc.rowChart)
Get or sets the x axis for the row chart instance.
See the [d3.axis](https://github.com/d3/d3-axis/blob/master/README.md)
documention for more information.

**Kind**: instance method of [<code>rowChart</code>](#dc.rowChart)  

| Param | Type |
| --- | --- |
| [xAxis] | <code>d3.axis</code> | 

**Example**  
```js
// customize x axis tick format
chart.xAxis().tickFormat(function (v) {return v + '%';});
// customize x axis tick values
chart.xAxis().tickValues([0, 100, 200, 300]);
// use a top-oriented axis. Note: position of the axis and grid lines will need to
// be set manually, see https://dc-js.github.io/dc.js/examples/row-top-axis.html
chart.xAxis(d3.axisTop())
```
<a name="dc.rowChart+fixedBarHeight"></a>

#### rowChart.fixedBarHeight([fixedBarHeight]) ⇒ <code>Boolean</code> \| <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
Get or set the fixed bar height. Default is [false] which will auto-scale bars.
For example, if you want to fix the height for a specific number of bars (useful in TopN charts)
you could fix height as follows (where count = total number of bars in your TopN and gap is
your vertical gap space).

**Kind**: instance method of [<code>rowChart</code>](#dc.rowChart)  

| Param | Type | Default |
| --- | --- | --- |
| [fixedBarHeight] | <code>Boolean</code> \| <code>Number</code> | <code>false</code> | 

**Example**  
```js
chart.fixedBarHeight( chartheight - (count + 1) * gap / count);
```
<a name="dc.rowChart+gap"></a>

#### rowChart.gap([gap]) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
Get or set the vertical gap space between rows on a particular row chart instance.

**Kind**: instance method of [<code>rowChart</code>](#dc.rowChart)  

| Param | Type | Default |
| --- | --- | --- |
| [gap] | <code>Number</code> | <code>5</code> | 

<a name="dc.rowChart+elasticX"></a>

#### rowChart.elasticX([elasticX]) ⇒ <code>Boolean</code> \| [<code>rowChart</code>](#dc.rowChart)
Get or set the elasticity on x axis. If this attribute is set to true, then the x axis will rescale to auto-fit the
data range when filtered.

**Kind**: instance method of [<code>rowChart</code>](#dc.rowChart)  

| Param | Type |
| --- | --- |
| [elasticX] | <code>Boolean</code> | 

<a name="dc.rowChart+labelOffsetX"></a>

#### rowChart.labelOffsetX([labelOffsetX]) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
Get or set the x offset (horizontal space to the top left corner of a row) for labels on a particular row chart.

**Kind**: instance method of [<code>rowChart</code>](#dc.rowChart)  

| Param | Type | Default |
| --- | --- | --- |
| [labelOffsetX] | <code>Number</code> | <code>10</code> | 

<a name="dc.rowChart+labelOffsetY"></a>

#### rowChart.labelOffsetY([labelOffsety]) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
Get or set the y offset (vertical space to the top left corner of a row) for labels on a particular row chart.

**Kind**: instance method of [<code>rowChart</code>](#dc.rowChart)  

| Param | Type | Default |
| --- | --- | --- |
| [labelOffsety] | <code>Number</code> | <code>15</code> | 

<a name="dc.rowChart+titleLabelOffsetX"></a>

#### rowChart.titleLabelOffsetX([titleLabelOffsetX]) ⇒ <code>Number</code> \| [<code>rowChart</code>](#dc.rowChart)
Get of set the x offset (horizontal space between right edge of row and right edge or text.

**Kind**: instance method of [<code>rowChart</code>](#dc.rowChart)  

| Param | Type | Default |
| --- | --- | --- |
| [titleLabelOffsetX] | <code>Number</code> | <code>2</code> | 

<a name="dc.legend"></a>

### dc.legend
**Kind**: static class of [<code>dc</code>](#dc)  

* [.legend](#dc.legend)
    * [new legend()](#new_dc.legend_new)
    * [.x([x])](#dc.legend+x) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
    * [.y([y])](#dc.legend+y) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
    * [.gap([gap])](#dc.legend+gap) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
    * [.itemHeight([itemHeight])](#dc.legend+itemHeight) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
    * [.horizontal([horizontal])](#dc.legend+horizontal) ⇒ <code>Boolean</code> \| [<code>legend</code>](#dc.legend)
    * [.legendWidth([legendWidth])](#dc.legend+legendWidth) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
    * [.itemWidth([itemWidth])](#dc.legend+itemWidth) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
    * [.autoItemWidth([autoItemWidth])](#dc.legend+autoItemWidth) ⇒ <code>Boolean</code> \| [<code>legend</code>](#dc.legend)
    * [.legendText([legendText])](#dc.legend+legendText) ⇒ <code>function</code> \| [<code>legend</code>](#dc.legend)
    * [.maxItems([maxItems])](#dc.legend+maxItems) ⇒ [<code>legend</code>](#dc.legend)

<a name="new_dc.legend_new"></a>

#### new legend()
Legend is a attachable widget that can be added to other dc charts to render horizontal legend
labels.

Examples:
- [Nasdaq 100 Index](http://dc-js.github.com/dc.js/)
- [Canadian City Crime Stats](http://dc-js.github.com/dc.js/crime/index.html)

**Example**  
```js
chart.legend(dc.legend().x(400).y(10).itemHeight(13).gap(5))
```
<a name="dc.legend+x"></a>

#### legend.x([x]) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
Set or get x coordinate for legend widget.

**Kind**: instance method of [<code>legend</code>](#dc.legend)  

| Param | Type | Default |
| --- | --- | --- |
| [x] | <code>Number</code> | <code>0</code> | 

<a name="dc.legend+y"></a>

#### legend.y([y]) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
Set or get y coordinate for legend widget.

**Kind**: instance method of [<code>legend</code>](#dc.legend)  

| Param | Type | Default |
| --- | --- | --- |
| [y] | <code>Number</code> | <code>0</code> | 

<a name="dc.legend+gap"></a>

#### legend.gap([gap]) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
Set or get gap between legend items.

**Kind**: instance method of [<code>legend</code>](#dc.legend)  

| Param | Type | Default |
| --- | --- | --- |
| [gap] | <code>Number</code> | <code>5</code> | 

<a name="dc.legend+itemHeight"></a>

#### legend.itemHeight([itemHeight]) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
Set or get legend item height.

**Kind**: instance method of [<code>legend</code>](#dc.legend)  

| Param | Type | Default |
| --- | --- | --- |
| [itemHeight] | <code>Number</code> | <code>12</code> | 

<a name="dc.legend+horizontal"></a>

#### legend.horizontal([horizontal]) ⇒ <code>Boolean</code> \| [<code>legend</code>](#dc.legend)
Position legend horizontally instead of vertically.

**Kind**: instance method of [<code>legend</code>](#dc.legend)  

| Param | Type | Default |
| --- | --- | --- |
| [horizontal] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.legend+legendWidth"></a>

#### legend.legendWidth([legendWidth]) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
Maximum width for horizontal legend.

**Kind**: instance method of [<code>legend</code>](#dc.legend)  

| Param | Type | Default |
| --- | --- | --- |
| [legendWidth] | <code>Number</code> | <code>500</code> | 

<a name="dc.legend+itemWidth"></a>

#### legend.itemWidth([itemWidth]) ⇒ <code>Number</code> \| [<code>legend</code>](#dc.legend)
Legend item width for horizontal legend.

**Kind**: instance method of [<code>legend</code>](#dc.legend)  

| Param | Type | Default |
| --- | --- | --- |
| [itemWidth] | <code>Number</code> | <code>70</code> | 

<a name="dc.legend+autoItemWidth"></a>

#### legend.autoItemWidth([autoItemWidth]) ⇒ <code>Boolean</code> \| [<code>legend</code>](#dc.legend)
Turn automatic width for legend items on or off. If true, [itemWidth](#dc.legend+itemWidth) is ignored.
This setting takes into account the [gap](#dc.legend+gap).

**Kind**: instance method of [<code>legend</code>](#dc.legend)  

| Param | Type | Default |
| --- | --- | --- |
| [autoItemWidth] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.legend+legendText"></a>

#### legend.legendText([legendText]) ⇒ <code>function</code> \| [<code>legend</code>](#dc.legend)
Set or get the legend text function. The legend widget uses this function to render the legend
text for each item. If no function is specified the legend widget will display the names
associated with each group.

**Kind**: instance method of [<code>legend</code>](#dc.legend)  

| Param | Type |
| --- | --- |
| [legendText] | <code>function</code> | 

**Example**  
```js
// default legendText
legend.legendText(dc.pluck('name'))

// create numbered legend items
chart.legend(dc.legend().legendText(function(d, i) { return i + '. ' + d.name; }))

// create legend displaying group counts
chart.legend(dc.legend().legendText(function(d) { return d.name + ': ' d.data; }))
```
<a name="dc.legend+maxItems"></a>

#### legend.maxItems([maxItems]) ⇒ [<code>legend</code>](#dc.legend)
Maximum number of legend items to display

**Kind**: instance method of [<code>legend</code>](#dc.legend)  

| Param | Type |
| --- | --- |
| [maxItems] | <code>Number</code> | 

<a name="dc.htmlLegend"></a>

### dc.htmlLegend
**Kind**: static class of [<code>dc</code>](#dc)  

* [.htmlLegend](#dc.htmlLegend)
    * [new htmlLegend()](#new_dc.htmlLegend_new)
    * [.container([container])](#dc.htmlLegend+container) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
    * [.legendItemClass([legendItemClass])](#dc.htmlLegend+legendItemClass) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
    * [.highlightSelected([highlightSelected])](#dc.htmlLegend+highlightSelected) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
    * [.horizontal([horizontal])](#dc.htmlLegend+horizontal) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
    * [.legendText([legendText])](#dc.htmlLegend+legendText) ⇒ <code>function</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
    * [.maxItems([maxItems])](#dc.htmlLegend+maxItems) ⇒ [<code>htmlLegend</code>](#dc.htmlLegend)

<a name="new_dc.htmlLegend_new"></a>

#### new htmlLegend()
htmlLegend is a attachable widget that can be added to other dc charts to render horizontal/vertical legend
labels.

**Example**  
```js
chart.legend(dc.htmlLegend().container(legendContainerElement).horizontal(false))
```
<a name="dc.htmlLegend+container"></a>

#### htmlLegend.container([container]) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
Set the container selector for the legend widget. Required.

**Kind**: instance method of [<code>htmlLegend</code>](#dc.htmlLegend)  

| Param | Type |
| --- | --- |
| [container] | <code>String</code> | 

<a name="dc.htmlLegend+legendItemClass"></a>

#### htmlLegend.legendItemClass([legendItemClass]) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
This can be optionally used to override class for legenditem and just use this class style.
This is helpful for overriding the style of a particular chart rather than overriding
the style for all charts.

Setting this will disable the highlighting of selected items also.

**Kind**: instance method of [<code>htmlLegend</code>](#dc.htmlLegend)  

| Param | Type |
| --- | --- |
| [legendItemClass] | <code>String</code> | 

<a name="dc.htmlLegend+highlightSelected"></a>

#### htmlLegend.highlightSelected([highlightSelected]) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
This can be optionally used to enable highlighting legends for the selections/filters for the
chart.

**Kind**: instance method of [<code>htmlLegend</code>](#dc.htmlLegend)  

| Param | Type |
| --- | --- |
| [highlightSelected] | <code>String</code> | 

<a name="dc.htmlLegend+horizontal"></a>

#### htmlLegend.horizontal([horizontal]) ⇒ <code>String</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
Display the legend horizontally instead of vertically

**Kind**: instance method of [<code>htmlLegend</code>](#dc.htmlLegend)  

| Param | Type |
| --- | --- |
| [horizontal] | <code>String</code> | 

<a name="dc.htmlLegend+legendText"></a>

#### htmlLegend.legendText([legendText]) ⇒ <code>function</code> \| [<code>htmlLegend</code>](#dc.htmlLegend)
Set or get the legend text function. The legend widget uses this function to render the legend
text for each item. If no function is specified the legend widget will display the names
associated with each group.

**Kind**: instance method of [<code>htmlLegend</code>](#dc.htmlLegend)  

| Param | Type |
| --- | --- |
| [legendText] | <code>function</code> | 

**Example**  
```js
// default legendText
legend.legendText(dc.pluck('name'))

// create numbered legend items
chart.legend(dc.htmlLegend().legendText(function(d, i) { return i + '. ' + d.name; }))

// create legend displaying group counts
chart.legend(dc.htmlLegend().legendText(function(d) { return d.name + ': ' d.data; }))
```
<a name="dc.htmlLegend+maxItems"></a>

#### htmlLegend.maxItems([maxItems]) ⇒ [<code>htmlLegend</code>](#dc.htmlLegend)
Maximum number of legend items to display

**Kind**: instance method of [<code>htmlLegend</code>](#dc.htmlLegend)  

| Param | Type |
| --- | --- |
| [maxItems] | <code>Number</code> | 

<a name="dc.scatterPlot"></a>

### dc.scatterPlot
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

* [.scatterPlot](#dc.scatterPlot)
    * [new scatterPlot(parent, [chartGroup])](#new_dc.scatterPlot_new)
    * [.emptyColor](#dc.scatterPlot+emptyColor) ⇒ <code>String</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.emptyOpacity](#dc.scatterPlot+emptyOpacity) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.nonemptyOpacity](#dc.scatterPlot+nonemptyOpacity) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.resetSvg()](#dc.scatterPlot+resetSvg) ⇒ <code>SVGElement</code>
    * [.useCanvas([useCanvas])](#dc.scatterPlot+useCanvas) ⇒ <code>Boolean</code> \| <code>d3.selection</code>
    * [.canvas([canvasElement])](#dc.scatterPlot+canvas) ⇒ <code>CanvasElement</code> \| <code>d3.selection</code>
    * [.context()](#dc.scatterPlot+context) ⇒ <code>CanvasContext</code>
    * [.existenceAccessor([accessor])](#dc.scatterPlot+existenceAccessor) ⇒ <code>function</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.symbol([type])](#dc.scatterPlot+symbol) ⇒ <code>function</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.customSymbol([customSymbol])](#dc.scatterPlot+customSymbol) ⇒ <code>String</code> \| <code>function</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.symbolSize([symbolSize])](#dc.scatterPlot+symbolSize) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.highlightedSize([highlightedSize])](#dc.scatterPlot+highlightedSize) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.excludedSize([excludedSize])](#dc.scatterPlot+excludedSize) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.excludedColor([excludedColor])](#dc.scatterPlot+excludedColor) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.excludedOpacity([excludedOpacity])](#dc.scatterPlot+excludedOpacity) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
    * [.emptySize([emptySize])](#dc.scatterPlot+emptySize) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)

<a name="new_dc.scatterPlot_new"></a>

#### new scatterPlot(parent, [chartGroup])
A scatter plot chart

Examples:
- [Scatter Chart](http://dc-js.github.io/dc.js/examples/scatter.html)
- [Multi-Scatter Chart](http://dc-js.github.io/dc.js/examples/multi-scatter.html)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a scatter plot under #chart-container1 element using the default global chart group
var chart1 = dc.scatterPlot('#chart-container1');
// create a scatter plot under #chart-container2 element using chart group A
var chart2 = dc.scatterPlot('#chart-container2', 'chartGroupA');
// create a sub-chart under a composite parent chart
var chart3 = dc.scatterPlot(compositeChart);
```
<a name="dc.scatterPlot+emptyColor"></a>

#### scatterPlot.emptyColor ⇒ <code>String</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Set or get color for symbols when the group is empty. If null, just use the
[colorMixin.colors](#dc.colorMixin+colors) color scale zero value.

**Kind**: instance property of [<code>scatterPlot</code>](#dc.scatterPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [emptyColor] | <code>String</code> | <code></code> | 

<a name="dc.scatterPlot+emptyOpacity"></a>

#### scatterPlot.emptyOpacity ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Set or get opacity for symbols when the group is empty.

**Kind**: instance property of [<code>scatterPlot</code>](#dc.scatterPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [emptyOpacity] | <code>Number</code> | <code>0</code> | 

<a name="dc.scatterPlot+nonemptyOpacity"></a>

#### scatterPlot.nonemptyOpacity ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Set or get opacity for symbols when the group is not empty.

**Kind**: instance property of [<code>scatterPlot</code>](#dc.scatterPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [nonemptyOpacity] | <code>Number</code> | <code>1</code> | 

<a name="dc.scatterPlot+resetSvg"></a>

#### scatterPlot.resetSvg() ⇒ <code>SVGElement</code>
Method that replaces original resetSvg and appropriately inserts canvas
element along with svg element and sets their CSS properties appropriately
so they are overlapped on top of each other.
Remove the chart's SVGElements from the dom and recreate the container SVGElement.

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  
**See**: [SVGElement](https://developer.mozilla.org/en-US/docs/Web/API/SVGElement)  
<a name="dc.scatterPlot+useCanvas"></a>

#### scatterPlot.useCanvas([useCanvas]) ⇒ <code>Boolean</code> \| <code>d3.selection</code>
Set or get whether to use canvas backend for plotting scatterPlot. Note that the
canvas backend does not currently support
[customSymbol](#dc.scatterPlot+customSymbol) or
[symbol](#dc.scatterPlot+symbol) methods and is limited to always plotting
with filled circles. Symbols are drawn with
[symbolSize](#dc.scatterPlot+symbolSize) radius. By default, the SVG backend
is used when `useCanvas` is set to `false`.

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [useCanvas] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.scatterPlot+canvas"></a>

#### scatterPlot.canvas([canvasElement]) ⇒ <code>CanvasElement</code> \| <code>d3.selection</code>
Set or get canvas element. You should usually only ever use the get method as
dc.js will handle canvas element generation.  Provides valid canvas only when
[useCanvas](#dc.scatterPlot+useCanvas) is set to `true`

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  

| Param | Type |
| --- | --- |
| [canvasElement] | <code>CanvasElement</code> \| <code>d3.selection</code> | 

<a name="dc.scatterPlot+context"></a>

#### scatterPlot.context() ⇒ <code>CanvasContext</code>
Get canvas 2D context. Provides valid context only when
[useCanvas](#dc.scatterPlot+useCanvas) is set to `true`

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  
<a name="dc.scatterPlot+existenceAccessor"></a>

#### scatterPlot.existenceAccessor([accessor]) ⇒ <code>function</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Get or set the existence accessor.  If a point exists, it is drawn with
[symbolSize](#dc.scatterPlot+symbolSize) radius and
opacity 1; if it does not exist, it is drawn with
[emptySize](#dc.scatterPlot+emptySize) radius and opacity 0. By default,
the existence accessor checks if the reduced value is truthy.

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  
**See**

- [symbolSize](#dc.scatterPlot+symbolSize)
- [emptySize](#dc.scatterPlot+emptySize)


| Param | Type |
| --- | --- |
| [accessor] | <code>function</code> | 

**Example**  
```js
// default accessor
chart.existenceAccessor(function (d) { return d.value; });
```
<a name="dc.scatterPlot+symbol"></a>

#### scatterPlot.symbol([type]) ⇒ <code>function</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Get or set the symbol type used for each point. By default the symbol is a circle (d3.symbolCircle).
Type can be a constant or an accessor.

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  
**See**: [symbol.type](https://github.com/d3/d3-shape/blob/master/README.md#symbol_type)  

| Param | Type | Default |
| --- | --- | --- |
| [type] | <code>function</code> | <code>d3.symbolCircle</code> | 

**Example**  
```js
// Circle type
chart.symbol(d3.symbolCircle);
// Square type
chart.symbol(d3.symbolSquare);
```
<a name="dc.scatterPlot+customSymbol"></a>

#### scatterPlot.customSymbol([customSymbol]) ⇒ <code>String</code> \| <code>function</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Get or set the symbol generator. By default `dc.scatterPlot` will use
[d3.symbol()](https://github.com/d3/d3-shape/blob/master/README.md#symbol)
to generate symbols. `dc.scatterPlot` will set the
[symbol size accessor](https://github.com/d3/d3-shape/blob/master/README.md#symbol_size)
on the symbol generator.

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  
**See**

- [d3.symbol](https://github.com/d3/d3-shape/blob/master/README.md#symbol)
- [Create additional D3.js symbols](https://stackoverflow.com/questions/25332120/create-additional-d3-js-symbols)


| Param | Type | Default |
| --- | --- | --- |
| [customSymbol] | <code>String</code> \| <code>function</code> | <code>d3.symbol()</code> | 

<a name="dc.scatterPlot+symbolSize"></a>

#### scatterPlot.symbolSize([symbolSize]) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Set or get radius for symbols.

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  
**See**: [d3.symbol.size](https://github.com/d3/d3-shape/blob/master/README.md#symbol_size)  

| Param | Type | Default |
| --- | --- | --- |
| [symbolSize] | <code>Number</code> | <code>3</code> | 

<a name="dc.scatterPlot+highlightedSize"></a>

#### scatterPlot.highlightedSize([highlightedSize]) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Set or get radius for highlighted symbols.

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  
**See**: [d3.symbol.size](https://github.com/d3/d3-shape/blob/master/README.md#symbol_size)  

| Param | Type | Default |
| --- | --- | --- |
| [highlightedSize] | <code>Number</code> | <code>5</code> | 

<a name="dc.scatterPlot+excludedSize"></a>

#### scatterPlot.excludedSize([excludedSize]) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Set or get size for symbols excluded from this chart's filter. If null, no
special size is applied for symbols based on their filter status.

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  
**See**: [d3.symbol.size](https://github.com/d3/d3-shape/blob/master/README.md#symbol_size)  

| Param | Type | Default |
| --- | --- | --- |
| [excludedSize] | <code>Number</code> | <code></code> | 

<a name="dc.scatterPlot+excludedColor"></a>

#### scatterPlot.excludedColor([excludedColor]) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Set or get color for symbols excluded from this chart's filter. If null, no
special color is applied for symbols based on their filter status.

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [excludedColor] | <code>Number</code> | <code></code> | 

<a name="dc.scatterPlot+excludedOpacity"></a>

#### scatterPlot.excludedOpacity([excludedOpacity]) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Set or get opacity for symbols excluded from this chart's filter.

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [excludedOpacity] | <code>Number</code> | <code>1.0</code> | 

<a name="dc.scatterPlot+emptySize"></a>

#### scatterPlot.emptySize([emptySize]) ⇒ <code>Number</code> \| [<code>scatterPlot</code>](#dc.scatterPlot)
Set or get radius for symbols when the group is empty.

**Kind**: instance method of [<code>scatterPlot</code>](#dc.scatterPlot)  
**See**: [d3.symbol.size](https://github.com/d3/d3-shape/blob/master/README.md#symbol_size)  

| Param | Type | Default |
| --- | --- | --- |
| [emptySize] | <code>Number</code> | <code>0</code> | 

<a name="dc.numberDisplay"></a>

### dc.numberDisplay
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>baseMixin</code>](#dc.baseMixin)  

* [.numberDisplay](#dc.numberDisplay)
    * [new numberDisplay(parent, [chartGroup])](#new_dc.numberDisplay_new)
    * [.html([html])](#dc.numberDisplay+html) ⇒ <code>Object</code> \| [<code>numberDisplay</code>](#dc.numberDisplay)
    * [.value()](#dc.numberDisplay+value) ⇒ <code>Number</code>
    * [.formatNumber([formatter])](#dc.numberDisplay+formatNumber) ⇒ <code>function</code> \| [<code>numberDisplay</code>](#dc.numberDisplay)

<a name="new_dc.numberDisplay_new"></a>

#### new numberDisplay(parent, [chartGroup])
A display of a single numeric value.

Unlike other charts, you do not need to set a dimension. Instead a group object must be provided and
a valueAccessor that returns a single value.

If the group is a [groupAll](https://github.com/crossfilter/crossfilter/wiki/API-Reference#crossfilter_groupAll)
then its `.value()` will be displayed. This is the recommended usage.

However, if it is given an ordinary group, the `numberDisplay` will show the last bin's value, after
sorting with the [ordering](https://dc-js.github.io/dc.js/docs/html/dc.baseMixin.html#ordering__anchor)
function. `numberDisplay` defaults the `ordering` function to sorting by value, so this will display
the largest value if the values are numeric.


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a number display under #chart-container1 element using the default global chart group
var display1 = dc.numberDisplay('#chart-container1');
```
<a name="dc.numberDisplay+html"></a>

#### numberDisplay.html([html]) ⇒ <code>Object</code> \| [<code>numberDisplay</code>](#dc.numberDisplay)
Gets or sets an optional object specifying HTML templates to use depending on the number
displayed.  The text `%number` will be replaced with the current value.
- one: HTML template to use if the number is 1
- zero: HTML template to use if the number is 0
- some: HTML template to use otherwise

**Kind**: instance method of [<code>numberDisplay</code>](#dc.numberDisplay)  

| Param | Type | Default |
| --- | --- | --- |
| [html] | <code>Object</code> | <code>{one: &#x27;&#x27;, some: &#x27;&#x27;, none: &#x27;&#x27;}</code> | 

**Example**  
```js
numberWidget.html({
     one:'%number record',
     some:'%number records',
     none:'no records'})
```
<a name="dc.numberDisplay+value"></a>

#### numberDisplay.value() ⇒ <code>Number</code>
Calculate and return the underlying value of the display.

**Kind**: instance method of [<code>numberDisplay</code>](#dc.numberDisplay)  
<a name="dc.numberDisplay+formatNumber"></a>

#### numberDisplay.formatNumber([formatter]) ⇒ <code>function</code> \| [<code>numberDisplay</code>](#dc.numberDisplay)
Get or set a function to format the value for the display.

**Kind**: instance method of [<code>numberDisplay</code>](#dc.numberDisplay)  
**See**: [d3.format](https://github.com/d3/d3-format/blob/master/README.md#format)  

| Param | Type | Default |
| --- | --- | --- |
| [formatter] | <code>function</code> | <code>d3.format(&#x27;.2s&#x27;)</code> | 

<a name="dc.heatMap"></a>

### dc.heatMap
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>colorMixin</code>](#dc.colorMixin), [<code>marginMixin</code>](#dc.marginMixin), [<code>baseMixin</code>](#dc.baseMixin)  

* [.heatMap](#dc.heatMap)
    * [new heatMap(parent, [chartGroup])](#new_dc.heatMap_new)
    * [.colsLabel([labelFunction])](#dc.heatMap+colsLabel) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
    * [.rowsLabel([labelFunction])](#dc.heatMap+rowsLabel) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
    * [.rows([rows])](#dc.heatMap+rows) ⇒ <code>Array.&lt;(String\|Number)&gt;</code> \| [<code>heatMap</code>](#dc.heatMap)
    * [.rowOrdering([rowOrdering])](#dc.heatMap+rowOrdering) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
    * [.cols([cols])](#dc.heatMap+cols) ⇒ <code>Array.&lt;(String\|Number)&gt;</code> \| [<code>heatMap</code>](#dc.heatMap)
    * [.colOrdering([colOrdering])](#dc.heatMap+colOrdering) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
    * [.boxOnClick([handler])](#dc.heatMap+boxOnClick) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
    * [.xAxisOnClick([handler])](#dc.heatMap+xAxisOnClick) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
    * [.yAxisOnClick([handler])](#dc.heatMap+yAxisOnClick) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
    * [.xBorderRadius([xBorderRadius])](#dc.heatMap+xBorderRadius) ⇒ <code>Number</code> \| [<code>heatMap</code>](#dc.heatMap)
    * [.yBorderRadius([yBorderRadius])](#dc.heatMap+yBorderRadius) ⇒ <code>Number</code> \| [<code>heatMap</code>](#dc.heatMap)

<a name="new_dc.heatMap_new"></a>

#### new heatMap(parent, [chartGroup])
A heat map is matrix that represents the values of two dimensions of data using colors.


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a heat map under #chart-container1 element using the default global chart group
var heatMap1 = dc.heatMap('#chart-container1');
// create a heat map under #chart-container2 element using chart group A
var heatMap2 = dc.heatMap('#chart-container2', 'chartGroupA');
```
<a name="dc.heatMap+colsLabel"></a>

#### heatMap.colsLabel([labelFunction]) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
Set or get the column label function. The chart class uses this function to render
column labels on the X axis. It is passed the column name.

**Kind**: instance method of [<code>heatMap</code>](#dc.heatMap)  

| Param | Type | Default |
| --- | --- | --- |
| [labelFunction] | <code>function</code> | <code>function(d) { return d; }</code> | 

**Example**  
```js
// the default label function just returns the name
chart.colsLabel(function(d) { return d; });
```
<a name="dc.heatMap+rowsLabel"></a>

#### heatMap.rowsLabel([labelFunction]) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
Set or get the row label function. The chart class uses this function to render
row labels on the Y axis. It is passed the row name.

**Kind**: instance method of [<code>heatMap</code>](#dc.heatMap)  

| Param | Type | Default |
| --- | --- | --- |
| [labelFunction] | <code>function</code> | <code>function(d) { return d; }</code> | 

**Example**  
```js
// the default label function just returns the name
chart.rowsLabel(function(d) { return d; });
```
<a name="dc.heatMap+rows"></a>

#### heatMap.rows([rows]) ⇒ <code>Array.&lt;(String\|Number)&gt;</code> \| [<code>heatMap</code>](#dc.heatMap)
Gets or sets the values used to create the rows of the heatmap, as an array. By default, all
the values will be fetched from the data using the value accessor.

**Kind**: instance method of [<code>heatMap</code>](#dc.heatMap)  

| Param | Type |
| --- | --- |
| [rows] | <code>Array.&lt;(String\|Number)&gt;</code> | 

<a name="dc.heatMap+rowOrdering"></a>

#### heatMap.rowOrdering([rowOrdering]) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
Get or set a comparator to order the rows.
Default is [d3.ascending](https://github.com/d3/d3-array#ascending).

**Kind**: instance method of [<code>heatMap</code>](#dc.heatMap)  

| Param | Type |
| --- | --- |
| [rowOrdering] | <code>function</code> | 

<a name="dc.heatMap+cols"></a>

#### heatMap.cols([cols]) ⇒ <code>Array.&lt;(String\|Number)&gt;</code> \| [<code>heatMap</code>](#dc.heatMap)
Gets or sets the keys used to create the columns of the heatmap, as an array. By default, all
the values will be fetched from the data using the key accessor.

**Kind**: instance method of [<code>heatMap</code>](#dc.heatMap)  

| Param | Type |
| --- | --- |
| [cols] | <code>Array.&lt;(String\|Number)&gt;</code> | 

<a name="dc.heatMap+colOrdering"></a>

#### heatMap.colOrdering([colOrdering]) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
Get or set a comparator to order the columns.
Default is  [d3.ascending](https://github.com/d3/d3-array#ascending).

**Kind**: instance method of [<code>heatMap</code>](#dc.heatMap)  

| Param | Type |
| --- | --- |
| [colOrdering] | <code>function</code> | 

<a name="dc.heatMap+boxOnClick"></a>

#### heatMap.boxOnClick([handler]) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
Gets or sets the handler that fires when an individual cell is clicked in the heatmap.
By default, filtering of the cell will be toggled.

**Kind**: instance method of [<code>heatMap</code>](#dc.heatMap)  

| Param | Type |
| --- | --- |
| [handler] | <code>function</code> | 

**Example**  
```js
// default box on click handler
chart.boxOnClick(function (d) {
    var filter = d.key;
    dc.events.trigger(function () {
        _chart.filter(filter);
        _chart.redrawGroup();
    });
});
```
<a name="dc.heatMap+xAxisOnClick"></a>

#### heatMap.xAxisOnClick([handler]) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
Gets or sets the handler that fires when a column tick is clicked in the x axis.
By default, if any cells in the column are unselected, the whole column will be selected,
otherwise the whole column will be unselected.

**Kind**: instance method of [<code>heatMap</code>](#dc.heatMap)  

| Param | Type |
| --- | --- |
| [handler] | <code>function</code> | 

<a name="dc.heatMap+yAxisOnClick"></a>

#### heatMap.yAxisOnClick([handler]) ⇒ <code>function</code> \| [<code>heatMap</code>](#dc.heatMap)
Gets or sets the handler that fires when a row tick is clicked in the y axis.
By default, if any cells in the row are unselected, the whole row will be selected,
otherwise the whole row will be unselected.

**Kind**: instance method of [<code>heatMap</code>](#dc.heatMap)  

| Param | Type |
| --- | --- |
| [handler] | <code>function</code> | 

<a name="dc.heatMap+xBorderRadius"></a>

#### heatMap.xBorderRadius([xBorderRadius]) ⇒ <code>Number</code> \| [<code>heatMap</code>](#dc.heatMap)
Gets or sets the X border radius.  Set to 0 to get full rectangles.

**Kind**: instance method of [<code>heatMap</code>](#dc.heatMap)  

| Param | Type | Default |
| --- | --- | --- |
| [xBorderRadius] | <code>Number</code> | <code>6.75</code> | 

<a name="dc.heatMap+yBorderRadius"></a>

#### heatMap.yBorderRadius([yBorderRadius]) ⇒ <code>Number</code> \| [<code>heatMap</code>](#dc.heatMap)
Gets or sets the Y border radius.  Set to 0 to get full rectangles.

**Kind**: instance method of [<code>heatMap</code>](#dc.heatMap)  

| Param | Type | Default |
| --- | --- | --- |
| [yBorderRadius] | <code>Number</code> | <code>6.75</code> | 

<a name="dc.boxPlot"></a>

### dc.boxPlot
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

* [.boxPlot](#dc.boxPlot)
    * [new boxPlot(parent, [chartGroup])](#new_dc.boxPlot_new)
    * [.boxPadding([padding])](#dc.boxPlot+boxPadding) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
    * [.outerPadding([padding])](#dc.boxPlot+outerPadding) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
    * [.boxWidth([boxWidth])](#dc.boxPlot+boxWidth) ⇒ <code>Number</code> \| <code>function</code> \| [<code>boxPlot</code>](#dc.boxPlot)
    * [.tickFormat([tickFormat])](#dc.boxPlot+tickFormat) ⇒ <code>Number</code> \| <code>function</code> \| [<code>boxPlot</code>](#dc.boxPlot)
    * [.yRangePadding([yRangePadding])](#dc.boxPlot+yRangePadding) ⇒ <code>Number</code> \| <code>function</code> \| [<code>boxPlot</code>](#dc.boxPlot)
    * [.renderDataPoints([show])](#dc.boxPlot+renderDataPoints) ⇒ <code>Boolean</code> \| [<code>boxPlot</code>](#dc.boxPlot)
    * [.dataOpacity([opacity])](#dc.boxPlot+dataOpacity) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
    * [.dataWidthPortion([percentage])](#dc.boxPlot+dataWidthPortion) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
    * [.showOutliers([show])](#dc.boxPlot+showOutliers) ⇒ <code>Boolean</code> \| [<code>boxPlot</code>](#dc.boxPlot)
    * [.boldOutlier([show])](#dc.boxPlot+boldOutlier) ⇒ <code>Boolean</code> \| [<code>boxPlot</code>](#dc.boxPlot)

<a name="new_dc.boxPlot_new"></a>

#### new boxPlot(parent, [chartGroup])
A box plot is a chart that depicts numerical data via their quartile ranges.

Examples:
- [Boxplot Basic example](http://dc-js.github.io/dc.js/examples/boxplot-basic.html)
- [Boxplot Enhanced example](http://dc-js.github.io/dc.js/examples/boxplot-enhanced.html)
- [Boxplot Render Data example](http://dc-js.github.io/dc.js/examples/boxplot-render-data.html)
- [Boxplot time example](http://dc-js.github.io/dc.js/examples/boxplot-time.html)


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
// create a box plot under #chart-container1 element using the default global chart group
var boxPlot1 = dc.boxPlot('#chart-container1');
// create a box plot under #chart-container2 element using chart group A
var boxPlot2 = dc.boxPlot('#chart-container2', 'chartGroupA');
```
<a name="dc.boxPlot+boxPadding"></a>

#### boxPlot.boxPadding([padding]) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
Get or set the spacing between boxes as a fraction of box size. Valid values are within 0-1.
See the [d3 docs](https://github.com/d3/d3-scale/blob/master/README.md#scaleBand)
for a visual description of how the padding is applied.

**Kind**: instance method of [<code>boxPlot</code>](#dc.boxPlot)  
**See**: [d3.scaleBand](https://github.com/d3/d3-scale/blob/master/README.md#scaleBand)  

| Param | Type | Default |
| --- | --- | --- |
| [padding] | <code>Number</code> | <code>0.8</code> | 

<a name="dc.boxPlot+outerPadding"></a>

#### boxPlot.outerPadding([padding]) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
Get or set the outer padding on an ordinal box chart. This setting has no effect on non-ordinal charts
or on charts with a custom [.boxWidth](#dc.boxPlot+boxWidth). Will pad the width by
`padding * barWidth` on each side of the chart.

**Kind**: instance method of [<code>boxPlot</code>](#dc.boxPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [padding] | <code>Number</code> | <code>0.5</code> | 

<a name="dc.boxPlot+boxWidth"></a>

#### boxPlot.boxWidth([boxWidth]) ⇒ <code>Number</code> \| <code>function</code> \| [<code>boxPlot</code>](#dc.boxPlot)
Get or set the numerical width of the boxplot box. The width may also be a function taking as
parameters the chart width excluding the right and left margins, as well as the number of x
units.

**Kind**: instance method of [<code>boxPlot</code>](#dc.boxPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [boxWidth] | <code>Number</code> \| <code>function</code> | <code>0.5</code> | 

**Example**  
```js
// Using numerical parameter
chart.boxWidth(10);
// Using function
chart.boxWidth((innerChartWidth, xUnits) { ... });
```
<a name="dc.boxPlot+tickFormat"></a>

#### boxPlot.tickFormat([tickFormat]) ⇒ <code>Number</code> \| <code>function</code> \| [<code>boxPlot</code>](#dc.boxPlot)
Get or set the numerical format of the boxplot median, whiskers and quartile labels. Defaults
to integer formatting.

**Kind**: instance method of [<code>boxPlot</code>](#dc.boxPlot)  

| Param | Type |
| --- | --- |
| [tickFormat] | <code>function</code> | 

**Example**  
```js
// format ticks to 2 decimal places
chart.tickFormat(d3.format('.2f'));
```
<a name="dc.boxPlot+yRangePadding"></a>

#### boxPlot.yRangePadding([yRangePadding]) ⇒ <code>Number</code> \| <code>function</code> \| [<code>boxPlot</code>](#dc.boxPlot)
Get or set the amount of padding to add, in pixel coordinates, to the top and
bottom of the chart to accommodate box/whisker labels.

**Kind**: instance method of [<code>boxPlot</code>](#dc.boxPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [yRangePadding] | <code>function</code> | <code>8</code> | 

**Example**  
```js
// allow more space for a bigger whisker font
chart.yRangePadding(12);
```
<a name="dc.boxPlot+renderDataPoints"></a>

#### boxPlot.renderDataPoints([show]) ⇒ <code>Boolean</code> \| [<code>boxPlot</code>](#dc.boxPlot)
Get or set whether individual data points will be rendered.

**Kind**: instance method of [<code>boxPlot</code>](#dc.boxPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [show] | <code>Boolean</code> | <code>false</code> | 

**Example**  
```js
// Enable rendering of individual data points
chart.renderDataPoints(true);
```
<a name="dc.boxPlot+dataOpacity"></a>

#### boxPlot.dataOpacity([opacity]) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
Get or set the opacity when rendering data.

**Kind**: instance method of [<code>boxPlot</code>](#dc.boxPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [opacity] | <code>Number</code> | <code>0.3</code> | 

**Example**  
```js
// If individual data points are rendered increase the opacity.
chart.dataOpacity(0.7);
```
<a name="dc.boxPlot+dataWidthPortion"></a>

#### boxPlot.dataWidthPortion([percentage]) ⇒ <code>Number</code> \| [<code>boxPlot</code>](#dc.boxPlot)
Get or set the portion of the width of the box to show data points.

**Kind**: instance method of [<code>boxPlot</code>](#dc.boxPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [percentage] | <code>Number</code> | <code>0.8</code> | 

**Example**  
```js
// If individual data points are rendered increase the data box.
chart.dataWidthPortion(0.9);
```
<a name="dc.boxPlot+showOutliers"></a>

#### boxPlot.showOutliers([show]) ⇒ <code>Boolean</code> \| [<code>boxPlot</code>](#dc.boxPlot)
Get or set whether outliers will be rendered.

**Kind**: instance method of [<code>boxPlot</code>](#dc.boxPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [show] | <code>Boolean</code> | <code>true</code> | 

**Example**  
```js
// Disable rendering of outliers
chart.showOutliers(false);
```
<a name="dc.boxPlot+boldOutlier"></a>

#### boxPlot.boldOutlier([show]) ⇒ <code>Boolean</code> \| [<code>boxPlot</code>](#dc.boxPlot)
Get or set whether outliers will be drawn bold.

**Kind**: instance method of [<code>boxPlot</code>](#dc.boxPlot)  

| Param | Type | Default |
| --- | --- | --- |
| [show] | <code>Boolean</code> | <code>false</code> | 

**Example**  
```js
// If outliers are rendered display as bold
chart.boldOutlier(true);
```
<a name="dc.selectMenu"></a>

### dc.selectMenu
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>baseMixin</code>](#dc.baseMixin)  

* [.selectMenu](#dc.selectMenu)
    * [new selectMenu(parent, [chartGroup])](#new_dc.selectMenu_new)
    * [.order([order])](#dc.selectMenu+order) ⇒ <code>function</code> \| [<code>selectMenu</code>](#dc.selectMenu)
    * [.promptText([promptText])](#dc.selectMenu+promptText) ⇒ <code>String</code> \| [<code>selectMenu</code>](#dc.selectMenu)
    * [.filterDisplayed([filterDisplayed])](#dc.selectMenu+filterDisplayed) ⇒ <code>function</code> \| [<code>selectMenu</code>](#dc.selectMenu)
    * [.multiple([multiple])](#dc.selectMenu+multiple) ⇒ <code>boolean</code> \| [<code>selectMenu</code>](#dc.selectMenu)
    * [.promptValue([promptValue])](#dc.selectMenu+promptValue) ⇒ <code>\*</code> \| [<code>selectMenu</code>](#dc.selectMenu)
    * [.numberItems([numberVisible])](#dc.selectMenu+numberItems) ⇒ <code>number</code> \| [<code>selectMenu</code>](#dc.selectMenu)

<a name="new_dc.selectMenu_new"></a>

#### new selectMenu(parent, [chartGroup])
The select menu is a simple widget designed to filter a dimension by selecting an option from
an HTML `<select/>` menu. The menu can be optionally turned into a multiselect.


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> \| [<code>compositeChart</code>](#dc.compositeChart) | Any valid [d3 single selector](https://github.com/mbostock/d3/wiki/Selections#selecting-elements) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this widget should be placed in. Interaction with the widget will only trigger events and redraws within its group. |

**Example**  
```js
// create a select menu under #select-container using the default global chart group
var select = dc.selectMenu('#select-container')
               .dimension(states)
               .group(stateGroup);
// the option text can be set via the title() function
// by default the option text is '`key`: `value`'
select.title(function (d){
    return 'STATE: ' + d.key;
})
```
<a name="dc.selectMenu+order"></a>

#### selectMenu.order([order]) ⇒ <code>function</code> \| [<code>selectMenu</code>](#dc.selectMenu)
Get or set the function that controls the ordering of option tags in the
select menu. By default options are ordered by the group key in ascending
order.

**Kind**: instance method of [<code>selectMenu</code>](#dc.selectMenu)  

| Param | Type |
| --- | --- |
| [order] | <code>function</code> | 

**Example**  
```js
// order by the group's value
chart.order(function (a,b) {
    return a.value > b.value ? 1 : b.value > a.value ? -1 : 0;
});
```
<a name="dc.selectMenu+promptText"></a>

#### selectMenu.promptText([promptText]) ⇒ <code>String</code> \| [<code>selectMenu</code>](#dc.selectMenu)
Get or set the text displayed in the options used to prompt selection.

**Kind**: instance method of [<code>selectMenu</code>](#dc.selectMenu)  

| Param | Type | Default |
| --- | --- | --- |
| [promptText] | <code>String</code> | <code>&#x27;Select all&#x27;</code> | 

**Example**  
```js
chart.promptText('All states');
```
<a name="dc.selectMenu+filterDisplayed"></a>

#### selectMenu.filterDisplayed([filterDisplayed]) ⇒ <code>function</code> \| [<code>selectMenu</code>](#dc.selectMenu)
Get or set the function that filters option tags prior to display. By default options
with a value of < 1 are not displayed.

**Kind**: instance method of [<code>selectMenu</code>](#dc.selectMenu)  

| Param | Type |
| --- | --- |
| [filterDisplayed] | <code>function</code> | 

**Example**  
```js
// display all options override the `filterDisplayed` function:
chart.filterDisplayed(function () {
    return true;
});
```
<a name="dc.selectMenu+multiple"></a>

#### selectMenu.multiple([multiple]) ⇒ <code>boolean</code> \| [<code>selectMenu</code>](#dc.selectMenu)
Controls the type of select menu. Setting it to true converts the underlying
HTML tag into a multiple select.

**Kind**: instance method of [<code>selectMenu</code>](#dc.selectMenu)  

| Param | Type | Default |
| --- | --- | --- |
| [multiple] | <code>boolean</code> | <code>false</code> | 

**Example**  
```js
chart.multiple(true);
```
<a name="dc.selectMenu+promptValue"></a>

#### selectMenu.promptValue([promptValue]) ⇒ <code>\*</code> \| [<code>selectMenu</code>](#dc.selectMenu)
Controls the default value to be used for
[dimension.filter](https://github.com/crossfilter/crossfilter/wiki/API-Reference#dimension_filter)
when only the prompt value is selected. If `null` (the default), no filtering will occur when
just the prompt is selected.

**Kind**: instance method of [<code>selectMenu</code>](#dc.selectMenu)  

| Param | Type | Default |
| --- | --- | --- |
| [promptValue] | <code>\*</code> | <code></code> | 

<a name="dc.selectMenu+numberItems"></a>

#### selectMenu.numberItems([numberVisible]) ⇒ <code>number</code> \| [<code>selectMenu</code>](#dc.selectMenu)
Controls the number of items to show in the select menu, when `.multiple()` is true. This
controls the [`size` attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select#Attributes) of
the `select` element. If `null` (the default), uses the browser's default height.

**Kind**: instance method of [<code>selectMenu</code>](#dc.selectMenu)  

| Param | Type | Default |
| --- | --- | --- |
| [numberVisible] | <code>number</code> | <code></code> | 

**Example**  
```js
chart.numberVisible(10);
```
<a name="dc.textFilterWidget"></a>

### dc.textFilterWidget
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>baseMixin</code>](#dc.baseMixin)  

* [.textFilterWidget](#dc.textFilterWidget)
    * [new textFilterWidget(parent, [chartGroup])](#new_dc.textFilterWidget_new)
    * [.normalize](#dc.textFilterWidget+normalize) ⇒ [<code>textFilterWidget</code>](#dc.textFilterWidget) \| <code>function</code>
    * [.placeHolder](#dc.textFilterWidget+placeHolder) ⇒ [<code>textFilterWidget</code>](#dc.textFilterWidget) \| <code>string</code>
    * [.filterFunctionFactory](#dc.textFilterWidget+filterFunctionFactory) ⇒ [<code>textFilterWidget</code>](#dc.textFilterWidget) \| <code>function</code>

<a name="new_dc.textFilterWidget_new"></a>

#### new textFilterWidget(parent, [chartGroup])
Text Filter Widget

The text filter widget is a simple widget designed to display an input field allowing to filter
data that matches the text typed.
As opposed to the other charts, this doesn't display any result and doesn't update its display,
it's just to input an filter other charts.


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> \| [<code>compositeChart</code>](#dc.compositeChart) | Any valid [d3 single selector](https://github.com/d3/d3-selection/blob/master/README.md#select) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this chart instance should be placed in. Interaction with a chart will only trigger events and redraws within the chart's group. |

**Example**  
```js
var data = [{"firstName":"John","lastName":"Coltrane"}{"firstName":"Miles",lastName:"Davis"}]
var ndx = crossfilter(data);
var dimension = ndx.dimension(function(d) {
    return d.lastName.toLowerCase() + ' ' + d.firstName.toLowerCase();
});

dc.textFilterWidget('#search')
    .dimension(dimension);
    // you don't need the group() function
```
<a name="dc.textFilterWidget+normalize"></a>

#### textFilterWidget.normalize ⇒ [<code>textFilterWidget</code>](#dc.textFilterWidget) \| <code>function</code>
This function will be called on values before calling the filter function.

**Kind**: instance property of [<code>textFilterWidget</code>](#dc.textFilterWidget)  

| Param | Type |
| --- | --- |
| [normalize] | <code>function</code> | 

**Example**  
```js
// This is the default
chart.normalize(function (s) {
  return s.toLowerCase();
});
```
<a name="dc.textFilterWidget+placeHolder"></a>

#### textFilterWidget.placeHolder ⇒ [<code>textFilterWidget</code>](#dc.textFilterWidget) \| <code>string</code>
Placeholder text in the search box.

**Kind**: instance property of [<code>textFilterWidget</code>](#dc.textFilterWidget)  

| Param | Type | Default |
| --- | --- | --- |
| [placeHolder] | <code>function</code> | <code>&#x27;search&#x27;</code> | 

**Example**  
```js
// This is the default
chart.placeHolder('type to filter');
```
<a name="dc.textFilterWidget+filterFunctionFactory"></a>

#### textFilterWidget.filterFunctionFactory ⇒ [<code>textFilterWidget</code>](#dc.textFilterWidget) \| <code>function</code>
This function will be called with the search text, it needs to return a function that will be used to
filter the data. The default function checks presence of the search text.

**Kind**: instance property of [<code>textFilterWidget</code>](#dc.textFilterWidget)  

| Param | Type |
| --- | --- |
| [filterFunctionFactory] | <code>function</code> | 

**Example**  
```js
// This is the default
function (query) {
    query = _normalize(query);
    return function (d) {
        return _normalize(d).indexOf(query) !== -1;
    };
};
```
<a name="dc.cboxMenu"></a>

### dc.cboxMenu
**Kind**: static class of [<code>dc</code>](#dc)  
**Mixes**: [<code>baseMixin</code>](#dc.baseMixin)  

* [.cboxMenu](#dc.cboxMenu)
    * [new cboxMenu(parent, [chartGroup])](#new_dc.cboxMenu_new)
    * [.order([order])](#dc.cboxMenu+order) ⇒ <code>function</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
    * [.promptText([promptText])](#dc.cboxMenu+promptText) ⇒ <code>String</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
    * [.filterDisplayed([filterDisplayed])](#dc.cboxMenu+filterDisplayed) ⇒ <code>function</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
    * [.multiple([multiple])](#dc.cboxMenu+multiple) ⇒ <code>Boolean</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
    * [.promptValue([promptValue])](#dc.cboxMenu+promptValue) ⇒ <code>\*</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)

<a name="new_dc.cboxMenu_new"></a>

#### new cboxMenu(parent, [chartGroup])
The cboxMenu is a simple widget designed to filter a dimension by
selecting option(s) from a set of HTML `<input />` elements. The menu can be
made into a set of radio buttons (single select) or checkboxes (multiple).


| Param | Type | Description |
| --- | --- | --- |
| parent | <code>String</code> \| <code>node</code> \| <code>d3.selection</code> \| [<code>compositeChart</code>](#dc.compositeChart) | Any valid [d3 single selector](https://github.com/mbostock/d3/wiki/Selections#selecting-elements) specifying a dom block element such as a div; or a dom element or d3 selection. |
| [chartGroup] | <code>String</code> | The name of the chart group this widget should be placed in. Interaction with the widget will only trigger events and redraws within its group. |

**Example**  
```js
// create a cboxMenu under #cbox-container using the default global chart group
var cbox = dc.cboxMenu('#cbox-container')
               .dimension(states)
               .group(stateGroup);
// the option text can be set via the title() function
// by default the option text is '`key`: `value`'
cbox.title(function (d){
    return 'STATE: ' + d.key;
})
```
<a name="dc.cboxMenu+order"></a>

#### cboxMenu.order([order]) ⇒ <code>function</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
Get or set the function that controls the ordering of option tags in the
cbox menu. By default options are ordered by the group key in ascending
order.

**Kind**: instance method of [<code>cboxMenu</code>](#dc.cboxMenu)  

| Param | Type |
| --- | --- |
| [order] | <code>function</code> | 

**Example**  
```js
// order by the group's value
chart.order(function (a,b) {
    return a.value > b.value ? 1 : b.value > a.value ? -1 : 0;
});
```
<a name="dc.cboxMenu+promptText"></a>

#### cboxMenu.promptText([promptText]) ⇒ <code>String</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
Get or set the text displayed in the options used to prompt selection.

**Kind**: instance method of [<code>cboxMenu</code>](#dc.cboxMenu)  

| Param | Type | Default |
| --- | --- | --- |
| [promptText] | <code>String</code> | <code>&#x27;Select all&#x27;</code> | 

**Example**  
```js
chart.promptText('All states');
```
<a name="dc.cboxMenu+filterDisplayed"></a>

#### cboxMenu.filterDisplayed([filterDisplayed]) ⇒ <code>function</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
Get or set the function that filters options prior to display. By default options
with a value of < 1 are not displayed.

**Kind**: instance method of [<code>cboxMenu</code>](#dc.cboxMenu)  

| Param | Type |
| --- | --- |
| [filterDisplayed] | <code>function</code> | 

**Example**  
```js
// display all options override the `filterDisplayed` function:
chart.filterDisplayed(function () {
    return true;
});
```
<a name="dc.cboxMenu+multiple"></a>

#### cboxMenu.multiple([multiple]) ⇒ <code>Boolean</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
Controls the type of input element. Setting it to true converts
the HTML `input` tags from radio buttons to checkboxes.

**Kind**: instance method of [<code>cboxMenu</code>](#dc.cboxMenu)  

| Param | Type | Default |
| --- | --- | --- |
| [multiple] | <code>boolean</code> | <code>false</code> | 

**Example**  
```js
chart.multiple(true);
```
<a name="dc.cboxMenu+promptValue"></a>

#### cboxMenu.promptValue([promptValue]) ⇒ <code>\*</code> \| [<code>cboxMenu</code>](#dc.cboxMenu)
Controls the default value to be used for
[dimension.filter](https://github.com/crossfilter/crossfilter/wiki/API-Reference#dimension_filter)
when only the prompt value is selected. If `null` (the default), no filtering will occur when
just the prompt is selected.

**Kind**: instance method of [<code>cboxMenu</code>](#dc.cboxMenu)  

| Param | Type | Default |
| --- | --- | --- |
| [promptValue] | <code>\*</code> | <code></code> | 

<a name="dc.baseMixin"></a>

### dc.baseMixin ⇒ [<code>baseMixin</code>](#dc.baseMixin)
`dc.baseMixin` is an abstract functional object representing a basic `dc` chart object
for all chart and widget implementations. Methods from the [dc.baseMixin](#dc.baseMixin) are inherited
and available on all chart implementations in the `dc` library.

**Kind**: static mixin of [<code>dc</code>](#dc)  

| Param | Type |
| --- | --- |
| _chart | <code>Object</code> | 


* [.baseMixin](#dc.baseMixin) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.height([height])](#dc.baseMixin+height) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.width([width])](#dc.baseMixin+width) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.minWidth([minWidth])](#dc.baseMixin+minWidth) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.minHeight([minHeight])](#dc.baseMixin+minHeight) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.useViewBoxResizing([useViewBoxResizing])](#dc.baseMixin+useViewBoxResizing) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.dimension([dimension])](#dc.baseMixin+dimension) ⇒ <code>crossfilter.dimension</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.data([callback])](#dc.baseMixin+data) ⇒ <code>\*</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.group([group], [name])](#dc.baseMixin+group) ⇒ <code>crossfilter.group</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.ordering([orderFunction])](#dc.baseMixin+ordering) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.filterAll()](#dc.baseMixin+filterAll) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.select(sel)](#dc.baseMixin+select) ⇒ <code>d3.selection</code>
    * [.selectAll(sel)](#dc.baseMixin+selectAll) ⇒ <code>d3.selection</code>
    * [.anchor([parent], [chartGroup])](#dc.baseMixin+anchor) ⇒ <code>String</code> \| <code>node</code> \| <code>d3.selection</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.anchorName()](#dc.baseMixin+anchorName) ⇒ <code>String</code>
    * [.root([rootElement])](#dc.baseMixin+root) ⇒ <code>HTMLElement</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.svg([svgElement])](#dc.baseMixin+svg) ⇒ <code>SVGElement</code> \| <code>d3.selection</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.resetSvg()](#dc.baseMixin+resetSvg) ⇒ <code>SVGElement</code>
    * [.filterPrinter([filterPrinterFunction])](#dc.baseMixin+filterPrinter) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.controlsUseVisibility([controlsUseVisibility])](#dc.baseMixin+controlsUseVisibility) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.turnOnControls()](#dc.baseMixin+turnOnControls) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.turnOffControls()](#dc.baseMixin+turnOffControls) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.transitionDuration([duration])](#dc.baseMixin+transitionDuration) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.transitionDelay([delay])](#dc.baseMixin+transitionDelay) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.render()](#dc.baseMixin+render) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.redraw()](#dc.baseMixin+redraw) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.commitHandler(commitHandler)](#dc.baseMixin+commitHandler) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.redrawGroup()](#dc.baseMixin+redrawGroup) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.renderGroup()](#dc.baseMixin+renderGroup) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.hasFilterHandler([hasFilterHandler])](#dc.baseMixin+hasFilterHandler) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.hasFilter([filter])](#dc.baseMixin+hasFilter) ⇒ <code>Boolean</code>
    * [.removeFilterHandler([removeFilterHandler])](#dc.baseMixin+removeFilterHandler) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.addFilterHandler([addFilterHandler])](#dc.baseMixin+addFilterHandler) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.resetFilterHandler([resetFilterHandler])](#dc.baseMixin+resetFilterHandler) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.replaceFilter([filter])](#dc.baseMixin+replaceFilter) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.filter([filter])](#dc.baseMixin+filter) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.filters()](#dc.baseMixin+filters) ⇒ <code>Array.&lt;\*&gt;</code>
    * [.onClick(datum)](#dc.baseMixin+onClick) ⇒ <code>undefined</code>
    * [.filterHandler([filterHandler])](#dc.baseMixin+filterHandler) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.keyAccessor([keyAccessor])](#dc.baseMixin+keyAccessor) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.valueAccessor([valueAccessor])](#dc.baseMixin+valueAccessor) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.label([labelFunction], [enableLabels])](#dc.baseMixin+label) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.renderLabel([renderLabel])](#dc.baseMixin+renderLabel) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.title([titleFunction])](#dc.baseMixin+title) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.renderTitle([renderTitle])](#dc.baseMixin+renderTitle) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * ~~[.renderlet(renderletFunction)](#dc.baseMixin+renderlet) ⇒ [<code>baseMixin</code>](#dc.baseMixin)~~
    * [.chartGroup([chartGroup])](#dc.baseMixin+chartGroup) ⇒ <code>String</code> \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.expireCache()](#dc.baseMixin+expireCache) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.legend([legend])](#dc.baseMixin+legend) ⇒ [<code>legend</code>](#dc.legend) \| [<code>baseMixin</code>](#dc.baseMixin)
    * [.chartID()](#dc.baseMixin+chartID) ⇒ <code>String</code>
    * [.options(opts)](#dc.baseMixin+options) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
    * [.on(event, listener)](#dc.baseMixin+on) ⇒ [<code>baseMixin</code>](#dc.baseMixin)

<a name="dc.baseMixin+height"></a>

#### baseMixin.height([height]) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the height attribute of a chart. The height is applied to the SVGElement generated by
the chart when rendered (or re-rendered). If a value is given, then it will be used to calculate
the new height and the chart returned for method chaining.  The value can either be a numeric, a
function, or falsy. If no value is specified then the value of the current height attribute will
be returned.

By default, without an explicit height being given, the chart will select the width of its
anchor element. If that isn't possible it defaults to 200 (provided by the
[minHeight](#dc.baseMixin+minHeight) property). Setting the value falsy will return
the chart to the default behavior.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [minHeight](#dc.baseMixin+minHeight)  

| Param | Type |
| --- | --- |
| [height] | <code>Number</code> \| <code>function</code> | 

**Example**  
```js
// Default height
chart.height(function (element) {
    var height = element && element.getBoundingClientRect && element.getBoundingClientRect().height;
    return (height && height > chart.minHeight()) ? height : chart.minHeight();
});

chart.height(250); // Set the chart's height to 250px;
chart.height(function(anchor) { return doSomethingWith(anchor); }); // set the chart's height with a function
chart.height(null); // reset the height to the default auto calculation
```
<a name="dc.baseMixin+width"></a>

#### baseMixin.width([width]) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the width attribute of a chart.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**

- [height](#dc.baseMixin+height)
- [minWidth](#dc.baseMixin+minWidth)


| Param | Type |
| --- | --- |
| [width] | <code>Number</code> \| <code>function</code> | 

**Example**  
```js
// Default width
chart.width(function (element) {
    var width = element && element.getBoundingClientRect && element.getBoundingClientRect().width;
    return (width && width > chart.minWidth()) ? width : chart.minWidth();
});
```
<a name="dc.baseMixin+minWidth"></a>

#### baseMixin.minWidth([minWidth]) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the minimum width attribute of a chart. This only has effect when used with the default
[width](#dc.baseMixin+width) function.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [width](#dc.baseMixin+width)  

| Param | Type | Default |
| --- | --- | --- |
| [minWidth] | <code>Number</code> | <code>200</code> | 

<a name="dc.baseMixin+minHeight"></a>

#### baseMixin.minHeight([minHeight]) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the minimum height attribute of a chart. This only has effect when used with the default
[height](#dc.baseMixin+height) function.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [height](#dc.baseMixin+height)  

| Param | Type | Default |
| --- | --- | --- |
| [minHeight] | <code>Number</code> | <code>200</code> | 

<a name="dc.baseMixin+useViewBoxResizing"></a>

#### baseMixin.useViewBoxResizing([useViewBoxResizing]) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Turn on/off using the SVG
[`viewBox` attribute](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/viewBox).
When enabled, `viewBox` will be set on the svg root element instead of `width` and `height`.
Requires that the chart aspect ratio be defined using chart.width(w) and chart.height(h).

This will maintain the aspect ratio while enabling the chart to resize responsively to the
space given to the chart using CSS. For example, the chart can use `width: 100%; height:
100%` or absolute positioning to resize to its parent div.

Since the text will be sized as if the chart is drawn according to the width and height, and
will be resized if the chart is any other size, you need to set the chart width and height so
that the text looks good. In practice, 600x400 seems to work pretty well for most charts.

You can see examples of this resizing strategy in the [Chart Resizing
Examples](http://dc-js.github.io/dc.js/resizing/); just add `?resize=viewbox` to any of the
one-chart examples to enable `useViewBoxResizing`.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [useViewBoxResizing] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.baseMixin+dimension"></a>

#### baseMixin.dimension([dimension]) ⇒ <code>crossfilter.dimension</code> \| [<code>baseMixin</code>](#dc.baseMixin)
**mandatory**

Set or get the dimension attribute of a chart. In `dc`, a dimension can be any valid
[crossfilter dimension](https://github.com/crossfilter/crossfilter/wiki/API-Reference#dimension)

If a value is given, then it will be used as the new dimension. If no value is specified then
the current dimension will be returned.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [crossfilter.dimension](https://github.com/crossfilter/crossfilter/wiki/API-Reference#dimension)  

| Param | Type |
| --- | --- |
| [dimension] | <code>crossfilter.dimension</code> | 

**Example**  
```js
var index = crossfilter([]);
var dimension = index.dimension(dc.pluck('key'));
chart.dimension(dimension);
```
<a name="dc.baseMixin+data"></a>

#### baseMixin.data([callback]) ⇒ <code>\*</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set the data callback or retrieve the chart's data set. The data callback is passed the chart's
group and by default will return
[group.all](https://github.com/crossfilter/crossfilter/wiki/API-Reference#group_all).
This behavior may be modified to, for instance, return only the top 5 groups.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [callback] | <code>function</code> | 

**Example**  
```js
// Default data function
chart.data(function (group) { return group.all(); });

chart.data(function (group) { return group.top(5); });
```
<a name="dc.baseMixin+group"></a>

#### baseMixin.group([group], [name]) ⇒ <code>crossfilter.group</code> \| [<code>baseMixin</code>](#dc.baseMixin)
**mandatory**

Set or get the group attribute of a chart. In `dc` a group is a
[crossfilter group](https://github.com/crossfilter/crossfilter/wiki/API-Reference#group-map-reduce).
Usually the group should be created from the particular dimension associated with the same chart. If a value is
given, then it will be used as the new group.

If no value specified then the current group will be returned.
If `name` is specified then it will be used to generate legend label.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [crossfilter.group](https://github.com/crossfilter/crossfilter/wiki/API-Reference#group-map-reduce)  

| Param | Type |
| --- | --- |
| [group] | <code>crossfilter.group</code> | 
| [name] | <code>String</code> | 

**Example**  
```js
var index = crossfilter([]);
var dimension = index.dimension(dc.pluck('key'));
chart.dimension(dimension);
chart.group(dimension.group().reduceSum());
```
<a name="dc.baseMixin+ordering"></a>

#### baseMixin.ordering([orderFunction]) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Get or set an accessor to order ordinal dimensions.  The chart uses
[Array.sort](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
to sort elements; this accessor returns the value to order on.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [orderFunction] | <code>function</code> | 

**Example**  
```js
// Default ordering accessor
_chart.ordering(dc.pluck('key'));
```
<a name="dc.baseMixin+filterAll"></a>

#### baseMixin.filterAll() ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Clear all filters associated with this chart. The same effect can be achieved by calling
[chart.filter(null)](#dc.baseMixin+filter).

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
<a name="dc.baseMixin+select"></a>

#### baseMixin.select(sel) ⇒ <code>d3.selection</code>
Execute d3 single selection in the chart's scope using the given selector and return the d3
selection.

This function is **not chainable** since it does not return a chart instance; however the d3
selection result can be chained to d3 function calls.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [d3.select](https://github.com/d3/d3-selection/blob/master/README.md#select)  

| Param | Type | Description |
| --- | --- | --- |
| sel | <code>String</code> | CSS selector string |

**Example**  
```js
// Has the same effect as d3.select('#chart-id').select(selector)
chart.select(selector)
```
<a name="dc.baseMixin+selectAll"></a>

#### baseMixin.selectAll(sel) ⇒ <code>d3.selection</code>
Execute in scope d3 selectAll using the given selector and return d3 selection result.

This function is **not chainable** since it does not return a chart instance; however the d3
selection result can be chained to d3 function calls.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [d3.selectAll](https://github.com/d3/d3-selection/blob/master/README.md#selectAll)  

| Param | Type | Description |
| --- | --- | --- |
| sel | <code>String</code> | CSS selector string |

**Example**  
```js
// Has the same effect as d3.select('#chart-id').selectAll(selector)
chart.selectAll(selector)
```
<a name="dc.baseMixin+anchor"></a>

#### baseMixin.anchor([parent], [chartGroup]) ⇒ <code>String</code> \| <code>node</code> \| <code>d3.selection</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set the root SVGElement to either be an existing chart's root; or any valid [d3 single
selector](https://github.com/d3/d3-selection/blob/master/README.md#selecting-elements) specifying a dom
block element such as a div; or a dom element or d3 selection. Optionally registers the chart
within the chartGroup. This class is called internally on chart initialization, but be called
again to relocate the chart. However, it will orphan any previously created SVGElements.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [parent] | <code>anchorChart</code> \| <code>anchorSelector</code> \| <code>anchorNode</code> | 
| [chartGroup] | <code>String</code> | 

<a name="dc.baseMixin+anchorName"></a>

#### baseMixin.anchorName() ⇒ <code>String</code>
Returns the DOM id for the chart's anchored location.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
<a name="dc.baseMixin+root"></a>

#### baseMixin.root([rootElement]) ⇒ <code>HTMLElement</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Returns the root element where a chart resides. Usually it will be the parent div element where
the SVGElement was created. You can also pass in a new root element however this is usually handled by
dc internally. Resetting the root element on a chart outside of dc internals may have
unexpected consequences.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [HTMLElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement)  

| Param | Type |
| --- | --- |
| [rootElement] | <code>HTMLElement</code> | 

<a name="dc.baseMixin+svg"></a>

#### baseMixin.svg([svgElement]) ⇒ <code>SVGElement</code> \| <code>d3.selection</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Returns the top SVGElement for this specific chart. You can also pass in a new SVGElement,
however this is usually handled by dc internally. Resetting the SVGElement on a chart outside
of dc internals may have unexpected consequences.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [SVGElement](https://developer.mozilla.org/en-US/docs/Web/API/SVGElement)  

| Param | Type |
| --- | --- |
| [svgElement] | <code>SVGElement</code> \| <code>d3.selection</code> | 

<a name="dc.baseMixin+resetSvg"></a>

#### baseMixin.resetSvg() ⇒ <code>SVGElement</code>
Remove the chart's SVGElements from the dom and recreate the container SVGElement.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [SVGElement](https://developer.mozilla.org/en-US/docs/Web/API/SVGElement)  
<a name="dc.baseMixin+filterPrinter"></a>

#### baseMixin.filterPrinter([filterPrinterFunction]) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the filter printer function. The filter printer function is used to generate human
friendly text for filter value(s) associated with the chart instance. The text will get shown
in the `.filter element; see [turnOnControls](#dc.baseMixin+turnOnControls).

By default dc charts use a default filter printer [filters](#dc.printers.filters)
that provides simple printing support for both single value and ranged filters.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [filterPrinterFunction] | <code>function</code> | <code>dc.printers.filters</code> | 

**Example**  
```js
// for a chart with an ordinal brush, print the filters in upper case
chart.filterPrinter(function(filters) {
  return filters.map(function(f) { return f.toUpperCase(); }).join(', ');
});
// for a chart with a range brush, print the filter as start and extent
chart.filterPrinter(function(filters) {
  return 'start ' + dc.utils.printSingleValue(filters[0][0]) +
    ' extent ' + dc.utils.printSingleValue(filters[0][1] - filters[0][0]);
});
```
<a name="dc.baseMixin+controlsUseVisibility"></a>

#### baseMixin.controlsUseVisibility([controlsUseVisibility]) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
If set, use the `visibility` attribute instead of the `display` attribute for showing/hiding
chart reset and filter controls, for less disruption to the layout.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [controlsUseVisibility] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.baseMixin+turnOnControls"></a>

#### baseMixin.turnOnControls() ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Turn on optional control elements within the root element. dc currently supports the
following html control elements.
* root.selectAll('.reset') - elements are turned on if the chart has an active filter. This type
of control element is usually used to store a reset link to allow user to reset filter on a
certain chart. This element will be turned off automatically if the filter is cleared.
* root.selectAll('.filter') elements are turned on if the chart has an active filter. The text
content of this element is then replaced with the current filter value using the filter printer
function. This type of element will be turned off automatically if the filter is cleared.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
<a name="dc.baseMixin+turnOffControls"></a>

#### baseMixin.turnOffControls() ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Turn off optional control elements within the root element.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [turnOnControls](#dc.baseMixin+turnOnControls)  
<a name="dc.baseMixin+transitionDuration"></a>

#### baseMixin.transitionDuration([duration]) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the animation transition duration (in milliseconds) for this chart instance.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [duration] | <code>Number</code> | <code>750</code> | 

<a name="dc.baseMixin+transitionDelay"></a>

#### baseMixin.transitionDelay([delay]) ⇒ <code>Number</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the animation transition delay (in milliseconds) for this chart instance.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [delay] | <code>Number</code> | <code>0</code> | 

<a name="dc.baseMixin+render"></a>

#### baseMixin.render() ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Invoking this method will force the chart to re-render everything from scratch. Generally it
should only be used to render the chart for the first time on the page or if you want to make
sure everything is redrawn from scratch instead of relying on the default incremental redrawing
behaviour.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
<a name="dc.baseMixin+redraw"></a>

#### baseMixin.redraw() ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Calling redraw will cause the chart to re-render data changes incrementally. If there is no
change in the underlying data dimension then calling this method will have no effect on the
chart. Most chart interaction in dc will automatically trigger this method through internal
events (in particular [redrawAll](#dc.redrawAll)); therefore, you only need to
manually invoke this function if data is manipulated outside of dc's control (for example if
data is loaded in the background using
[crossfilter.add](https://github.com/crossfilter/crossfilter/wiki/API-Reference#crossfilter_add)).

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
<a name="dc.baseMixin+commitHandler"></a>

#### baseMixin.commitHandler(commitHandler) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Gets/sets the commit handler. If the chart has a commit handler, the handler will be called when
the chart's filters have changed, in order to send the filter data asynchronously to a server.

Unlike other functions in dc.js, the commit handler is asynchronous. It takes two arguments:
a flag indicating whether this is a render (true) or a redraw (false), and a callback to be
triggered once the commit is done. The callback has the standard node.js continuation signature
with error first and result second.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| commitHandler | <code>function</code> | 

<a name="dc.baseMixin+redrawGroup"></a>

#### baseMixin.redrawGroup() ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Redraws all charts in the same group as this chart, typically in reaction to a filter
change. If the chart has a [commitHandler](dc.baseMixin.commitFilter), it will
be executed and waited for.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
<a name="dc.baseMixin+renderGroup"></a>

#### baseMixin.renderGroup() ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Renders all charts in the same group as this chart. If the chart has a
[commitHandler](dc.baseMixin.commitFilter), it will be executed and waited for

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
<a name="dc.baseMixin+hasFilterHandler"></a>

#### baseMixin.hasFilterHandler([hasFilterHandler]) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the has-filter handler. The has-filter handler is a function that checks to see if
the chart's current filters (first argument) include a specific filter (second argument).  Using a custom has-filter handler allows
you to change the way filters are checked for and replaced.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [hasFilterHandler] | <code>function</code> | 

**Example**  
```js
// default has-filter handler
chart.hasFilterHandler(function (filters, filter) {
    if (filter === null || typeof(filter) === 'undefined') {
        return filters.length > 0;
    }
    return filters.some(function (f) {
        return filter <= f && filter >= f;
    });
});

// custom filter handler (no-op)
chart.hasFilterHandler(function(filters, filter) {
    return false;
});
```
<a name="dc.baseMixin+hasFilter"></a>

#### baseMixin.hasFilter([filter]) ⇒ <code>Boolean</code>
Check whether any active filter or a specific filter is associated with particular chart instance.
This function is **not chainable**.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [hasFilterHandler](#dc.baseMixin+hasFilterHandler)  

| Param | Type |
| --- | --- |
| [filter] | <code>\*</code> | 

<a name="dc.baseMixin+removeFilterHandler"></a>

#### baseMixin.removeFilterHandler([removeFilterHandler]) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the remove filter handler. The remove filter handler is a function that removes a
filter from the chart's current filters. Using a custom remove filter handler allows you to
change how filters are removed or perform additional work when removing a filter, e.g. when
using a filter server other than crossfilter.

The handler should return a new or modified array as the result.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [removeFilterHandler] | <code>function</code> | 

**Example**  
```js
// default remove filter handler
chart.removeFilterHandler(function (filters, filter) {
    for (var i = 0; i < filters.length; i++) {
        if (filters[i] <= filter && filters[i] >= filter) {
            filters.splice(i, 1);
            break;
        }
    }
    return filters;
});

// custom filter handler (no-op)
chart.removeFilterHandler(function(filters, filter) {
    return filters;
});
```
<a name="dc.baseMixin+addFilterHandler"></a>

#### baseMixin.addFilterHandler([addFilterHandler]) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the add filter handler. The add filter handler is a function that adds a filter to
the chart's filter list. Using a custom add filter handler allows you to change the way filters
are added or perform additional work when adding a filter, e.g. when using a filter server other
than crossfilter.

The handler should return a new or modified array as the result.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [addFilterHandler] | <code>function</code> | 

**Example**  
```js
// default add filter handler
chart.addFilterHandler(function (filters, filter) {
    filters.push(filter);
    return filters;
});

// custom filter handler (no-op)
chart.addFilterHandler(function(filters, filter) {
    return filters;
});
```
<a name="dc.baseMixin+resetFilterHandler"></a>

#### baseMixin.resetFilterHandler([resetFilterHandler]) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Set or get the reset filter handler. The reset filter handler is a function that resets the
chart's filter list by returning a new list. Using a custom reset filter handler allows you to
change the way filters are reset, or perform additional work when resetting the filters,
e.g. when using a filter server other than crossfilter.

The handler should return a new or modified array as the result.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [resetFilterHandler] | <code>function</code> | 

**Example**  
```js
// default remove filter handler
function (filters) {
    return [];
}

// custom filter handler (no-op)
chart.resetFilterHandler(function(filters) {
    return filters;
});
```
<a name="dc.baseMixin+replaceFilter"></a>

#### baseMixin.replaceFilter([filter]) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Replace the chart filter. This is equivalent to calling `chart.filter(null).filter(filter)`
but more efficient because the filter is only applied once.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [filter] | <code>\*</code> | 

<a name="dc.baseMixin+filter"></a>

#### baseMixin.filter([filter]) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Filter the chart by the given parameter, or return the current filter if no input parameter
is given.

The filter parameter can take one of these forms:
* A single value: the value will be toggled (added if it is not present in the current
filters, removed if it is present)
* An array containing a single array of values (`[[value,value,value]]`): each value is
toggled
* When appropriate for the chart, a [dc filter object](#dc.filters) such as
  * [`dc.filters.RangedFilter`](#dc.filters.RangedFilter) for the
[coordinateGridMixin](#dc.coordinateGridMixin) charts
  * [`dc.filters.TwoDimensionalFilter`](#dc.filters.TwoDimensionalFilter) for the
[heat map](#dc.heatMap)
  * [`dc.filters.RangedTwoDimensionalFilter`](#dc.filters.RangedTwoDimensionalFilter)
for the [scatter plot](#dc.scatterPlot)
* `null`: the filter will be reset using the
[resetFilterHandler](#dc.baseMixin+resetFilterHandler)

Note that this is always a toggle (even when it doesn't make sense for the filter type). If
you wish to replace the current filter, either call `chart.filter(null)` first - or it's more
efficient to call [`chart.replaceFilter(filter)`](#dc.baseMixin+replaceFilter) instead.

Each toggle is executed by checking if the value is already present using the
[hasFilterHandler](#dc.baseMixin+hasFilterHandler); if it is not present, it is added
using the [addFilterHandler](#dc.baseMixin+addFilterHandler); if it is already present,
it is removed using the [removeFilterHandler](#dc.baseMixin+removeFilterHandler).

Once the filters array has been updated, the filters are applied to the
crossfilter dimension, using the [filterHandler](#dc.baseMixin+filterHandler).

Once you have set the filters, call [`chart.redrawGroup()`](#dc.baseMixin+redrawGroup)
(or [`dc.redrawAll()`](#dc.redrawAll)) to redraw the chart's group.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**

- [addFilterHandler](#dc.baseMixin+addFilterHandler)
- [removeFilterHandler](#dc.baseMixin+removeFilterHandler)
- [resetFilterHandler](#dc.baseMixin+resetFilterHandler)
- [filterHandler](#dc.baseMixin+filterHandler)


| Param | Type |
| --- | --- |
| [filter] | <code>\*</code> | 

**Example**  
```js
// filter by a single string
chart.filter('Sunday');
// filter by a single age
chart.filter(18);
// filter by a set of states
chart.filter([['MA', 'TX', 'ND', 'WA']]);
// filter by range -- note the use of dc.filters.RangedFilter, which is different
// from the syntax for filtering a crossfilter dimension directly, dimension.filter([15,20])
chart.filter(dc.filters.RangedFilter(15,20));
```
<a name="dc.baseMixin+filters"></a>

#### baseMixin.filters() ⇒ <code>Array.&lt;\*&gt;</code>
Returns all current filters. This method does not perform defensive cloning of the internal
filter array before returning, therefore any modification of the returned array will effect the
chart's internal filter storage.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
<a name="dc.baseMixin+onClick"></a>

#### baseMixin.onClick(datum) ⇒ <code>undefined</code>
This function is passed to d3 as the onClick handler for each chart. The default behavior is to
filter on the clicked datum (passed to the callback) and redraw the chart group.

This function can be replaced in order to change the click behavior (but first look at

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| datum | <code>\*</code> | 

**Example**  
```js
var oldHandler = chart.onClick;
chart.onClick = function(datum) {
  // use datum.
```
<a name="dc.baseMixin+filterHandler"></a>

#### baseMixin.filterHandler([filterHandler]) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the filter handler. The filter handler is a function that performs the filter action
on a specific dimension. Using a custom filter handler allows you to perform additional logic
before or after filtering.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [crossfilter.dimension.filter](https://github.com/crossfilter/crossfilter/wiki/API-Reference#dimension_filter)  

| Param | Type |
| --- | --- |
| [filterHandler] | <code>function</code> | 

**Example**  
```js
// the default filter handler handles all possible cases for the charts in dc.js
// you can replace it with something more specialized for your own chart
chart.filterHandler(function (dimension, filters) {
    if (filters.length === 0) {
        // the empty case (no filtering)
        dimension.filter(null);
    } else if (filters.length === 1 && !filters[0].isFiltered) {
        // single value and not a function-based filter
        dimension.filterExact(filters[0]);
    } else if (filters.length === 1 && filters[0].filterType === 'RangedFilter') {
        // single range-based filter
        dimension.filterRange(filters[0]);
    } else {
        // an array of values, or an array of filter objects
        dimension.filterFunction(function (d) {
            for (var i = 0; i < filters.length; i++) {
                var filter = filters[i];
                if (filter.isFiltered && filter.isFiltered(d)) {
                    return true;
                } else if (filter <= d && filter >= d) {
                    return true;
                }
            }
            return false;
        });
    }
    return filters;
});

// custom filter handler
chart.filterHandler(function(dimension, filter){
    var newFilter = filter + 10;
    dimension.filter(newFilter);
    return newFilter; // set the actual filter value to the new value
});
```
<a name="dc.baseMixin+keyAccessor"></a>

#### baseMixin.keyAccessor([keyAccessor]) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the key accessor function. The key accessor function is used to retrieve the key
value from the crossfilter group. Key values are used differently in different charts, for
example keys correspond to slices in a pie chart and x axis positions in a grid coordinate chart.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [keyAccessor] | <code>function</code> | 

**Example**  
```js
// default key accessor
chart.keyAccessor(function(d) { return d.key; });
// custom key accessor for a multi-value crossfilter reduction
chart.keyAccessor(function(p) { return p.value.absGain; });
```
<a name="dc.baseMixin+valueAccessor"></a>

#### baseMixin.valueAccessor([valueAccessor]) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the value accessor function. The value accessor function is used to retrieve the
value from the crossfilter group. Group values are used differently in different charts, for
example values correspond to slice sizes in a pie chart and y axis positions in a grid
coordinate chart.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [valueAccessor] | <code>function</code> | 

**Example**  
```js
// default value accessor
chart.valueAccessor(function(d) { return d.value; });
// custom value accessor for a multi-value crossfilter reduction
chart.valueAccessor(function(p) { return p.value.percentageGain; });
```
<a name="dc.baseMixin+label"></a>

#### baseMixin.label([labelFunction], [enableLabels]) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the label function. The chart class will use this function to render labels for each
child element in the chart, e.g. slices in a pie chart or bubbles in a bubble chart. Not every
chart supports the label function, for example line chart does not use this function
at all. By default, enables labels; pass false for the second parameter if this is not desired.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [labelFunction] | <code>function</code> |  | 
| [enableLabels] | <code>Boolean</code> | <code>true</code> | 

**Example**  
```js
// default label function just return the key
chart.label(function(d) { return d.key; });
// label function has access to the standard d3 data binding and can get quite complicated
chart.label(function(d) { return d.data.key + '(' + Math.floor(d.data.value / all.value() * 100) + '%)'; });
```
<a name="dc.baseMixin+renderLabel"></a>

#### baseMixin.renderLabel([renderLabel]) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Turn on/off label rendering

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [renderLabel] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.baseMixin+title"></a>

#### baseMixin.title([titleFunction]) ⇒ <code>function</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Set or get the title function. The chart class will use this function to render the SVGElement title
(usually interpreted by browser as tooltips) for each child element in the chart, e.g. a slice
in a pie chart or a bubble in a bubble chart. Almost every chart supports the title function;
however in grid coordinate charts you need to turn off the brush in order to see titles, because
otherwise the brush layer will block tooltip triggering.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [titleFunction] | <code>function</code> | 

**Example**  
```js
// default title function shows "key: value"
chart.title(function(d) { return d.key + ': ' + d.value; });
// title function has access to the standard d3 data binding and can get quite complicated
chart.title(function(p) {
   return p.key.getFullYear()
       + '\n'
       + 'Index Gain: ' + numberFormat(p.value.absGain) + '\n'
       + 'Index Gain in Percentage: ' + numberFormat(p.value.percentageGain) + '%\n'
       + 'Fluctuation / Index Ratio: ' + numberFormat(p.value.fluctuationPercentage) + '%';
});
```
<a name="dc.baseMixin+renderTitle"></a>

#### baseMixin.renderTitle([renderTitle]) ⇒ <code>Boolean</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Turn on/off title rendering, or return the state of the render title flag if no arguments are
given.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [renderTitle] | <code>Boolean</code> | <code>true</code> | 

<a name="dc.baseMixin+renderlet"></a>

#### ~~baseMixin.renderlet(renderletFunction) ⇒ [<code>baseMixin</code>](#dc.baseMixin)~~
***Deprecated***

A renderlet is similar to an event listener on rendering event. Multiple renderlets can be added
to an individual chart.  Each time a chart is rerendered or redrawn the renderlets are invoked
right after the chart finishes its transitions, giving you a way to modify the SVGElements.
Renderlet functions take the chart instance as the only input parameter and you can
use the dc API or use raw d3 to achieve pretty much any effect.

Use [on](#dc.baseMixin+on) with a 'renderlet' prefix.
Generates a random key for the renderlet, which makes it hard to remove.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| renderletFunction | <code>function</code> | 

**Example**  
```js
// do this instead of .renderlet(function(chart) { ... })
chart.on("renderlet", function(chart){
    // mix of dc API and d3 manipulation
    chart.select('g.y').style('display', 'none');
    // its a closure so you can also access other chart variable available in the closure scope
    moveChart.filter(chart.filter());
});
```
<a name="dc.baseMixin+chartGroup"></a>

#### baseMixin.chartGroup([chartGroup]) ⇒ <code>String</code> \| [<code>baseMixin</code>](#dc.baseMixin)
Get or set the chart group to which this chart belongs. Chart groups are rendered or redrawn
together since it is expected they share the same underlying crossfilter data set.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [chartGroup] | <code>String</code> | 

<a name="dc.baseMixin+expireCache"></a>

#### baseMixin.expireCache() ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Expire the internal chart cache. dc charts cache some data internally on a per chart basis to
speed up rendering and avoid unnecessary calculation; however it might be useful to clear the
cache if you have changed state which will affect rendering.  For example, if you invoke
[crossfilter.add](https://github.com/crossfilter/crossfilter/wiki/API-Reference#crossfilter_add)
function or reset group or dimension after rendering, it is a good idea to
clear the cache to make sure charts are rendered properly.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
<a name="dc.baseMixin+legend"></a>

#### baseMixin.legend([legend]) ⇒ [<code>legend</code>](#dc.legend) \| [<code>baseMixin</code>](#dc.baseMixin)
Attach a dc.legend widget to this chart. The legend widget will automatically draw legend labels
based on the color setting and names associated with each group.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| [legend] | [<code>legend</code>](#dc.legend) | 

**Example**  
```js
chart.legend(dc.legend().x(400).y(10).itemHeight(13).gap(5))
```
<a name="dc.baseMixin+chartID"></a>

#### baseMixin.chartID() ⇒ <code>String</code>
Returns the internal numeric ID of the chart.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
<a name="dc.baseMixin+options"></a>

#### baseMixin.options(opts) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
Set chart options using a configuration object. Each key in the object will cause the method of
the same name to be called with the value to set that attribute for the chart.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| opts | <code>Object</code> | 

**Example**  
```js
chart.options({dimension: myDimension, group: myGroup});
```
<a name="dc.baseMixin+on"></a>

#### baseMixin.on(event, listener) ⇒ [<code>baseMixin</code>](#dc.baseMixin)
All dc chart instance supports the following listeners.
Supports the following events:
* `renderlet` - This listener function will be invoked after transitions after redraw and render. Replaces the
deprecated [renderlet](#dc.baseMixin+renderlet) method.
* `pretransition` - Like `.on('renderlet', ...)` but the event is fired before transitions start.
* `preRender` - This listener function will be invoked before chart rendering.
* `postRender` - This listener function will be invoked after chart finish rendering including
all renderlets' logic.
* `preRedraw` - This listener function will be invoked before chart redrawing.
* `postRedraw` - This listener function will be invoked after chart finish redrawing
including all renderlets' logic.
* `filtered` - This listener function will be invoked after a filter is applied, added or removed.
* `zoomed` - This listener function will be invoked after a zoom is triggered.

**Kind**: instance method of [<code>baseMixin</code>](#dc.baseMixin)  
**See**: [d3.dispatch.on](https://github.com/d3/d3-dispatch/blob/master/README.md#dispatch_on)  

| Param | Type |
| --- | --- |
| event | <code>String</code> | 
| listener | <code>function</code> | 

**Example**  
```js
.on('renderlet', function(chart, filter){...})
.on('pretransition', function(chart, filter){...})
.on('preRender', function(chart){...})
.on('postRender', function(chart){...})
.on('preRedraw', function(chart){...})
.on('postRedraw', function(chart){...})
.on('filtered', function(chart, filter){...})
.on('zoomed', function(chart, filter){...})
```
<a name="dc.marginMixin"></a>

### dc.marginMixin ⇒ [<code>marginMixin</code>](#dc.marginMixin)
Margin is a mixin that provides margin utility functions for both the Row Chart and Coordinate Grid
Charts.

**Kind**: static mixin of [<code>dc</code>](#dc)  

| Param | Type |
| --- | --- |
| _chart | <code>Object</code> | 

<a name="dc.marginMixin+margins"></a>

#### marginMixin.margins([margins]) ⇒ <code>Object</code> \| [<code>marginMixin</code>](#dc.marginMixin)
Get or set the margins for a particular coordinate grid chart instance. The margins is stored as
an associative Javascript array.

**Kind**: instance method of [<code>marginMixin</code>](#dc.marginMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [margins] | <code>Object</code> | <code>{top: 10, right: 50, bottom: 30, left: 30}</code> | 

**Example**  
```js
var leftMargin = chart.margins().left; // 30 by default
chart.margins().left = 50;
leftMargin = chart.margins().left; // now 50
```
<a name="dc.colorMixin"></a>

### dc.colorMixin ⇒ [<code>colorMixin</code>](#dc.colorMixin)
The Color Mixin is an abstract chart functional class providing universal coloring support
as a mix-in for any concrete chart implementation.

**Kind**: static mixin of [<code>dc</code>](#dc)  

| Param | Type |
| --- | --- |
| _chart | <code>Object</code> | 


* [.colorMixin](#dc.colorMixin) ⇒ [<code>colorMixin</code>](#dc.colorMixin)
    * [.colors([colorScale])](#dc.colorMixin+colors) ⇒ <code>d3.scale</code> \| [<code>colorMixin</code>](#dc.colorMixin)
    * [.ordinalColors(r)](#dc.colorMixin+ordinalColors) ⇒ [<code>colorMixin</code>](#dc.colorMixin)
    * [.linearColors(r)](#dc.colorMixin+linearColors) ⇒ [<code>colorMixin</code>](#dc.colorMixin)
    * [.colorAccessor([colorAccessor])](#dc.colorMixin+colorAccessor) ⇒ <code>function</code> \| [<code>colorMixin</code>](#dc.colorMixin)
    * [.colorDomain([domain])](#dc.colorMixin+colorDomain) ⇒ <code>Array.&lt;String&gt;</code> \| [<code>colorMixin</code>](#dc.colorMixin)
    * [.calculateColorDomain()](#dc.colorMixin+calculateColorDomain) ⇒ [<code>colorMixin</code>](#dc.colorMixin)
    * [.getColor(d, [i])](#dc.colorMixin+getColor) ⇒ <code>String</code>
    * [.colorCalculator([colorCalculator])](#dc.colorMixin+colorCalculator) ⇒ <code>function</code> \| [<code>colorMixin</code>](#dc.colorMixin)

<a name="dc.colorMixin+colors"></a>

#### colorMixin.colors([colorScale]) ⇒ <code>d3.scale</code> \| [<code>colorMixin</code>](#dc.colorMixin)
Retrieve current color scale or set a new color scale. This methods accepts any function that
operates like a d3 scale.

**Kind**: instance method of [<code>colorMixin</code>](#dc.colorMixin)  
**See**: [d3.scale](https://github.com/d3/d3-scale/blob/master/README.md)  

| Param | Type | Default |
| --- | --- | --- |
| [colorScale] | <code>d3.scale</code> | <code>d3.scaleOrdinal(d3.schemeCategory20c)</code> | 

**Example**  
```js
// alternate categorical scale
chart.colors(d3.scale.category20b());
// ordinal scale
chart.colors(d3.scaleOrdinal().range(['red','green','blue']));
// convenience method, the same as above
chart.ordinalColors(['red','green','blue']);
// set a linear scale
chart.linearColors(["#4575b4", "#ffffbf", "#a50026"]);
```
<a name="dc.colorMixin+ordinalColors"></a>

#### colorMixin.ordinalColors(r) ⇒ [<code>colorMixin</code>](#dc.colorMixin)
Convenience method to set the color scale to
[d3.scaleOrdinal](https://github.com/d3/d3-scale/blob/master/README.md#ordinal-scales) with
range `r`.

**Kind**: instance method of [<code>colorMixin</code>](#dc.colorMixin)  

| Param | Type |
| --- | --- |
| r | <code>Array.&lt;String&gt;</code> | 

<a name="dc.colorMixin+linearColors"></a>

#### colorMixin.linearColors(r) ⇒ [<code>colorMixin</code>](#dc.colorMixin)
Convenience method to set the color scale to an Hcl interpolated linear scale with range `r`.

**Kind**: instance method of [<code>colorMixin</code>](#dc.colorMixin)  

| Param | Type |
| --- | --- |
| r | <code>Array.&lt;Number&gt;</code> | 

<a name="dc.colorMixin+colorAccessor"></a>

#### colorMixin.colorAccessor([colorAccessor]) ⇒ <code>function</code> \| [<code>colorMixin</code>](#dc.colorMixin)
Set or the get color accessor function. This function will be used to map a data point in a
crossfilter group to a color value on the color scale. The default function uses the key
accessor.

**Kind**: instance method of [<code>colorMixin</code>](#dc.colorMixin)  

| Param | Type |
| --- | --- |
| [colorAccessor] | <code>function</code> | 

**Example**  
```js
// default index based color accessor
.colorAccessor(function (d, i){return i;})
// color accessor for a multi-value crossfilter reduction
.colorAccessor(function (d){return d.value.absGain;})
```
<a name="dc.colorMixin+colorDomain"></a>

#### colorMixin.colorDomain([domain]) ⇒ <code>Array.&lt;String&gt;</code> \| [<code>colorMixin</code>](#dc.colorMixin)
Set or get the current domain for the color mapping function. The domain must be supplied as an
array.

Note: previously this method accepted a callback function. Instead you may use a custom scale
set by [.colors](#dc.colorMixin+colors).

**Kind**: instance method of [<code>colorMixin</code>](#dc.colorMixin)  

| Param | Type |
| --- | --- |
| [domain] | <code>Array.&lt;String&gt;</code> | 

<a name="dc.colorMixin+calculateColorDomain"></a>

#### colorMixin.calculateColorDomain() ⇒ [<code>colorMixin</code>](#dc.colorMixin)
Set the domain by determining the min and max values as retrieved by
[.colorAccessor](#dc.colorMixin+colorAccessor) over the chart's dataset.

**Kind**: instance method of [<code>colorMixin</code>](#dc.colorMixin)  
<a name="dc.colorMixin+getColor"></a>

#### colorMixin.getColor(d, [i]) ⇒ <code>String</code>
Get the color for the datum d and counter i. This is used internally by charts to retrieve a color.

**Kind**: instance method of [<code>colorMixin</code>](#dc.colorMixin)  

| Param | Type |
| --- | --- |
| d | <code>\*</code> | 
| [i] | <code>Number</code> | 

<a name="dc.colorMixin+colorCalculator"></a>

#### colorMixin.colorCalculator([colorCalculator]) ⇒ <code>function</code> \| [<code>colorMixin</code>](#dc.colorMixin)
Overrides the color selection algorithm, replacing it with a simple function.

Normally colors will be determined by calling the `colorAccessor` to get a value, and then passing that
value through the `colorScale`.

But sometimes it is difficult to get a color scale to produce the desired effect. The `colorCalculator`
takes the datum and index and returns a color directly.

**Kind**: instance method of [<code>colorMixin</code>](#dc.colorMixin)  

| Param | Type |
| --- | --- |
| [colorCalculator] | <code>\*</code> | 

<a name="dc.coordinateGridMixin"></a>

### dc.coordinateGridMixin ⇒ [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Coordinate Grid is an abstract base chart designed to support a number of coordinate grid based
concrete chart types, e.g. bar chart, line chart, and bubble chart.

**Kind**: static mixin of [<code>dc</code>](#dc)  
**Mixes**: [<code>colorMixin</code>](#dc.colorMixin), [<code>marginMixin</code>](#dc.marginMixin), [<code>baseMixin</code>](#dc.baseMixin)  

| Param | Type |
| --- | --- |
| _chart | <code>Object</code> | 


* [.coordinateGridMixin](#dc.coordinateGridMixin) ⇒ [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.rescale()](#dc.coordinateGridMixin+rescale) ⇒ [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.rangeChart([rangeChart])](#dc.coordinateGridMixin+rangeChart) ⇒ [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.zoomScale([extent])](#dc.coordinateGridMixin+zoomScale) ⇒ <code>Array.&lt;(Number\|Date)&gt;</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.zoomOutRestrict([zoomOutRestrict])](#dc.coordinateGridMixin+zoomOutRestrict) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.g([gElement])](#dc.coordinateGridMixin+g) ⇒ <code>SVGElement</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.mouseZoomable([mouseZoomable])](#dc.coordinateGridMixin+mouseZoomable) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.chartBodyG([chartBodyG])](#dc.coordinateGridMixin+chartBodyG) ⇒ <code>SVGElement</code>
    * [.x([xScale])](#dc.coordinateGridMixin+x) ⇒ <code>d3.scale</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.xUnits([xUnits])](#dc.coordinateGridMixin+xUnits) ⇒ <code>function</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.xAxis([xAxis])](#dc.coordinateGridMixin+xAxis) ⇒ <code>d3.axis</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.elasticX([elasticX])](#dc.coordinateGridMixin+elasticX) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.xAxisPadding([padding])](#dc.coordinateGridMixin+xAxisPadding) ⇒ <code>Number</code> \| <code>String</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.xAxisPaddingUnit([unit])](#dc.coordinateGridMixin+xAxisPaddingUnit) ⇒ <code>String</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.xUnitCount()](#dc.coordinateGridMixin+xUnitCount) ⇒ <code>Number</code>
    * [.useRightYAxis([useRightYAxis])](#dc.coordinateGridMixin+useRightYAxis) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.isOrdinal()](#dc.coordinateGridMixin+isOrdinal) ⇒ <code>Boolean</code>
    * [.xAxisLabel([labelText], [padding])](#dc.coordinateGridMixin+xAxisLabel) ⇒ <code>String</code>
    * [.yAxisLabel([labelText], [padding])](#dc.coordinateGridMixin+yAxisLabel) ⇒ <code>String</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.y([yScale])](#dc.coordinateGridMixin+y) ⇒ <code>d3.scale</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.yAxis([yAxis])](#dc.coordinateGridMixin+yAxis) ⇒ <code>d3.axisLeft</code> \| <code>d3.axisRight</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.elasticY([elasticY])](#dc.coordinateGridMixin+elasticY) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.renderHorizontalGridLines([renderHorizontalGridLines])](#dc.coordinateGridMixin+renderHorizontalGridLines) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.renderVerticalGridLines([renderVerticalGridLines])](#dc.coordinateGridMixin+renderVerticalGridLines) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.xAxisMin()](#dc.coordinateGridMixin+xAxisMin) ⇒ <code>\*</code>
    * [.xAxisMax()](#dc.coordinateGridMixin+xAxisMax) ⇒ <code>\*</code>
    * [.yAxisMin()](#dc.coordinateGridMixin+yAxisMin) ⇒ <code>\*</code>
    * [.yAxisMax()](#dc.coordinateGridMixin+yAxisMax) ⇒ <code>\*</code>
    * [.yAxisPadding([padding])](#dc.coordinateGridMixin+yAxisPadding) ⇒ <code>Number</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.round([round])](#dc.coordinateGridMixin+round) ⇒ <code>function</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.brush([_])](#dc.coordinateGridMixin+brush) ⇒ <code>d3.brush</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.clipPadding([padding])](#dc.coordinateGridMixin+clipPadding) ⇒ <code>Number</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.focus([range], [noRaiseEvents])](#dc.coordinateGridMixin+focus) ⇒ <code>undefined</code>
    * [.brushOn([brushOn])](#dc.coordinateGridMixin+brushOn) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
    * [.parentBrushOn([brushOn])](#dc.coordinateGridMixin+parentBrushOn) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)

<a name="dc.coordinateGridMixin+rescale"></a>

#### coordinateGridMixin.rescale() ⇒ [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
When changing the domain of the x or y scale, it is necessary to tell the chart to recalculate
and redraw the axes. (`.rescale()` is called automatically when the x or y scale is replaced
with [.x()](dc.coordinateGridMixin+x) or [.y()](#dc.coordinateGridMixin+y), and has
no effect on elastic scales.)

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
<a name="dc.coordinateGridMixin+rangeChart"></a>

#### coordinateGridMixin.rangeChart([rangeChart]) ⇒ [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Get or set the range selection chart associated with this instance. Setting the range selection
chart using this function will automatically update its selection brush when the current chart
zooms in. In return the given range chart will also automatically attach this chart as its focus
chart hence zoom in when range brush updates.

Usually the range and focus charts will share a dimension. The range chart will set the zoom
boundaries for the focus chart, so its dimension values must be compatible with the domain of
the focus chart.

See the [Nasdaq 100 Index](http://dc-js.github.com/dc.js/) example for this effect in action.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type |
| --- | --- |
| [rangeChart] | [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin) | 

<a name="dc.coordinateGridMixin+zoomScale"></a>

#### coordinateGridMixin.zoomScale([extent]) ⇒ <code>Array.&lt;(Number\|Date)&gt;</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Get or set the scale extent for mouse zooms.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [extent] | <code>Array.&lt;(Number\|Date)&gt;</code> | <code>[1, Infinity]</code> | 

<a name="dc.coordinateGridMixin+zoomOutRestrict"></a>

#### coordinateGridMixin.zoomOutRestrict([zoomOutRestrict]) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Get or set the zoom restriction for the chart. If true limits the zoom to origional domain of the chart.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [zoomOutRestrict] | <code>Boolean</code> | <code>true</code> | 

<a name="dc.coordinateGridMixin+g"></a>

#### coordinateGridMixin.g([gElement]) ⇒ <code>SVGElement</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Get or set the root g element. This method is usually used to retrieve the g element in order to
overlay custom svg drawing programatically. **Caution**: The root g element is usually generated
by dc.js internals, and resetting it might produce unpredictable result.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type |
| --- | --- |
| [gElement] | <code>SVGElement</code> | 

<a name="dc.coordinateGridMixin+mouseZoomable"></a>

#### coordinateGridMixin.mouseZoomable([mouseZoomable]) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Set or get mouse zoom capability flag (default: false). When turned on the chart will be
zoomable using the mouse wheel. If the range selector chart is attached zooming will also update
the range selection brush on the associated range selector chart.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [mouseZoomable] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.coordinateGridMixin+chartBodyG"></a>

#### coordinateGridMixin.chartBodyG([chartBodyG]) ⇒ <code>SVGElement</code>
Retrieve the svg group for the chart body.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type |
| --- | --- |
| [chartBodyG] | <code>SVGElement</code> | 

<a name="dc.coordinateGridMixin+x"></a>

#### coordinateGridMixin.x([xScale]) ⇒ <code>d3.scale</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
**mandatory**

Get or set the x scale. The x scale can be any d3
[d3.scale](https://github.com/d3/d3-scale/blob/master/README.md) or
[ordinal scale](https://github.com/d3/d3-scale/blob/master/README.md#ordinal-scales)

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
**See**: [d3.scale](https://github.com/d3/d3-scale/blob/master/README.md)  

| Param | Type |
| --- | --- |
| [xScale] | <code>d3.scale</code> | 

**Example**  
```js
// set x to a linear scale
chart.x(d3.scaleLinear().domain([-2500, 2500]))
// set x to a time scale to generate histogram
chart.x(d3.scaleTime().domain([new Date(1985, 0, 1), new Date(2012, 11, 31)]))
```
<a name="dc.coordinateGridMixin+xUnits"></a>

#### coordinateGridMixin.xUnits([xUnits]) ⇒ <code>function</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Set or get the xUnits function. The coordinate grid chart uses the xUnits function to calculate
the number of data projections on the x axis such as the number of bars for a bar chart or the
number of dots for a line chart.

This function is expected to return a Javascript array of all data points on the x axis, or
the number of points on the axis. d3 time range functions [d3.timeDays, d3.timeMonths, and
d3.timeYears](https://github.com/d3/d3-time/blob/master/README.md#intervals) are all valid
xUnits functions.

dc.js also provides a few units function, see the [Units Namespace](#dc.units) for
a list of built-in units functions.

Note that as of dc.js 3.0, `dc.units.ordinal` is not a real function, because it is not
possible to define this function compliant with the d3 range functions. It was already a
magic value which caused charts to behave differently, and now it is completely so.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [xUnits] | <code>function</code> | <code>dc.units.integers</code> | 

**Example**  
```js
// set x units to count days
chart.xUnits(d3.timeDays);
// set x units to count months
chart.xUnits(d3.timeMonths);

// A custom xUnits function can be used as long as it follows the following interface:
// units in integer
function(start, end) {
     // simply calculates how many integers in the domain
     return Math.abs(end - start);
}

// fixed units
function(start, end) {
     // be aware using fixed units will disable the focus/zoom ability on the chart
     return 1000;
}
```
<a name="dc.coordinateGridMixin+xAxis"></a>

#### coordinateGridMixin.xAxis([xAxis]) ⇒ <code>d3.axis</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Set or get the x axis used by a particular coordinate grid chart instance. This function is most
useful when x axis customization is required. The x axis in dc.js is an instance of a
[d3 bottom axis object](https://github.com/d3/d3-axis/blob/master/README.md#axisBottom);
therefore it supports any valid d3 axisBottom manipulation.

**Caution**: The x axis is usually generated internally by dc; resetting it may cause
unexpected results. Note also that when used as a getter, this function is not chainable:
it returns the axis, not the chart,
{@link https://github.com/dc-js/dc.js/wiki/FAQ#why-does-everything-break-after-a-call-to-xaxis-or-yaxis
so attempting to call chart functions after calling `.xAxis()` will fail}.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
**See**: [d3.axisBottom](https://github.com/d3/d3-axis/blob/master/README.md#axisBottom)  

| Param | Type | Default |
| --- | --- | --- |
| [xAxis] | <code>d3.axis</code> | <code>d3.axisBottom()</code> | 

**Example**  
```js
// customize x axis tick format
chart.xAxis().tickFormat(function(v) {return v + '%';});
// customize x axis tick values
chart.xAxis().tickValues([0, 100, 200, 300]);
```
<a name="dc.coordinateGridMixin+elasticX"></a>

#### coordinateGridMixin.elasticX([elasticX]) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Turn on/off elastic x axis behavior. If x axis elasticity is turned on, then the grid chart will
attempt to recalculate the x axis range whenever a redraw event is triggered.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [elasticX] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.coordinateGridMixin+xAxisPadding"></a>

#### coordinateGridMixin.xAxisPadding([padding]) ⇒ <code>Number</code> \| <code>String</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Set or get x axis padding for the elastic x axis. The padding will be added to both end of the x
axis if elasticX is turned on; otherwise it is ignored.

Padding can be an integer or percentage in string (e.g. '10%'). Padding can be applied to
number or date x axes.  When padding a date axis, an integer represents number of units being padded
and a percentage string will be treated the same as an integer. The unit will be determined by the
xAxisPaddingUnit variable.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [padding] | <code>Number</code> \| <code>String</code> | <code>0</code> | 

<a name="dc.coordinateGridMixin+xAxisPaddingUnit"></a>

#### coordinateGridMixin.xAxisPaddingUnit([unit]) ⇒ <code>String</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Set or get x axis padding unit for the elastic x axis. The padding unit will determine which unit to
use when applying xAxis padding if elasticX is turned on and if x-axis uses a time dimension;
otherwise it is ignored.

The padding unit should be a
[d3 time interval](https://github.com/d3/d3-time/blob/master/README.md#_interval).
For backward compatibility with dc.js 2.0, it can also be the name of a d3 time interval
('day', 'hour', etc). Available arguments are the
[d3 time intervals](https://github.com/d3/d3-time/blob/master/README.md#intervals d3.timeInterval).

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [unit] | <code>String</code> | <code>d3.timeDay</code> | 

<a name="dc.coordinateGridMixin+xUnitCount"></a>

#### coordinateGridMixin.xUnitCount() ⇒ <code>Number</code>
Returns the number of units displayed on the x axis. If the x axis is ordinal (`xUnits` is
`dc.units.ordinal`), this is the number of items in the domain of the x scale. Otherwise, the
x unit count is calculated using the [xUnits](#dc.coordinateGridMixin+xUnits) function.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
<a name="dc.coordinateGridMixin+useRightYAxis"></a>

#### coordinateGridMixin.useRightYAxis([useRightYAxis]) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Gets or sets whether the chart should be drawn with a right axis instead of a left axis. When
used with a chart in a composite chart, allows both left and right Y axes to be shown on a
chart.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [useRightYAxis] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.coordinateGridMixin+isOrdinal"></a>

#### coordinateGridMixin.isOrdinal() ⇒ <code>Boolean</code>
Returns true if the chart is using ordinal xUnits ([ordinal](#dc.units.ordinal), or false
otherwise. Most charts behave differently with ordinal data and use the result of this method to
trigger the appropriate logic.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
<a name="dc.coordinateGridMixin+xAxisLabel"></a>

#### coordinateGridMixin.xAxisLabel([labelText], [padding]) ⇒ <code>String</code>
Set or get the x axis label. If setting the label, you may optionally include additional padding to
the margin to make room for the label. By default the padded is set to 12 to accomodate the text height.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [labelText] | <code>String</code> |  | 
| [padding] | <code>Number</code> | <code>12</code> | 

<a name="dc.coordinateGridMixin+yAxisLabel"></a>

#### coordinateGridMixin.yAxisLabel([labelText], [padding]) ⇒ <code>String</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Set or get the y axis label. If setting the label, you may optionally include additional padding
to the margin to make room for the label. By default the padding is set to 12 to accommodate the
text height.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [labelText] | <code>String</code> |  | 
| [padding] | <code>Number</code> | <code>12</code> | 

<a name="dc.coordinateGridMixin+y"></a>

#### coordinateGridMixin.y([yScale]) ⇒ <code>d3.scale</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Get or set the y scale. The y scale is typically automatically determined by the chart implementation.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
**See**: [d3.scale](https://github.com/d3/d3-scale/blob/master/README.md)  

| Param | Type |
| --- | --- |
| [yScale] | <code>d3.scale</code> | 

<a name="dc.coordinateGridMixin+yAxis"></a>

#### coordinateGridMixin.yAxis([yAxis]) ⇒ <code>d3.axisLeft</code> \| <code>d3.axisRight</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Set or get the y axis used by the coordinate grid chart instance. This function is most useful
when y axis customization is required. Depending on `useRightYAxis` the y axis in dc.js is an instance of
either [d3.axisLeft](https://github.com/d3/d3-axis/blob/master/README.md#axisLeft) or
[d3.axisRight](https://github.com/d3/d3-axis/blob/master/README.md#axisRight); therefore it supports any
valid d3 axis manipulation.

**Caution**: The y axis is usually generated internally by dc; resetting it may cause
unexpected results.  Note also that when used as a getter, this function is not chainable: it
returns the axis, not the chart,
{@link https://github.com/dc-js/dc.js/wiki/FAQ#why-does-everything-break-after-a-call-to-xaxis-or-yaxis
so attempting to call chart functions after calling `.yAxis()` will fail}.
In addition, depending on whether you are going to use the axis on left or right
you need to appropriately pass [d3.axisLeft](https://github.com/d3/d3-axis/blob/master/README.md#axisLeft)
or [d3.axisRight](https://github.com/d3/d3-axis/blob/master/README.md#axisRight)

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
**See**: [d3.axis](https://github.com/d3/d3-axis/blob/master/README.md)  

| Param | Type |
| --- | --- |
| [yAxis] | <code>d3.axisLeft</code> \| <code>d3.axisRight</code> | 

**Example**  
```js
// customize y axis tick format
chart.yAxis().tickFormat(function(v) {return v + '%';});
// customize y axis tick values
chart.yAxis().tickValues([0, 100, 200, 300]);
```
<a name="dc.coordinateGridMixin+elasticY"></a>

#### coordinateGridMixin.elasticY([elasticY]) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Turn on/off elastic y axis behavior. If y axis elasticity is turned on, then the grid chart will
attempt to recalculate the y axis range whenever a redraw event is triggered.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [elasticY] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.coordinateGridMixin+renderHorizontalGridLines"></a>

#### coordinateGridMixin.renderHorizontalGridLines([renderHorizontalGridLines]) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Turn on/off horizontal grid lines.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [renderHorizontalGridLines] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.coordinateGridMixin+renderVerticalGridLines"></a>

#### coordinateGridMixin.renderVerticalGridLines([renderVerticalGridLines]) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Turn on/off vertical grid lines.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [renderVerticalGridLines] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.coordinateGridMixin+xAxisMin"></a>

#### coordinateGridMixin.xAxisMin() ⇒ <code>\*</code>
Calculates the minimum x value to display in the chart. Includes xAxisPadding if set.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
<a name="dc.coordinateGridMixin+xAxisMax"></a>

#### coordinateGridMixin.xAxisMax() ⇒ <code>\*</code>
Calculates the maximum x value to display in the chart. Includes xAxisPadding if set.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
<a name="dc.coordinateGridMixin+yAxisMin"></a>

#### coordinateGridMixin.yAxisMin() ⇒ <code>\*</code>
Calculates the minimum y value to display in the chart. Includes yAxisPadding if set.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
<a name="dc.coordinateGridMixin+yAxisMax"></a>

#### coordinateGridMixin.yAxisMax() ⇒ <code>\*</code>
Calculates the maximum y value to display in the chart. Includes yAxisPadding if set.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
<a name="dc.coordinateGridMixin+yAxisPadding"></a>

#### coordinateGridMixin.yAxisPadding([padding]) ⇒ <code>Number</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Set or get y axis padding for the elastic y axis. The padding will be added to the top and
bottom of the y axis if elasticY is turned on; otherwise it is ignored.

Padding can be an integer or percentage in string (e.g. '10%'). Padding can be applied to
number or date axes. When padding a date axis, an integer represents number of days being padded
and a percentage string will be treated the same as an integer.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [padding] | <code>Number</code> \| <code>String</code> | <code>0</code> | 

<a name="dc.coordinateGridMixin+round"></a>

#### coordinateGridMixin.round([round]) ⇒ <code>function</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Set or get the rounding function used to quantize the selection when brushing is enabled.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type |
| --- | --- |
| [round] | <code>function</code> | 

**Example**  
```js
// set x unit round to by month, this will make sure range selection brush will
// select whole months
chart.round(d3.timeMonth.round);
```
<a name="dc.coordinateGridMixin+brush"></a>

#### coordinateGridMixin.brush([_]) ⇒ <code>d3.brush</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Get or set the brush. Brush must be an instance of d3 brushes
https://github.com/d3/d3-brush/blob/master/README.md
You will use this only if you are writing a new chart type that supports brushing.

**Caution**: dc creates and manages brushes internally. Go through and understand the source code
if you want to pass a new brush object. Even if you are only using the getter,
the brush object may not behave the way you expect.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type |
| --- | --- |
| [_] | <code>d3.brush</code> | 

<a name="dc.coordinateGridMixin+clipPadding"></a>

#### coordinateGridMixin.clipPadding([padding]) ⇒ <code>Number</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Get or set the padding in pixels for the clip path. Once set padding will be applied evenly to
the top, left, right, and bottom when the clip path is generated. If set to zero, the clip area
will be exactly the chart body area minus the margins.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [padding] | <code>Number</code> | <code>5</code> | 

<a name="dc.coordinateGridMixin+focus"></a>

#### coordinateGridMixin.focus([range], [noRaiseEvents]) ⇒ <code>undefined</code>
Zoom this chart to focus on the given range. The given range should be an array containing only
2 elements (`[start, end]`) defining a range in the x domain. If the range is not given or set
to null, then the zoom will be reset. _For focus to work elasticX has to be turned off;
otherwise focus will be ignored.

To avoid ping-pong volley of events between a pair of range and focus charts please set
`noRaiseEvents` to `true`. In that case it will update this chart but will not fire `zoom` event
and not try to update back the associated range chart.
If you are calling it manually - typically you will leave it to `false` (the default).

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [range] | <code>Array.&lt;Number&gt;</code> |  | 
| [noRaiseEvents] | <code>Boolean</code> | <code>false</code> | 

**Example**  
```js
chart.on('renderlet', function(chart) {
    // smooth the rendering through event throttling
    dc.events.trigger(function(){
         // focus some other chart to the range selected by user on this chart
         someOtherChart.focus(chart.filter());
    });
})
```
<a name="dc.coordinateGridMixin+brushOn"></a>

#### coordinateGridMixin.brushOn([brushOn]) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
Turn on/off the brush-based range filter. When brushing is on then user can drag the mouse
across a chart with a quantitative scale to perform range filtering based on the extent of the
brush, or click on the bars of an ordinal bar chart or slices of a pie chart to filter and
un-filter them. However turning on the brush filter will disable other interactive elements on
the chart such as highlighting, tool tips, and reference lines. Zooming will still be possible
if enabled, but only via scrolling (panning will be disabled.)

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [brushOn] | <code>Boolean</code> | <code>true</code> | 

<a name="dc.coordinateGridMixin+parentBrushOn"></a>

#### coordinateGridMixin.parentBrushOn([brushOn]) ⇒ <code>Boolean</code> \| [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)
This will be internally used by composite chart onto children. Please go not invoke directly.

**Kind**: instance method of [<code>coordinateGridMixin</code>](#dc.coordinateGridMixin)  
**Access**: protected  

| Param | Type | Default |
| --- | --- | --- |
| [brushOn] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.stackMixin"></a>

### dc.stackMixin ⇒ [<code>stackMixin</code>](#dc.stackMixin)
Stack Mixin is an mixin that provides cross-chart support of stackability using d3.stackD3v3.

**Kind**: static mixin of [<code>dc</code>](#dc)  

| Param | Type |
| --- | --- |
| _chart | <code>Object</code> | 


* [.stackMixin](#dc.stackMixin) ⇒ [<code>stackMixin</code>](#dc.stackMixin)
    * [.stack(group, [name], [accessor])](#dc.stackMixin+stack) ⇒ <code>Array.&lt;{group: crossfilter.group, name: String, accessor: function()}&gt;</code> \| [<code>stackMixin</code>](#dc.stackMixin)
    * [.hidableStacks([hidableStacks])](#dc.stackMixin+hidableStacks) ⇒ <code>Boolean</code> \| [<code>stackMixin</code>](#dc.stackMixin)
    * [.hideStack(stackName)](#dc.stackMixin+hideStack) ⇒ [<code>stackMixin</code>](#dc.stackMixin)
    * [.showStack(stackName)](#dc.stackMixin+showStack) ⇒ [<code>stackMixin</code>](#dc.stackMixin)
    * [.title([stackName], [titleAccessor])](#dc.stackMixin+title) ⇒ <code>String</code> \| [<code>stackMixin</code>](#dc.stackMixin)
    * [.stackLayout([stack])](#dc.stackMixin+stackLayout) ⇒ <code>function</code> \| [<code>stackMixin</code>](#dc.stackMixin)
    * [.evadeDomainFilter([evadeDomainFilter])](#dc.stackMixin+evadeDomainFilter) ⇒ <code>Boolean</code> \| [<code>stackMixin</code>](#dc.stackMixin)

<a name="dc.stackMixin+stack"></a>

#### stackMixin.stack(group, [name], [accessor]) ⇒ <code>Array.&lt;{group: crossfilter.group, name: String, accessor: function()}&gt;</code> \| [<code>stackMixin</code>](#dc.stackMixin)
Stack a new crossfilter group onto this chart with an optional custom value accessor. All stacks
in the same chart will share the same key accessor and therefore the same set of keys.

For example, in a stacked bar chart, the bars of each stack will be positioned using the same set
of keys on the x axis, while stacked vertically. If name is specified then it will be used to
generate the legend label.

**Kind**: instance method of [<code>stackMixin</code>](#dc.stackMixin)  
**See**: [crossfilter.group](https://github.com/crossfilter/crossfilter/wiki/API-Reference#group-map-reduce)  

| Param | Type |
| --- | --- |
| group | <code>crossfilter.group</code> | 
| [name] | <code>String</code> | 
| [accessor] | <code>function</code> | 

**Example**  
```js
// stack group using default accessor
chart.stack(valueSumGroup)
// stack group using custom accessor
.stack(avgByDayGroup, function(d){return d.value.avgByDay;});
```
<a name="dc.stackMixin+hidableStacks"></a>

#### stackMixin.hidableStacks([hidableStacks]) ⇒ <code>Boolean</code> \| [<code>stackMixin</code>](#dc.stackMixin)
Allow named stacks to be hidden or shown by clicking on legend items.
This does not affect the behavior of hideStack or showStack.

**Kind**: instance method of [<code>stackMixin</code>](#dc.stackMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [hidableStacks] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.stackMixin+hideStack"></a>

#### stackMixin.hideStack(stackName) ⇒ [<code>stackMixin</code>](#dc.stackMixin)
Hide all stacks on the chart with the given name.
The chart must be re-rendered for this change to appear.

**Kind**: instance method of [<code>stackMixin</code>](#dc.stackMixin)  

| Param | Type |
| --- | --- |
| stackName | <code>String</code> | 

<a name="dc.stackMixin+showStack"></a>

#### stackMixin.showStack(stackName) ⇒ [<code>stackMixin</code>](#dc.stackMixin)
Show all stacks on the chart with the given name.
The chart must be re-rendered for this change to appear.

**Kind**: instance method of [<code>stackMixin</code>](#dc.stackMixin)  

| Param | Type |
| --- | --- |
| stackName | <code>String</code> | 

<a name="dc.stackMixin+title"></a>

#### stackMixin.title([stackName], [titleAccessor]) ⇒ <code>String</code> \| [<code>stackMixin</code>](#dc.stackMixin)
Set or get the title function. Chart class will use this function to render svg title (usually interpreted by
browser as tooltips) for each child element in the chart, i.e. a slice in a pie chart or a bubble in a bubble chart.
Almost every chart supports title function however in grid coordinate chart you need to turn off brush in order to
use title otherwise the brush layer will block tooltip trigger.

If the first argument is a stack name, the title function will get or set the title for that stack. If stackName
is not provided, the first stack is implied.

**Kind**: instance method of [<code>stackMixin</code>](#dc.stackMixin)  

| Param | Type |
| --- | --- |
| [stackName] | <code>String</code> | 
| [titleAccessor] | <code>function</code> | 

**Example**  
```js
// set a title function on 'first stack'
chart.title('first stack', function(d) { return d.key + ': ' + d.value; });
// get a title function from 'second stack'
var secondTitleFunction = chart.title('second stack');
```
<a name="dc.stackMixin+stackLayout"></a>

#### stackMixin.stackLayout([stack]) ⇒ <code>function</code> \| [<code>stackMixin</code>](#dc.stackMixin)
Gets or sets the stack layout algorithm, which computes a baseline for each stack and
propagates it to the next.

**Kind**: instance method of [<code>stackMixin</code>](#dc.stackMixin)  
**See**: [d3.stackD3v3](https://github.com/d3/d3-3.x-api-reference/blob/master/Stack-Layout.md)  

| Param | Type | Default |
| --- | --- | --- |
| [stack] | <code>function</code> | <code>d3.stackD3v3</code> | 

<a name="dc.stackMixin+evadeDomainFilter"></a>

#### stackMixin.evadeDomainFilter([evadeDomainFilter]) ⇒ <code>Boolean</code> \| [<code>stackMixin</code>](#dc.stackMixin)
Since dc.js 2.0, there has been [an issue](https://github.com/dc-js/dc.js/issues/949)
where points are filtered to the current domain. While this is a useful optimization, it is
incorrectly implemented: the next point outside the domain is required in order to draw lines
that are clipped to the bounds, as well as bars that are partly clipped.

A fix will be included in dc.js 2.1.x, but a workaround is needed for dc.js 2.0 and until
that fix is published, so set this flag to skip any filtering of points.

Once the bug is fixed, this flag will have no effect, and it will be deprecated.

**Kind**: instance method of [<code>stackMixin</code>](#dc.stackMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [evadeDomainFilter] | <code>Boolean</code> | <code>false</code> | 

<a name="dc.capMixin"></a>

### dc.capMixin ⇒ [<code>capMixin</code>](#dc.capMixin)
Cap is a mixin that groups small data elements below a _cap_ into an *others* grouping for both the
Row and Pie Charts.

The top ordered elements in the group up to the cap amount will be kept in the chart, and the rest
will be replaced with an *others* element, with value equal to the sum of the replaced values. The
keys of the elements below the cap limit are recorded in order to filter by those keys when the
others* element is clicked.

**Kind**: static mixin of [<code>dc</code>](#dc)  

| Param | Type |
| --- | --- |
| _chart | <code>Object</code> | 


* [.capMixin](#dc.capMixin) ⇒ [<code>capMixin</code>](#dc.capMixin)
    * [.cap([count])](#dc.capMixin+cap) ⇒ <code>Number</code> \| [<code>capMixin</code>](#dc.capMixin)
    * [.takeFront([takeFront])](#dc.capMixin+takeFront) ⇒ <code>Boolean</code> \| [<code>capMixin</code>](#dc.capMixin)
    * [.othersLabel([label])](#dc.capMixin+othersLabel) ⇒ <code>String</code> \| [<code>capMixin</code>](#dc.capMixin)
    * [.othersGrouper([grouperFunction])](#dc.capMixin+othersGrouper) ⇒ <code>function</code> \| [<code>capMixin</code>](#dc.capMixin)

<a name="dc.capMixin+cap"></a>

#### capMixin.cap([count]) ⇒ <code>Number</code> \| [<code>capMixin</code>](#dc.capMixin)
Get or set the count of elements to that will be included in the cap. If there is an
[othersGrouper](#dc.capMixin+othersGrouper), any further elements will be combined in an
extra element with its name determined by [othersLabel](#dc.capMixin+othersLabel).

As of dc.js 2.1 and onward, the capped charts use
[group.all()](https://github.com/crossfilter/crossfilter/wiki/API-Reference#group_all)
and [baseMixin.ordering()](#dc.baseMixin+ordering) to determine the order of
elements. Then `cap` and [takeFront](#dc.capMixin+takeFront) determine how many elements
to keep, from which end of the resulting array.

**Migration note:** Up through dc.js 2.0.*, capping used
[group.top(N)](https://github.com/crossfilter/crossfilter/wiki/API-Reference#group_top),
which selects the largest items according to
[group.order()](https://github.com/crossfilter/crossfilter/wiki/API-Reference#group_order).
The chart then sorted the items according to [baseMixin.ordering()](#dc.baseMixin+ordering).
So the two values essentially had to agree, but if the `group.order()` was incorrect (it's
easy to forget about), the wrong rows or slices would be displayed, in the correct order.

If your chart previously relied on `group.order()`, use `chart.ordering()` instead. As of
2.1.5, the ordering defaults to sorting from greatest to least like `group.top(N)` did.

If you want to cap by one ordering but sort by another, you can still do this by
specifying your own [`.data()`](#dc.baseMixin+data) callback. For details, see the example
[Cap and Sort Differently](https://dc-js.github.io/dc.js/examples/cap-and-sort-differently.html).

**Kind**: instance method of [<code>capMixin</code>](#dc.capMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [count] | <code>Number</code> | <code>Infinity</code> | 

<a name="dc.capMixin+takeFront"></a>

#### capMixin.takeFront([takeFront]) ⇒ <code>Boolean</code> \| [<code>capMixin</code>](#dc.capMixin)
Get or set the direction of capping. If set, the chart takes the first
[cap](#dc.capMixin+cap) elements from the sorted array of elements; otherwise
it takes the last `cap` elements.

**Kind**: instance method of [<code>capMixin</code>](#dc.capMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [takeFront] | <code>Boolean</code> | <code>true</code> | 

<a name="dc.capMixin+othersLabel"></a>

#### capMixin.othersLabel([label]) ⇒ <code>String</code> \| [<code>capMixin</code>](#dc.capMixin)
Get or set the label for *Others* slice when slices cap is specified.

**Kind**: instance method of [<code>capMixin</code>](#dc.capMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [label] | <code>String</code> | <code>&quot;Others&quot;</code> | 

<a name="dc.capMixin+othersGrouper"></a>

#### capMixin.othersGrouper([grouperFunction]) ⇒ <code>function</code> \| [<code>capMixin</code>](#dc.capMixin)
Get or set the grouper function that will perform the insertion of data for the *Others* slice
if the slices cap is specified. If set to a falsy value, no others will be added.

The grouper function takes an array of included ("top") items, and an array of the rest of
the items. By default the grouper function computes the sum of the rest.

**Kind**: instance method of [<code>capMixin</code>](#dc.capMixin)  

| Param | Type |
| --- | --- |
| [grouperFunction] | <code>function</code> | 

**Example**  
```js
// Do not show others
chart.othersGrouper(null);
// Default others grouper
chart.othersGrouper(function (topItems, restItems) {
    var restItemsSum = d3.sum(restItems, _chart.valueAccessor()),
        restKeys = restItems.map(_chart.keyAccessor());
    if (restItemsSum > 0) {
        return topItems.concat([{
            others: restKeys,
            key: _chart.othersLabel(),
            value: restItemsSum
        }]);
    }
    return topItems;
});
```
<a name="dc.bubbleMixin"></a>

### dc.bubbleMixin ⇒ [<code>bubbleMixin</code>](#dc.bubbleMixin)
This Mixin provides reusable functionalities for any chart that needs to visualize data using bubbles.

**Kind**: static mixin of [<code>dc</code>](#dc)  
**Mixes**: [<code>colorMixin</code>](#dc.colorMixin)  

| Param | Type |
| --- | --- |
| _chart | <code>Object</code> | 


* [.bubbleMixin](#dc.bubbleMixin) ⇒ [<code>bubbleMixin</code>](#dc.bubbleMixin)
    * [.r([bubbleRadiusScale])](#dc.bubbleMixin+r) ⇒ <code>d3.scale</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
    * [.radiusValueAccessor([radiusValueAccessor])](#dc.bubbleMixin+radiusValueAccessor) ⇒ <code>function</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
    * [.minRadius([radius])](#dc.bubbleMixin+minRadius) ⇒ <code>Number</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
    * [.minRadiusWithLabel([radius])](#dc.bubbleMixin+minRadiusWithLabel) ⇒ <code>Number</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
    * [.maxBubbleRelativeSize([relativeSize])](#dc.bubbleMixin+maxBubbleRelativeSize) ⇒ <code>Number</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)

<a name="dc.bubbleMixin+r"></a>

#### bubbleMixin.r([bubbleRadiusScale]) ⇒ <code>d3.scale</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
Get or set the bubble radius scale. By default the bubble chart uses
[d3.scaleLinear().domain([0, 100])](https://github.com/d3/d3-scale/blob/master/README.md#scaleLinear)
as its radius scale.

**Kind**: instance method of [<code>bubbleMixin</code>](#dc.bubbleMixin)  
**See**: [d3.scale](https://github.com/d3/d3-scale/blob/master/README.md)  

| Param | Type | Default |
| --- | --- | --- |
| [bubbleRadiusScale] | <code>d3.scale</code> | <code>d3.scaleLinear().domain([0, 100])</code> | 

<a name="dc.bubbleMixin+radiusValueAccessor"></a>

#### bubbleMixin.radiusValueAccessor([radiusValueAccessor]) ⇒ <code>function</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
Get or set the radius value accessor function. If set, the radius value accessor function will
be used to retrieve a data value for each bubble. The data retrieved then will be mapped using
the r scale to the actual bubble radius. This allows you to encode a data dimension using bubble
size.

**Kind**: instance method of [<code>bubbleMixin</code>](#dc.bubbleMixin)  

| Param | Type |
| --- | --- |
| [radiusValueAccessor] | <code>function</code> | 

<a name="dc.bubbleMixin+minRadius"></a>

#### bubbleMixin.minRadius([radius]) ⇒ <code>Number</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
Get or set the minimum radius. This will be used to initialize the radius scale's range.

**Kind**: instance method of [<code>bubbleMixin</code>](#dc.bubbleMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [radius] | <code>Number</code> | <code>10</code> | 

<a name="dc.bubbleMixin+minRadiusWithLabel"></a>

#### bubbleMixin.minRadiusWithLabel([radius]) ⇒ <code>Number</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
Get or set the minimum radius for label rendering. If a bubble's radius is less than this value
then no label will be rendered.

**Kind**: instance method of [<code>bubbleMixin</code>](#dc.bubbleMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [radius] | <code>Number</code> | <code>10</code> | 

<a name="dc.bubbleMixin+maxBubbleRelativeSize"></a>

#### bubbleMixin.maxBubbleRelativeSize([relativeSize]) ⇒ <code>Number</code> \| [<code>bubbleMixin</code>](#dc.bubbleMixin)
Get or set the maximum relative size of a bubble to the length of x axis. This value is useful
when the difference in radius between bubbles is too great.

**Kind**: instance method of [<code>bubbleMixin</code>](#dc.bubbleMixin)  

| Param | Type | Default |
| --- | --- | --- |
| [relativeSize] | <code>Number</code> | <code>0.3</code> | 

<a name="dc.disableTransitions"></a>

### dc.disableTransitions : <code>Boolean</code>
If this boolean is set truthy, all transitions will be disabled, and changes to the charts will happen
immediately.

**Kind**: static property of [<code>dc</code>](#dc)  
**Default**: <code>false</code>  
<a name="dc.dateFormat"></a>

### dc.dateFormat : <code>function</code>
The default date format for dc.js

**Kind**: static property of [<code>dc</code>](#dc)  
**Default**: <code>d3.timeFormat(&#x27;%m/%d/%Y&#x27;)</code>  
<a name="dc.chartRegistry"></a>

### dc.chartRegistry : <code>object</code>
The dc.chartRegistry object maintains sets of all instantiated dc.js charts under named groups
and the default group.

A chart group often corresponds to a crossfilter instance. It specifies
the set of charts which should be updated when a filter changes on one of the charts or when the
global functions [filterAll](#dc.filterAll), [refocusAll](#dc.refocusAll),
[renderAll](#dc.renderAll), [redrawAll](#dc.redrawAll), or chart functions
[baseMixin.renderGroup](#dc.baseMixin+renderGroup),
[baseMixin.redrawGroup](#dc.baseMixin+redrawGroup) are called.

**Kind**: static namespace of [<code>dc</code>](#dc)  

* [.chartRegistry](#dc.chartRegistry) : <code>object</code>
    * [.has(chart)](#dc.chartRegistry.has) ⇒ <code>Boolean</code>
    * [.register(chart, [group])](#dc.chartRegistry.register) ⇒ <code>undefined</code>
    * [.deregister(chart, [group])](#dc.chartRegistry.deregister) ⇒ <code>undefined</code>
    * [.clear(group)](#dc.chartRegistry.clear) ⇒ <code>undefined</code>
    * [.list([group])](#dc.chartRegistry.list) ⇒ <code>Array.&lt;Object&gt;</code>

<a name="dc.chartRegistry.has"></a>

#### chartRegistry.has(chart) ⇒ <code>Boolean</code>
Determine if a given chart instance resides in any group in the registry.

**Kind**: static method of [<code>chartRegistry</code>](#dc.chartRegistry)  

| Param | Type | Description |
| --- | --- | --- |
| chart | <code>Object</code> | dc.js chart instance |

<a name="dc.chartRegistry.register"></a>

#### chartRegistry.register(chart, [group]) ⇒ <code>undefined</code>
Add given chart instance to the given group, creating the group if necessary.
If no group is provided, the default group `dc.constants.DEFAULT_CHART_GROUP` will be used.

**Kind**: static method of [<code>chartRegistry</code>](#dc.chartRegistry)  

| Param | Type | Description |
| --- | --- | --- |
| chart | <code>Object</code> | dc.js chart instance |
| [group] | <code>String</code> | Group name |

<a name="dc.chartRegistry.deregister"></a>

#### chartRegistry.deregister(chart, [group]) ⇒ <code>undefined</code>
Remove given chart instance from the given group, creating the group if necessary.
If no group is provided, the default group `dc.constants.DEFAULT_CHART_GROUP` will be used.

**Kind**: static method of [<code>chartRegistry</code>](#dc.chartRegistry)  

| Param | Type | Description |
| --- | --- | --- |
| chart | <code>Object</code> | dc.js chart instance |
| [group] | <code>String</code> | Group name |

<a name="dc.chartRegistry.clear"></a>

#### chartRegistry.clear(group) ⇒ <code>undefined</code>
Clear given group if one is provided, otherwise clears all groups.

**Kind**: static method of [<code>chartRegistry</code>](#dc.chartRegistry)  

| Param | Type | Description |
| --- | --- | --- |
| group | <code>String</code> | Group name |

<a name="dc.chartRegistry.list"></a>

#### chartRegistry.list([group]) ⇒ <code>Array.&lt;Object&gt;</code>
Get an array of each chart instance in the given group.
If no group is provided, the charts in the default group are returned.

**Kind**: static method of [<code>chartRegistry</code>](#dc.chartRegistry)  

| Param | Type | Description |
| --- | --- | --- |
| [group] | <code>String</code> | Group name |

<a name="dc.units"></a>

### dc.units : <code>object</code>
**Kind**: static namespace of [<code>dc</code>](#dc)  

* [.units](#dc.units) : <code>object</code>
    * [.fp](#dc.units.fp) : <code>object</code>
        * [.precision(precision)](#dc.units.fp.precision) ⇒ <code>function</code>
    * [.integers(start, end)](#dc.units.integers) ⇒ <code>Number</code>
    * [.ordinal()](#dc.units.ordinal) ⇒ <code>uncallable</code>

<a name="dc.units.fp"></a>

#### units.fp : <code>object</code>
**Kind**: static namespace of [<code>units</code>](#dc.units)  
<a name="dc.units.fp.precision"></a>

##### fp.precision(precision) ⇒ <code>function</code>
This function generates an argument for the [Coordinate Grid Chart](#dc.coordinateGridMixin)
[.xUnits](#dc.coordinateGridMixin+xUnits) function specifying that the x values are floating-point
numbers with the given precision.
The returned function determines how many values at the given precision will fit into the range
supplied in its start and end parameters.

**Kind**: static method of [<code>fp</code>](#dc.units.fp)  
**Returns**: <code>function</code> - start-end unit function  
**See**: [coordinateGridMixin.xUnits](#dc.coordinateGridMixin+xUnits)  

| Param | Type |
| --- | --- |
| precision | <code>Number</code> | 

**Example**  
```js
// specify values (and ticks) every 0.1 units
chart.xUnits(dc.units.fp.precision(0.1)
// there are 500 units between 0.5 and 1 if the precision is 0.001
var thousandths = dc.units.fp.precision(0.001);
thousandths(0.5, 1.0) // returns 500
```
<a name="dc.units.integers"></a>

#### units.integers(start, end) ⇒ <code>Number</code>
The default value for [.xUnits](#dc.coordinateGridMixin+xUnits) for the
[Coordinate Grid Chart](#dc.coordinateGridMixin) and should
be used when the x values are a sequence of integers.
It is a function that counts the number of integers in the range supplied in its start and end parameters.

**Kind**: static method of [<code>units</code>](#dc.units)  
**See**: [coordinateGridMixin.xUnits](#dc.coordinateGridMixin+xUnits)  

| Param | Type |
| --- | --- |
| start | <code>Number</code> | 
| end | <code>Number</code> | 

**Example**  
```js
chart.xUnits(dc.units.integers) // already the default
```
<a name="dc.units.ordinal"></a>

#### units.ordinal() ⇒ <code>uncallable</code>
This argument can be passed to the [.xUnits](#dc.coordinateGridMixin+xUnits) function of a
coordinate grid chart to specify ordinal units for the x axis. Usually this parameter is used in
combination with passing
[d3.scaleOrdinal](https://github.com/d3/d3-scale/blob/master/README.md#ordinal-scales)
to [.x](#dc.coordinateGridMixin+x).

As of dc.js 3.0, this is purely a placeholder or magic value which causes the chart to go into ordinal mode; the
function is not called.

**Kind**: static method of [<code>units</code>](#dc.units)  
**See**

- [d3.scaleOrdinal](https://github.com/d3/d3-scale/blob/master/README.md#ordinal-scales)
- [coordinateGridMixin.xUnits](#dc.coordinateGridMixin+xUnits)
- [coordinateGridMixin.x](#dc.coordinateGridMixin+x)

**Example**  
```js
chart.xUnits(dc.units.ordinal)
     .x(d3.scaleOrdinal())
```
<a name="dc.printers"></a>

### dc.printers : <code>object</code>
**Kind**: static namespace of [<code>dc</code>](#dc)  

* [.printers](#dc.printers) : <code>object</code>
    * [.filters(filters)](#dc.printers.filters) ⇒ <code>String</code>
    * [.filter(filter)](#dc.printers.filter) ⇒ <code>String</code>

<a name="dc.printers.filters"></a>

#### printers.filters(filters) ⇒ <code>String</code>
Converts a list of filters into a readable string.

**Kind**: static method of [<code>printers</code>](#dc.printers)  

| Param | Type |
| --- | --- |
| filters | [<code>Array.&lt;filters&gt;</code>](#dc.filters) | 

<a name="dc.printers.filter"></a>

#### printers.filter(filter) ⇒ <code>String</code>
Converts a filter into a readable string.

**Kind**: static method of [<code>printers</code>](#dc.printers)  

| Param | Type |
| --- | --- |
| filter | [<code>filters</code>](#dc.filters) \| <code>any</code> \| <code>Array.&lt;any&gt;</code> | 

<a name="dc.utils"></a>

### dc.utils : <code>object</code>
**Kind**: static namespace of [<code>dc</code>](#dc)  

* [.utils](#dc.utils) : <code>object</code>
    * [.printSingleValue(filter)](#dc.utils.printSingleValue) ⇒ <code>String</code>
    * [.add(l, r, [t])](#dc.utils.add) ⇒ <code>Date</code> \| <code>Number</code>
    * [.subtract(l, r, [t])](#dc.utils.subtract) ⇒ <code>Date</code> \| <code>Number</code>
    * [.isNumber(n)](#dc.utils.isNumber) ⇒ <code>Boolean</code>
    * [.isFloat(n)](#dc.utils.isFloat) ⇒ <code>Boolean</code>
    * [.isInteger(n)](#dc.utils.isInteger) ⇒ <code>Boolean</code>
    * [.isNegligible(n)](#dc.utils.isNegligible) ⇒ <code>Boolean</code>
    * [.clamp(val, min, max)](#dc.utils.clamp) ⇒ <code>any</code>
    * [.constant(x)](#dc.utils.constant) ⇒ <code>function</code>
    * [.uniqueId()](#dc.utils.uniqueId) ⇒ <code>Number</code>
    * [.nameToId(name)](#dc.utils.nameToId) ⇒ <code>String</code>
    * [.appendOrSelect(parent, selector, tag)](#dc.utils.appendOrSelect) ⇒ <code>d3.selection</code>
    * [.safeNumber(n)](#dc.utils.safeNumber) ⇒ <code>Number</code>
    * [.arraysEqual(a1, a2)](#dc.utils.arraysEqual) ⇒ <code>Boolean</code>

<a name="dc.utils.printSingleValue"></a>

#### utils.printSingleValue(filter) ⇒ <code>String</code>
Print a single value filter.

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type |
| --- | --- |
| filter | <code>any</code> | 

<a name="dc.utils.add"></a>

#### utils.add(l, r, [t]) ⇒ <code>Date</code> \| <code>Number</code>
Arbitrary add one value to another.

If the value l is of type Date, adds r units to it. t becomes the unit.
For example dc.utils.add(dt, 3, 'week') will add 3 (r = 3) weeks (t= 'week') to dt.

If l is of type numeric, t is ignored. In this case if r is of type string,
it is assumed to be percentage (whether or not it includes %). For example
dc.utils.add(30, 10) will give 40 and dc.utils.add(30, '10') will give 33.

They also generate strange results if l is a string.

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| l | <code>Date</code> \| <code>Number</code> |  | the value to modify |
| r | <code>String</code> \| <code>Number</code> |  | the amount by which to modify the value |
| [t] | <code>function</code> \| <code>String</code> | <code>d3.timeDay</code> | if `l` is a `Date`, then this should be a [d3 time interval](https://github.com/d3/d3-time/blob/master/README.md#_interval). For backward compatibility with dc.js 2.0, it can also be the name of an interval, i.e. 'millis', 'second', 'minute', 'hour', 'day', 'week', 'month', or 'year' |

<a name="dc.utils.subtract"></a>

#### utils.subtract(l, r, [t]) ⇒ <code>Date</code> \| <code>Number</code>
Arbitrary subtract one value from another.

If the value l is of type Date, subtracts r units from it. t becomes the unit.
For example dc.utils.subtract(dt, 3, 'week') will subtract 3 (r = 3) weeks (t= 'week') from dt.

If l is of type numeric, t is ignored. In this case if r is of type string,
it is assumed to be percentage (whether or not it includes %). For example
dc.utils.subtract(30, 10) will give 20 and dc.utils.subtract(30, '10') will give 27.

They also generate strange results if l is a string.

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| l | <code>Date</code> \| <code>Number</code> |  | the value to modify |
| r | <code>String</code> \| <code>Number</code> |  | the amount by which to modify the value |
| [t] | <code>function</code> \| <code>String</code> | <code>d3.timeDay</code> | if `l` is a `Date`, then this should be a [d3 time interval](https://github.com/d3/d3-time/blob/master/README.md#_interval). For backward compatibility with dc.js 2.0, it can also be the name of an interval, i.e. 'millis', 'second', 'minute', 'hour', 'day', 'week', 'month', or 'year' |

<a name="dc.utils.isNumber"></a>

#### utils.isNumber(n) ⇒ <code>Boolean</code>
Is the value a number?

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type |
| --- | --- |
| n | <code>any</code> | 

<a name="dc.utils.isFloat"></a>

#### utils.isFloat(n) ⇒ <code>Boolean</code>
Is the value a float?

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type |
| --- | --- |
| n | <code>any</code> | 

<a name="dc.utils.isInteger"></a>

#### utils.isInteger(n) ⇒ <code>Boolean</code>
Is the value an integer?

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type |
| --- | --- |
| n | <code>any</code> | 

<a name="dc.utils.isNegligible"></a>

#### utils.isNegligible(n) ⇒ <code>Boolean</code>
Is the value very close to zero?

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type |
| --- | --- |
| n | <code>any</code> | 

<a name="dc.utils.clamp"></a>

#### utils.clamp(val, min, max) ⇒ <code>any</code>
Ensure the value is no greater or less than the min/max values.  If it is return the boundary value.

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type |
| --- | --- |
| val | <code>any</code> | 
| min | <code>any</code> | 
| max | <code>any</code> | 

<a name="dc.utils.constant"></a>

#### utils.constant(x) ⇒ <code>function</code>
Given `x`, return a function that always returns `x`.

[`d3.functor` was removed in d3 version 4](https://github.com/d3/d3/blob/master/CHANGES.md#internals).
This function helps to implement the replacement,
`typeof x === "function" ? x : dc.utils.constant(x)`

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type |
| --- | --- |
| x | <code>any</code> | 

<a name="dc.utils.uniqueId"></a>

#### utils.uniqueId() ⇒ <code>Number</code>
Using a simple static counter, provide a unique integer id.

**Kind**: static method of [<code>utils</code>](#dc.utils)  
<a name="dc.utils.nameToId"></a>

#### utils.nameToId(name) ⇒ <code>String</code>
Convert a name to an ID.

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type |
| --- | --- |
| name | <code>String</code> | 

<a name="dc.utils.appendOrSelect"></a>

#### utils.appendOrSelect(parent, selector, tag) ⇒ <code>d3.selection</code>
Append or select an item on a parent element.

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type |
| --- | --- |
| parent | <code>d3.selection</code> | 
| selector | <code>String</code> | 
| tag | <code>String</code> | 

<a name="dc.utils.safeNumber"></a>

#### utils.safeNumber(n) ⇒ <code>Number</code>
Return the number if the value is a number; else 0.

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type |
| --- | --- |
| n | <code>Number</code> \| <code>any</code> | 

<a name="dc.utils.arraysEqual"></a>

#### utils.arraysEqual(a1, a2) ⇒ <code>Boolean</code>
Return true if both arrays are equal, if both array are null these are considered equal

**Kind**: static method of [<code>utils</code>](#dc.utils)  

| Param | Type |
| --- | --- |
| a1 | <code>Array</code> \| <code>null</code> | 
| a2 | <code>Array</code> \| <code>null</code> | 

<a name="dc.filters"></a>

### dc.filters : <code>object</code>
The dc.js filters are functions which are passed into crossfilter to chose which records will be
accumulated to produce values for the charts.  In the crossfilter model, any filters applied on one
dimension will affect all the other dimensions but not that one.  dc always applies a filter
function to the dimension; the function combines multiple filters and if any of them accept a
record, it is filtered in.

These filter constructors are used as appropriate by the various charts to implement brushing.  We
mention below which chart uses which filter.  In some cases, many instances of a filter will be added.

Each of the dc.js filters is an object with the following properties:
* `isFiltered` - a function that returns true if a value is within the filter
* `filterType` - a string identifying the filter, here the name of the constructor

Currently these filter objects are also arrays, but this is not a requirement. Custom filters
can be used as long as they have the properties above.

**Kind**: static namespace of [<code>dc</code>](#dc)  

* [.filters](#dc.filters) : <code>object</code>
    * [.RangedFilter](#dc.filters.RangedFilter)
        * [new RangedFilter(low, high)](#new_dc.filters.RangedFilter_new)
    * [.TwoDimensionalFilter](#dc.filters.TwoDimensionalFilter)
        * [new TwoDimensionalFilter(filter)](#new_dc.filters.TwoDimensionalFilter_new)
    * [.RangedTwoDimensionalFilter](#dc.filters.RangedTwoDimensionalFilter)
        * [new RangedTwoDimensionalFilter(filter)](#new_dc.filters.RangedTwoDimensionalFilter_new)
    * [.HierarchyFilter](#dc.filters.HierarchyFilter)
        * [new HierarchyFilter(path)](#new_dc.filters.HierarchyFilter_new)

<a name="dc.filters.RangedFilter"></a>

#### filters.RangedFilter
**Kind**: static class of [<code>filters</code>](#dc.filters)  
<a name="new_dc.filters.RangedFilter_new"></a>

##### new RangedFilter(low, high)
RangedFilter is a filter which accepts keys between `low` and `high`.  It is used to implement X
axis brushing for the [coordinate grid charts](#dc.coordinateGridMixin).

Its `filterType` is 'RangedFilter'


| Param | Type |
| --- | --- |
| low | <code>Number</code> | 
| high | <code>Number</code> | 

<a name="dc.filters.TwoDimensionalFilter"></a>

#### filters.TwoDimensionalFilter
**Kind**: static class of [<code>filters</code>](#dc.filters)  
<a name="new_dc.filters.TwoDimensionalFilter_new"></a>

##### new TwoDimensionalFilter(filter)
TwoDimensionalFilter is a filter which accepts a single two-dimensional value.  It is used by the
[heat map chart](#dc.heatMap) to include particular cells as they are clicked.  (Rows and columns are
filtered by filtering all the cells in the row or column.)

Its `filterType` is 'TwoDimensionalFilter'


| Param | Type |
| --- | --- |
| filter | <code>Array.&lt;Number&gt;</code> | 

<a name="dc.filters.RangedTwoDimensionalFilter"></a>

#### filters.RangedTwoDimensionalFilter
**Kind**: static class of [<code>filters</code>](#dc.filters)  
<a name="new_dc.filters.RangedTwoDimensionalFilter_new"></a>

##### new RangedTwoDimensionalFilter(filter)
The RangedTwoDimensionalFilter allows filtering all values which fit within a rectangular
region. It is used by the [scatter plot](#dc.scatterPlot) to implement rectangular brushing.

It takes two two-dimensional points in the form `[[x1,y1],[x2,y2]]`, and normalizes them so that
`x1 <= x2` and `y1 <= y2`. It then returns a filter which accepts any points which are in the
rectangular range including the lower values but excluding the higher values.

If an array of two values are given to the RangedTwoDimensionalFilter, it interprets the values as
two x coordinates `x1` and `x2` and returns a filter which accepts any points for which `x1 <= x <
x2`.

Its `filterType` is 'RangedTwoDimensionalFilter'


| Param | Type |
| --- | --- |
| filter | <code>Array.&lt;Array.&lt;Number&gt;&gt;</code> | 

<a name="dc.filters.HierarchyFilter"></a>

#### filters.HierarchyFilter
**Kind**: static class of [<code>filters</code>](#dc.filters)  
<a name="new_dc.filters.HierarchyFilter_new"></a>

##### new HierarchyFilter(path)
HierarchyFilter is a filter which accepts a key path as an array. It matches any node at, or
child of, the given path. It is used by the [sunburst chart](#dc.sunburstChart) to include particular cells and all
their children as they are clicked.


| Param | Type |
| --- | --- |
| path | <code>String</code> | 

<a name="dc.registerChart"></a>

### dc.registerChart(chart, [group]) ⇒ <code>undefined</code>
Add given chart instance to the given group, creating the group if necessary.
If no group is provided, the default group `dc.constants.DEFAULT_CHART_GROUP` will be used.

**Kind**: static method of [<code>dc</code>](#dc)  

| Param | Type | Description |
| --- | --- | --- |
| chart | <code>Object</code> | dc.js chart instance |
| [group] | <code>String</code> | Group name |

<a name="dc.deregisterChart"></a>

### dc.deregisterChart(chart, [group]) ⇒ <code>undefined</code>
Remove given chart instance from the given group, creating the group if necessary.
If no group is provided, the default group `dc.constants.DEFAULT_CHART_GROUP` will be used.

**Kind**: static method of [<code>dc</code>](#dc)  

| Param | Type | Description |
| --- | --- | --- |
| chart | <code>Object</code> | dc.js chart instance |
| [group] | <code>String</code> | Group name |

<a name="dc.hasChart"></a>

### dc.hasChart(chart) ⇒ <code>Boolean</code>
Determine if a given chart instance resides in any group in the registry.

**Kind**: static method of [<code>dc</code>](#dc)  

| Param | Type | Description |
| --- | --- | --- |
| chart | <code>Object</code> | dc.js chart instance |

<a name="dc.deregisterAllCharts"></a>

### dc.deregisterAllCharts(group) ⇒ <code>undefined</code>
Clear given group if one is provided, otherwise clears all groups.

**Kind**: static method of [<code>dc</code>](#dc)  

| Param | Type | Description |
| --- | --- | --- |
| group | <code>String</code> | Group name |

<a name="dc.filterAll"></a>

### dc.filterAll([group]) ⇒ <code>undefined</code>
Clear all filters on all charts within the given chart group. If the chart group is not given then
only charts that belong to the default chart group will be reset.

**Kind**: static method of [<code>dc</code>](#dc)  

| Param | Type |
| --- | --- |
| [group] | <code>String</code> | 

<a name="dc.refocusAll"></a>

### dc.refocusAll([group]) ⇒ <code>undefined</code>
Reset zoom level / focus on all charts that belong to the given chart group. If the chart group is
not given then only charts that belong to the default chart group will be reset.

**Kind**: static method of [<code>dc</code>](#dc)  

| Param | Type |
| --- | --- |
| [group] | <code>String</code> | 

<a name="dc.renderAll"></a>

### dc.renderAll([group]) ⇒ <code>undefined</code>
Re-render all charts belong to the given chart group. If the chart group is not given then only
charts that belong to the default chart group will be re-rendered.

**Kind**: static method of [<code>dc</code>](#dc)  

| Param | Type |
| --- | --- |
| [group] | <code>String</code> | 

<a name="dc.redrawAll"></a>

### dc.redrawAll([group]) ⇒ <code>undefined</code>
Redraw all charts belong to the given chart group. If the chart group is not given then only charts
that belong to the default chart group will be re-drawn. Redraw is different from re-render since
when redrawing dc tries to update the graphic incrementally, using transitions, instead of starting
from scratch.

**Kind**: static method of [<code>dc</code>](#dc)  

| Param | Type |
| --- | --- |
| [group] | <code>String</code> | 

<a name="dc.transition"></a>

### dc.transition(selection, [duration], [delay], [name]) ⇒ <code>d3.transition</code> \| <code>d3.selection</code>
Start a transition on a selection if transitions are globally enabled
([disableTransitions](#dc.disableTransitions) is false) and the duration is greater than zero; otherwise return
the selection. Since most operations are the same on a d3 selection and a d3 transition, this
allows a common code path for both cases.

**Kind**: static method of [<code>dc</code>](#dc)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| selection | <code>d3.selection</code> |  | the selection to be transitioned |
| [duration] | <code>Number</code> \| <code>function</code> | <code>250</code> | the duration of the transition in milliseconds, a function returning the duration, or 0 for no transition |
| [delay] | <code>Number</code> \| <code>function</code> |  | the delay of the transition in milliseconds, or a function returning the delay, or 0 for no delay |
| [name] | <code>String</code> |  | the name of the transition (if concurrent transitions on the same elements are needed) |

<a name="dc.pluck"></a>

### dc.pluck(n, [f]) ⇒ <code>function</code>
Returns a function that given a string property name, can be used to pluck the property off an object.  A function
can be passed as the second argument to also alter the data being returned.

This can be a useful shorthand method to create accessor functions.

**Kind**: static method of [<code>dc</code>](#dc)  

| Param | Type |
| --- | --- |
| n | <code>String</code> | 
| [f] | <code>function</code> | 

**Example**  
```js
var xPluck = dc.pluck('x');
var objA = {x: 1};
xPluck(objA) // 1
```
**Example**  
```js
var xPosition = dc.pluck('x', function (x, i) {
    // `this` is the original datum,
    // `x` is the x property of the datum,
    // `i` is the position in the array
    return this.radius + x;
});
dc.selectAll('.circle').data(...).x(xPosition);
```

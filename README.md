## Angular snippets for Sublime Text
some snippet for sublime
## Installation
- Package Control : install package 'Angular snippets FN'
- Manual: download the zip file and decompression in the package directory

## Snippets
**ngctrl**
```javascript
(function(){
    var module, moduleName = '${1: ngModule}',
        ctrlName = '${2: controllerName}';
    try{
        module = angular.module(moduleName, []);
    }catch(e){
        module = angular.module(moduleName)
    }

    module.controller(ctrlName, ${2: controllerName});

    function ${2: controllerName}{
        ${3:}
    }

})();
```
**ngdirect**
```javascript
(function(){
    var module, moduleName = '${1: ngModule}',
        factoryName = '${2: directiveName}';
    try{
        module = angular.module(moduleName, []);
    }catch(e){
        module = angular.module(moduleName)
    }
    
    module.directive(factoryName, ${2: directiveName});

    function ${2: directiveName}{
        ${3:}
    }

})();
```
**ngfac**
```javascript
(function(){
    var module, moduleName = '${1: ngModule}',
        factoryName = '${2: factoryName}';
    try{
        module = angular.module(moduleName, []);
    }catch(e){
        module = angular.module(moduleName)
    }
    
    module.factory(factoryName, ${2: factoryName});

    function ${2: factoryName}{
        ${3:}
    }

})();
```

**nglist** 
```html
<div class="row content-scetion">
    <div class="col-sm-2">
    </div>

    <div class="col-sm-8">
        <form novalidate class="col-sm-8" name="searchForm">
            <div class="input-group">
                <input type="text" class="form-control" name="mobile" placeholder="输入内容标题关键词进行搜索" ng-model="ctrl.keyword">
                <span class="input-group-btn">
                    <button class="btn btn-primary" ng-click="ctrl.search()">
                        <span class="glyphicon glyphicon-search"></span>
                    </button>
                </span>
            </div>
        </form>
    </div>
    <div class="col-sm-2 text-right">
        <div class="btn-group">
            <button class="btn btn-warning" ng-click="$dismiss()">关闭</button>
        </div>
    </div>
</div>
<div class="table-responsive content-scetion">
    <table table-thead-fixed class="table table-hover table-certificates">
        <thead>
            <tr>
                <th>标题</th>
                <th>类别</th>
                <th>操作</th>
            </tr>
        </thead>
        <tbody>
            <tr current-page="paginationOptions.currentPage" total-items="paginationOptions.count" dir-paginate="items in series.list | itemsPerPage:paginationOptions.pageSize">
                <td>{{items.title}}</td>
                <td>{{items.newsType | newsDetailType}}</td>
                <td><a ng-click="series.select(items)">选取</a></td>
            </tr>
        </tbody>
    </table>
    <div>
        <dir-pagination-controls max-size="10" direction-links="true" on-page-change="search()" boundary-links="false" class="pull-right"></dir-pagination-controls>
    </div>
</div>
```

**ngmodal**
```html
<div class="modal-header">
    <h3></h3>
</div>

<div class="modal-body clearfix">
    <div class="form-horizontal">
        <div class="form-group">
            <label for="" class="col-sm-2 control-label">卡片类型：</label>
            <div class="col-sm-10">
                <select class="col-lg-12 form-control" ng-model="ctrl.cardType" ng-options="k as v for (k, v) in ctrl.cardTypes">
                    <option value="">请选择</option>
                </select>
            </div>
        </div>
    </div>
</div>

<div class="modal-footer">
    <button class="btn btn-success" type="button">确认</button>
    <button class="btn btn-default" type="button" ng-click="\$dismiss()">取消</button>
</div>
```

> in html, it won't prompt the snippet
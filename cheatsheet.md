## Thingsboard Widgets Cheatsheet

### Add Data to Timeseries

Swagger UI: https://thingsboard.cloud/swagger-ui.html#!/telemetry-controller/saveEntityTelemetryUsingPOST

Thingsboard Source:  

class AttributeService  
Method:

```javascript
  public saveEntityAttributes(entityId: EntityId, attributeScope: AttributeScope, attributes: Array<AttributeData>,
                              config?: RequestConfig): Observable<any>
```

Example:                              
       
```javascript                 
var attributeService = self.ctx.attributeService;
var entityId = self.ctx.datasources[0].entityId;
var entity = {
	    entityType: 'DEVICE',
	    id: entityId
	}
attributeService.saveEntityTimeseries(entity, 'CLIENT_SCOPE', [{key: 'BatteryLevel', value: 375}]).subscribe((responseBody) => {
    console.log(responseBody);
}); 
``` 

### Add Data to Attributes

```javascript
var attributeService = self.ctx.attributeService;
        var entityId = self.ctx.datasources[0].entityId;
        var entityType = self.ctx.datasources[0].entityType;
        var key = self.ctx.datasources[0].dataKeys[0].name;
        var entity = {
        	    entityType: entityType,     //DEVICE
        	    id: entityId
        	}
    
        	console.log (entityId)
        	var containerType = $('#containerType  option:selected', self.ctx.$container).val()
        	
        attributeService.saveEntityAttributes(entity, 'SERVER_SCOPE', [{key: 'Container type', value: containerType  }]).subscribe((responseBody) => {
            console.log(responseBody);
}); 
``` 
                                    
### Scale Widgets (Alternative to Zoom)

```html
<div id="outer" style="transform: scale(1); transform-origin: 0% 0% 0px;">
```

```javascript
$('#outer', self.ctx.$container)[0].style.transform =  "scale(" + (self.ctx.width / 190) + ")";
```

### For Latest Telemetry Widget limit Datasource to 1

https://thingsboard.io/docs/user-guide/contribution/widgets-development/#type-parameters-object

```javascript
self.typeParameters = function() {
    return {
        maxDatasources: 1,
        maxDataKeys: 1,
        singleEntity: true
    };
}
```
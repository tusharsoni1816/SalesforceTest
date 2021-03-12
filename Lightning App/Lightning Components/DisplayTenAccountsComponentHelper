({
	queryAccountRecords : function(component, event, helper) {
        
        component.set('v.columns', [
            {label: 'Account Name', fieldName: 'Name', type: 'text'},
            {label: 'Phone', fieldName: 'Phone', type: 'phone'},
            {label: 'Type', fieldName: 'Type', type: 'text'}, 
            {label: 'Industry', fieldName: 'Industry', type: 'text'}
        ]);
        
        
		var action = component.get("c.getAccountRecords");
        action.setParams({
        });
        
        action.setCallback(this, function(response){
            var state = response.getState();
            console.log("response", response.getReturnValue());
            if (state === "SUCCESS") {
                var rows = response.getReturnValue();
                component.set("v.data", rows);
            }
        });
        $A.enqueueAction(action);
	}
})

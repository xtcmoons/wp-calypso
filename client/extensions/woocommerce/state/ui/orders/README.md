UI Orders
=========

This module is used to manage state for the UI of the orders sections. This includes which filters are in effect for the list view.

## Actions

### `updateCurrentOrdersQuery( siteId: number, query: object )`

Update the query used to display the orders list - ex: set the search term, or change which page is being viewed.

## Reducer

This is saved on a per-site basis. 

```js
{
	"orders": {
		[ siteId ] : {
			list: {
				currentPage: 1,
				currentSearch: "Smith",
			},
		}
	}
}
```

## Selectors

### `getOrdersCurrentPage( state, [siteId] )`

Gets the current page being shown to the user. Defaults to 1.

### `getOrdersCurrentSearch( state, [siteId] )`

Gets the current search term being shown to the user. Defaults to "".

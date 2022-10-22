This is a repository of example wrappers and scripts to make API requests to get or post data.

Please refer to [API Support](https://api-portal.ti.com/support) for additional help and resources.

# 1. Python API Requests

We have the following example modules in the `/python` directory, each corresponding to a slide in the API introduction slideshow.

- `Example1.py` retrieves an API access token.
- `Example2.py` retrieves inventory information and places a test store order.
- `Example3.py` subscribes to a part and places a test order when notified.
- `Example4.py` retrieves a list of placed orders and then retrieves each order's invoice.

After updating the user credentials in the script, each example can be run from that directory in the terminal using the following command:

```
py <filename>.py
```

These examples use a module `TI_API_Suite.py` of API-specific classes which can also be used by customers out-of-the-box.

- `TI_AdvancedShippingNotifications` retrieves Advanced Shipping Notifications (ASN) and related information pertaining to an order.
- `TI_FinancialDocuments` retrieves financial documents pertaining to an order.
- `TI_Orders` allows the user to place and view orders.
- `TI_StoreCatalog` allows the user to browse the store inventory.
- `TI_StoreSubscription` allows the user to subscribe to parts in the store to receive notifications about them.

You can import specific classes from the above module using the following code in Python, replacing `<class>` with your desired API class:

```
from TI_API_Suite import <class>
```

Finally, the `API_Accessor.py` module contains the back-end logic for each of the API classes to acquire an API access token and send API requests.

The markdown file `python/Tutorial.md` goes into greater detail about how to write your own programs and classes to interface with APIs in Python.

You must have installed the `requests` package to use any of these classes and modules; it is available freely under the Apache2 license. The programs were written using Python 3.7.3.

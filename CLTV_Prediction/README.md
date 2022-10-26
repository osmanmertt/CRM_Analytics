**In this study, CLTV prediction was made using BG-NBD and Gamma-Gamma models.CLTV (Customer Lifetime Value) is a prognostication of the net profit contributed to the whole future relationship with a customer.Various formulations on the subject are given below.**
* **CLTV =** Conditional Expected Number of Transaction * Conditional Expected Number of Profit
* **CLTV =** BG-NBD Model * Gamma-Gamma Submodel
* **CLTV =** (Customer Value / Churn Rate(constant value)) * Profit Margin
* **Customer Value =** Average Order Value * Purchase Frequency
* **Average Order Value =** Total Price / Total Transaction
* **Purchase Frequency =** Total Transaction / Total Number of Customers
* **Churn Rate =** 1 - Repeat Rate(Retention Rate)
* **Repeat Rate =** Number of Customers Making Multiple Purchases / Total Number of Customers
* **Profit Margin =** Total Price * Profit Value(constant value)
 
**BG-NBD Model consists of probabilistic modeling of two processes for Expected Number of Transaction :**
> **Transaction Process(Buy) + Dropout Process (Till You Die)**

**In transaction Process, r and alpha describe the gamma distribution
of the BG-NBD transaction process. This distribution is the distribution of the number of transactions to be performed by a customer in a given period of time as long as it is alive. Also, each customer has a dropout probability with probability p. A customer drops with a certain probability after making purchase. This happens inside the Dropout Process.**

**The Gamma-Gamma Submodel is used to predict how much profit a customer can generate on average per trade. Since BG-NBD and Gamma-Gamma are probabilistic models, outliers in the dataset should be determine and processed while implementing them.**

**Information about the columns is given below.**

* **master_id :** Unique customer id
* **order_channel :** Which channel of the shopping platform is used (Android, ios, Desktop, Mobile)
* **last_order_channel :** The channel where the most recent purchase was made
* **first_order_date :** Date of the customer's first purchase
* **last_order_date :** Date of the customer's last purchase
* **last_order_date_online :** The date of the last purchase made by the customer on the online platform
* **last_order_date_offline :** The date of the last purchase made by the customer on the offline
* **order_num_total_ever_online :** The total number of purchases made by the customer on the online platform
* **order_num_total_ever_offline :** The total number of purchases made by the customer on the offline platform
* **customer_value_total_ever_offline :** Total fee paid by the customer for offline purchases
* **customer_value_total_ever_online :** Total fee paid by the customer for online purchases
* **interested_in_categories_12  :** List of categories the customer has shopped in the last 12 months

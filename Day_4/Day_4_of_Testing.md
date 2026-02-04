# Bug Report: Order placed with invalid total (NaN quantity)

## Summary
When the quantity field is manually cleared and incremented using the `+` button, the quantity becomes `NaN`.  
This results in `NaN` values for both subtotal and total in the cart.  
Despite this invalid monetary state, the order can still be placed successfully.

---

## Steps to Reproduce
1. Open the Potion Shop  
2. Add any potion to the cart  
3. Observe the default quantity (`1`)  
4. Manually clear the quantity input (leave it empty)  
5. Click the `+` button  
6. Observe:
   - Quantity becomes `NaN`
   - Subtotal shows `NaN gold`
   - Total shows `NaN gold`
7. Fill in delivery details  
8. Submit the order  

---

## Expected Result
- Quantity should never enter an invalid state  
- Cart totals should always be valid numeric values  
- Order submission should be blocked if totals are invalid  

---

## Actual Result
- Quantity becomes `NaN`  
- Cart displays `NaN` subtotal and total  
- Order submission succeeds despite invalid pricing  

---

## Severity
**High**

### Reason
The system allows checkout with an invalid price calculation, which can lead to incorrect billing and data integrity issues.
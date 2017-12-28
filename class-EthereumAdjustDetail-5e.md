```
class EthereumAdjustDetail(models.Model):
//
// SETTLEMENT DATA DETAILS
//
_name = 'x_ethereum.adjust_detail'
x_adjustID = fields.Char(string='SETTLEMENT MASTER CODE')
x_transactionID = fields.Char(string='TRANSACTION CODE')
x_exchangelD = fields.Char(string='MARKET PRICE CODE')
x_adjustIS = fields.Char(string='SETTLEMENT RESULT',default='N')
```

```
class EthereumAdjust(models.Model):
//
// SETTLEMENT DATA SUMMARY
//
_name = 'x_ethereum.adjust_master'
x_adjust_datetime = fields.Char(string='SETTLEMENT DATE')
x_adjust_customerlD = fields.Char(string='SETTLEMENT CUSTOMER CODE')
x_adjust_transCount = fields.Integer(string='SUM OF NUMBERS OF SETTLEMENT REQUESTS')
x_adjust_transAmount = fields.Char(string='SUM OF AMOUNT OF SETTLEMENT REQUESTS')
x_adiust_PayedAmount = fields.Char(string='SUM OF PAID AMOUNT OF SETTLEMENT')
x_adjust_balanceAmount = fields.Char(String='SETTLEMENT BALANCE')
x_adjust_transFromDate = fields.Char(string='SETTLEMENT START DATE')
x_adjust_transToDate = fields.Char(string='SETTLEMENT END DATE')
x_adjust_averageExchange = fields.Float(string='AVERAGE MARKET PRICE')
x_adjust_status = fields.Selection([('open','REQUEST'),('work','BEING SETTLED'),('close','COMPLETE')])
x_adjust_list = fields.Text(string='LIST OF SETTLEMENT TARGET TRANSACTION IDS')
```

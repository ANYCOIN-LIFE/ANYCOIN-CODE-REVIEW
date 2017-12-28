```
class EthereumExchangeLog(models.Model):
//
// ETHEREUM EXCHANGE RATE LOG
//
_name = 'x_ethereum.exchangelog'
x_exchangelD = fields.Char(string='EXCHANGE RATE CODE')
x_exchange_date = fields.Char(string='APPLICATION DATE',size=10)
x_exchange_time = fields.Char(string='APPLICATION TIME',size=5)
x_exchange_value = fields.Char(string='EXCHANGE RATE',size=20)
```

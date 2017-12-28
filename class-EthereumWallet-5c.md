```
class EthereumWallet(models.Model):
//
// WALLET INFORMATION
//
name = 'x_ethereum.wallet'
x_accountID = fields.Char(string='ACCOUNT CODE')
x_customerlD = fields.Char(string='CUSTOMER CODE')
x_use_tokenID = fields.Char(string='USED TOKEN')
x_wallet_kind = fields.Char(string='COIN TYPE',help='TYPE OF ELECTRONIC WALLET IS CLASSIFIED INTO BITCOIN AND ETHEREUM.')
#x_accountID = fields.Many2one('ethereum.account',string='ACCOUNT CODE')
#x_customerlD = fields.Many2one('ethereum.customer',string='CUSTOMER CODE')
#x_wallet_kind = fields.Selection([('BT','BITCOIN'), ('ET','ETHEREUM')],string='COIN TYPE',help='TYPE OF ELECTRONIC WALLET IS CLASSIFIED INTO BITCOIN AND ETHEREUM.')
x_wallet_address = fields.Char(string='WALLET ADDRESS',size=200)
x_wallet_balance = fields.Float(string='WALLET BALANCE',default=0)
x_ether_balance = fields.Float(string='ETHEREUM BALANCE',default=0)
x_is_master = fields.Char(string='MASTER TALK',size=1,default='N')
```

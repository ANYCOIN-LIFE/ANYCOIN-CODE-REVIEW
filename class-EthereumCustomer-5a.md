```
class EthereumCustomer(models.Model):
//
// CUSTOMER INFORMATION
//
# _inherit = 'res.partner'
_name = 'x_ethereum.customer'
x_name = fields.Char(string='USER NAME)
x_cust_type = fields.Selection([('PE','INDIVIDUAL'),('CO','COMPANY')], string='CUSTOMER TYPE',help='CUSTOMER IS CLASSIFIED AS INDIVIDUAL AND COMPANY.')
x_user_id = fields.Char(string='USER ID')
x_user_pw = fields.Char(string='USER PASSWORD', size=64, invisible=True, copy=False)
x_language_code = fields.Char(string='LANGUAGE CODE')
x_country_calling_code = fields.Char(string='COUNTRY CODE')
x_user_hp = fields.Char(string='USER PHONE NUMBER')
x_user_email = fields.Char(string='USER E-MAIL')
x_phone_kind = fields.Char(string='SMARTPHONE TYPE -A : ANDROID PHONE. I: iPHONE')
x_regid = fields.Char(string='PUSH MESSAGE regid')
x_join_version = fields.Char(string='VERSION AT THE TIME OF SUBSCRIPTION')
x_ioin_datetime = fields.Char(string='SUBSCRIPTION DATE')
x_agreed_terms_version = fields.Char(string='TERMS VERSION AGREED AT THE TIME OF SUBSCRIPTION')
x_current_version = fields.Char(string='CURRENT VERSION')
x_last_access_datetime = fields.Char(string='LAST ACCESS DATE')
x_store_name = fields.Char(string='STORE NAME')
x_store_address = fields.Char(string='STORE ADDRESS',size=100)
x_store_lmageURL = fields.Char(string='STORE IMAGE URL',size=100)
x_bank_account = fields.Char(string='BAND WITH WHICH USER HAS ACCOUNT AND ACCOUNT NUMBER',size=50)
x_store_kind = fields.Char(string='BUSINESS TYPE')
x_recommanded_userlD = fields.Char(string='RECOMMENDER ID')
x_ceo_name = fields.Char(string='REPRESENTATIVE NAME')
x_store_latitude = fields.Char(string='LATITUDE', default='0.0')
x_store_longitude = fields.Char(string='LONGITUDE', default='0.0')
x_token_kind = fields.Char(string='SERVICE TOKEN TYPE')
x_appoint_store = fields.Char(string='DESIGNATED STORE', default='all')
x_funding_groupID = fields.Char(string='FUNDING GROUP', default='n/a')
```

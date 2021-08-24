# scms 
select 
branch_code,
sum(CMSN_EXPN_CON_TAX) as HANSHUI,
sum(CMSN_EXPN_NOT_CON_TAX) as BUHANSHUI,
sum(CMSN_EXPN_CON_TAX-CMSN_EXPN_NOT_CON_TAX) as SHUIFEI,
sum(PBL_INS_PREM) as SHOURU
from channelcomm where STAT_MO=#{DATE}
GROUP BY branch_code

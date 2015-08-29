# jsPduDecoder

Decodes many PDU encoded SMS formats.
The main decoding is done in JavaScript. For WBXML decoding, a server side third party library 'wbxml.lib' is used via a proxy script.

## COPYRIGHT AND LICENCE

Copyright (C) 2009 Benjamin Erhart, berhart@tladesignz.com

This program is free software; you can redistribute it and/or modify it
under the terms of either: the GNU General Public License as published
by the Free Software Foundation; or the Artistic License.

See http://dev.perl.org/licenses/ for more information.


## Some test examples, the tool will work with:


### Standard SMS:
http://twit88.com/home/utility/sms-pdu-encode-decode
07911326040000F0040B911346610089F60000208062917314080CC8F71D14969741F977FD07

### Standard SMS Deliver:
http://www.dreamfabric.com/sms/
07917283010010F5040BC87238880900F10000993092516195800AE8329BFD4697D9EC37

### Standard SMS Submit:
http://www.dreamfabric.com/sms/
0011000B916407281553F80000AA0AE8329BFD4697D9EC37

### Standard SMS:
http://mobiletidings.com/2009/02/11/more-on-the-sms-pdu/
0001000B915121551532F400000CC8F79D9C07E54F61363B04

### Flash SMS:
http://mobiletidings.com/2009/02/12/sending-a-flash-sms-message/
0001010B915121551532F40010104190991D9EA341EDF27C1E3E9743

### 3 Concatenated SMS:
http://mobiletidings.com/2009/02/18/combining-sms-messages/
0041000B915121551532F40000A0050003000301986F79B90D4AC3E7F53688FC66BFE5A0799A0E0AB7CB741668FC76CFCB637A995E9783C2E4343C3D4F8FD3EE33A8CC4ED359A079990C22BF41E5747DDE7E9341F4721BFE9683D2EE719A9C26D7DD74509D0E6287C56F791954A683C86FF65B5E06B5C36777181466A7E3F5B0AB4A0795DDE936284C06B5D3EE741B642FBBD3E1360B14AFA7E7
0041010B915121551532F40000A005000300030240EEF79C2EAF9341657C593E4ED3C3F4F4DB0DAAB3D9E1F6F80D6287C56F797A0E72A7E769509D0E0AB3D3F17A1A0E2AE341E53068FC6EB7DFE43768FC76CFCBF17A98EE22D6D37350B84E2F83D2F2BABC0C22BFD96F3928ED06C9CB7079195D7693CBF2341D947683EC6F761D4E0FD3CB207B999DA683CAF37919344EB3D9F53688FC66BFE5
0041020B915121551532F4000090050003000303CAA0721D64AE9FD3613AC85D67B3C32078589E0ED3EB7257113F2EC3E9E5BA1C344FBBE9A0F7781C2E8FC374D0B80E4F93C3F4301DE47EBB4170F93B4D2EBBE92CD0BCEEA683D26ED0B8CE868741F17A1AF4369BD3E37418442ECFCBF2BA9B0E6ABFD9EC341D1476A7DBA03419549ED341ECB0F82DAFB75D

### Service Load WAP Push:
http://mobiletidings.com/2009/02/21/wap-push-over-sms-encodings/
0041000B915121551532F400042E0B05040B84C0020003F001010A060403B081EA02066A008509036D6F62696C65746964696E67732E636F6D2F0001

### Service Indication WAP Push:
http://mobiletidings.com/2009/02/26/wap-push-over-sms-si-encoding/
0041000B915121551532F400045E0B05040B84C0020003F001010B060403AE81EA02056A0045C60C036D6F62696C65746964696E67732E636F6D2F000AC30620090226162510C3062009030416250103436865636B206F7574204D6F62696C6520546964696E677321000101

### EMS with text formatting:
http://mobiletidings.com/2009/03/12/text-formatting-sms-ems/
0041000B915121551532F40000631A0A031906200A032104100A032705040A032E05080A043807002B8ACD29A85D9ECFC3E7F21C340EBB41E3B79B1E4EBB41697A989D1EB340E2379BCC02B1C3F27399059AB7C36C3628EC2683C66FF65B5E2683E8653C1D

### Voicemail Indication:
http://mobiletidings.com/2009/07/08/voicemail-waiting-indication-sms/
0001AB0B915121551532F400C80F3190BB7C07D9DFE971B91D4EB301

### Standard SMS-DELIVER:
http://www.developershome.com/sms/cmgrCommand3.asp
07915892000000F0040B915892214365F700007040213252242331493A283D0795C3F33C88FE06C9CB6132885EC6D341EDF27C1E3E97E7207B3A0C0A5241E377BB1D7693E72E

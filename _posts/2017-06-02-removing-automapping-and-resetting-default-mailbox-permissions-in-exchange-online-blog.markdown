---
layout: post 
title:  "Removing automapping and resetting default mailbox permissions in Exchange Online | Blog" 
date:   2017-06-01T22:09:25.271Z 
categories: exchange exchangeonline
link: http://www.michev.info/Blog/Post/1382/removing-automapping-and-resetting-default-mailbox-permissions-in-exchange-online 
tags:
  - links
ogtype: article 
---

> Removing automapping and resetting default mailbox permissions in Exchange Online
Posted on February 28, 2016 by Vasil Michev
Corrupted mailbox permissions and automapping settings are not that uncommon scenario and many Exchange admins have run into it. In the on-prem world, apart from re-examining the settings or re-applying the permissions, one can perform additional troubleshooting by playing with the relevant AD attributes directly. For the case of automapping, those are the msExchDelegateListLink and the msExchDelegateListBL attributes, as explained for example in this article.

In the Exchange Online world however, we don’t have access to the underlying AD infrastructure and we cannot even see the values of these attributes, let alone change them. So in case something was wrong with them, our only option was to escalate a case to Microsoft so that a support engineer can make any changes necessary. Last year however, life was made a bit easier, with Microsoft introducing support for the ClearAutoMapping parameter for Remove-MailboxPermission. The parameter basically purges any entries present in the msExchDelegateListLink attribute, which in turn should also remove the corresponding entry under the user’s msExchDelegateListBL backlink attribute. Usage of the cmdlet is very easy, you simply need to provide the identity of the mailbox for which to clear the automapping entries:
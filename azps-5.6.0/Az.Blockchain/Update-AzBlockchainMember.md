---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 833e660980d82c32667d166dbeed4520686d1124
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930402"
---
# Update-AzBlockchainMember

## SYNOPSIS
Blockchain-tag frissítése

## SZINTAXIS

### UpdateExpanded (alapértelmezett)
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## LEÍRÁS
Blockchain-tag frissítése

## PÉLDÁK

### 1. példa: Blockchain-tag frissítése
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

Ez a parancs frissíti a blockchain egyik tagját.

### 2. példa: Blockchain-tag frissítése
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

Ez a parancs frissíti a blockchain egyik tagját.

## PARAMETERS

### -ConsortiumManagementAccountPassword
Beállítja a felügyelt consortium felügyeleti fiók jelszavát.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallRule
Beállítja vagy beállítja a tűzfal szabályait.
Ennek létrehozásáról a NOTES (JEGYZETEK) szakaszban található a FIREWALLRULE tulajdonságokról és egy kivonattábla létrehozásáról.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Blockchain member name.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
Beállítja a tranzakciós csomópont dns-végpontjának alapvető hitelesítésjelszóját.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforrást tartalmazó erőforráscsoport neve.
Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.
Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
A szolgáltatás címkéi, amelyek az erőforrást leíró kulcsérték-párok listáját jelentik.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


FIREWALLRULE <IFirewallRule[]>: Beállítja vagy beállítja a tűzfal szabályait.
  - `[EndIPAddress <String>]`: Beállítja vagy beállítja a tűzfalszabály-tartomány IP-címét.
  - `[RuleName <String>]`: Beállítja vagy beállítja a tűzfalszabályok nevét.
  - `[StartIPAddress <String>]`: A tűzfalszabály tartományának kezdő IP-címét kapja meg vagy állítja be.

INPUTOBJECT: <IBlockchainIdentity> Identity Parameter
  - `[BlockchainMemberName <String>]`: Blockchain member name.
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[Location <String>]`: Hely neve.
  - `[OperationId <String>]`: Műveletazonosító.
  - `[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.
  - `[SubscriptionId <String>]`: Beveszi az előfizetés azonosítóját, amely egyedileg azonosítja a Microsoft Azure-előfizetést. Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.
  - `[TransactionNodeName <String>]`: Tranzakciós csomópont neve.

## KAPCSOLÓDÓ HIVATKOZÁSOK


---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: 33d6df1bfb22f2b1db0c59a041fafb079fe65660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492701"
---
# Add-AzureRmStorageAccountNetworkRule

## Áttekintés
 IpRules vagy VirtualNetworkRules hozzáadása a NetworkRule tulajdonságához

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### NetWorkRuleString (alapértelmezett)
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### IpRuleObject
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NetworkRuleObject
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### IpRuleString
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **Add-AzureRmStorageAccountNetworkRule** parancsmag IpRules vagy VirtualNetworkRules ad az NetworkRule tulajdonsághoz.

## Példák

### 1. példa: több IpRules hozzáadása a IPAddressOrRange
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

Ez a parancs több IpRules adhat hozzá a IPAddressOrRange-hoz.

### 2. példa: VirtualNetworkRule hozzáadása a VirtualNetworkResourceID
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

Ezzel a paranccsal VirtualNetworkRule adhat hozzá a VirtualNetworkResourceID-hoz.

### 3. példa: VirtualNetworkRules felvétele más fiókból származó VirtualNetworkRule-objektumokkal
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

Ezzel a paranccsal VirtualNetworkRules adhat hozzá a VirtualNetworkRule-objektumokból egy másik fiókból.

### 4. példa: több IpRule hozzáadása IpRule-objektumokhoz, JSON-bevitel
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

Ez a parancs több IpRule adhat hozzá IpRule objektumokkal, a JSON-szal.

## PARAMÉTEREK

### -AsJob
A parancsmag futtatása a háttérben

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressOrRange
A IpAddressOrRange tömbje, a beviteli IpAddressOrRange és az alapértelmezett művelettel IpRules adja hozzá az NetworkRule tulajdonságot.

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPRule
A NetworkRule tulajdonságba felvenni kívánt IpRule-objektumok tömbje.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A tárolási fiók nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkResourceId
A VirtualNetworkResourceId tömbje hozzáadja a VirtualNetworkRule a beviteli VirtualNetworkResourceId és az alapértelmezett művelettel NetworkRule tulajdonságot.

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkRule
A NetworkRule tulajdonságba felvenni kívánt VirtualNetworkRule-objektumok tömbje.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. Command. Management. Storage. models. PSIpRule []
Paraméterek: IPRule (ByValue)

### Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule []
Paraméterek: VirtualNetworkRule (ByValue)

## KIMENETEK

### Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule

### Microsoft. Azure. Command. Management. Storage. models. PSIpRule

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

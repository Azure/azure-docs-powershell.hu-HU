---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843586"
---
# Set-AzPublicIpAddress

## Áttekintés
Egy nyilvános IP-cím cél állapotának beállítása.

## SZINTAXISA

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzPublicIpAddress** parancsmag a nyilvános IP-cím cél állapotát állítja be.

## Példák

### 1: nyilvános IP-cím kiosztási módjának módosítása
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Az első parancs a nyilvános IP-cím erőforrást kapja a név $publicIPName az erőforráscsoport $rgName.
A második parancs a nyilvános IP-cím objektum kiosztási módját a "statikus" értékre állítja.
Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal, és a hozzárendelési módszert "Static" értékre módosítja. A nyilvános IP-címet azonnal kiosztja A rendszer.

### 2: nyilvános IP-cím DNS-tartománynevének módosítása
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Az első parancs a nyilvános IP-cím erőforrást kapja a név $publicIPName az erőforráscsoport $rgName.
A második parancs a DomainNameLabel tulajdonságot a szükséges DNS-előtagra állítja be.
Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal. A DomainNameLabel & FQDN a várt módon módosul.

## PARAMÉTEREK

### -AsJob
A parancsmag futtatása a háttérben

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
Itt adhatja meg azt a **PublicIpAddress** -objektumot, amely a nyilvános IP-címet megadó cél állapotot adja meg.

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSPublicIpAddress
A ' PublicIpAddress ' paraméter az "PSPublicIpAddress" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSPublicIpAddress

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[Új – AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)



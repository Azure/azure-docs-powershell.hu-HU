---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: f6de3902770fd799f8ce5a41d5aa1230e6821f02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493108"
---
# Get-AzureRmLoadBalancerFrontendIpConfig

## Áttekintés
Beilleszti az előtér IP-konfigurációját egy terheléselosztó nézetben.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmLoadBalancerFrontendIpConfig** parancsmag az előtér IP-konfigurációját, illetve az előtér IP-konfigurációinak listáját a terheléselosztásban kapja.

## Példák

### 1. példa: az előtér IP-konfigurációjának beszerzése a terheléselosztó bővítményben
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

Az első parancs beolvassa a MyLoadBalancer nevű terheléselosztást, majd a változóban tárolja $slb.

A második parancs beilleszti az előtér-végponthoz társított IP-konfigurációt.

## PARAMÉTEREK

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

### -LoadBalancer
Annak az IP-konfigurációnak a terheléselosztását adja meg, amely az előtér IP-konfigurációjához van társítva.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
Annak az IP-konfigurációnak a neve, amely az előtér IP-konfigurációját tartalmazza.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSLoadBalancer
A ' LoadBalancer ' paraméter az "PSLoadBalancer" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmLoadBalancerFrontendIpConfig](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[Get-AzureRmLoadBalancer](./Get-AzureRmLoadBalancer.md)

[Új – AzureRmLoadBalancerFrontendIpConfig](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[Remove-AzureRmLoadBalancerFrontendIpConfig](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[Set-AzureRmLoadBalancerFrontendIpConfig](./Set-AzureRmLoadBalancerFrontendIpConfig.md)



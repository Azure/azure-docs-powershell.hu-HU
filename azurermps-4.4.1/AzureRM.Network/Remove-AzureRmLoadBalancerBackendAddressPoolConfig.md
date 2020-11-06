---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: eb7f7b85286d491d4168e08ef94c1a46ff9076ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492473"
---
# Remove-AzureRmLoadBalancerBackendAddressPoolConfig

## Áttekintés
A backend-címkészlet konfigurációjának eltávolítása a terheléselosztó webhelyről.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** parancsmag a backend-címkészlet eltávolítását a terheléselosztó webhelyről.

## Példák

### 1. példa: a backend-címkészlet konfigurációjának eltávolítása a terheléselosztó webhelyről
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

Ez a parancs beolvassa a MyLoadBalancer nevű terheléselosztást, és átadja a **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , amely eltávolítja a BackendAddressPool02 konfigurációt a MyLoadBalancer.
Végül az Set-AzureRmLoadBalancer parancsmag frissíti a MyLoadBalancer.
Felhívjuk a figyelmét arra, hogy a backend-címkészlet konfigurációjának csak a törlése előtt kell lennie.

## PARAMÉTEREK

### -LoadBalancer
Itt adhatja meg az eltávolítandó backend-címkészletet tartalmazó terheléselosztót.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
Annak a backend-címkészlet a nevét adja meg, amelyre a parancsmag eltávolítja.

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### Microsoft. Azure. commands. Network. models. PSLoadBalancer

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmLoadBalancerBackendAddressPoolConfig](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[Get-AzureRmLoadBalancer](./Get-AzureRmLoadBalancer.md)

[Get-AzureRmLoadBalancerBackendAddressPoolConfig](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[Új – AzureRmLoadBalancerBackendAddressPoolConfig](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)



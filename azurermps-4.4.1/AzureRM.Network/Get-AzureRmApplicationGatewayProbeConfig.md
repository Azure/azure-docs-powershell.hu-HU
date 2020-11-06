---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 6583856eb6d44fa170b53a855e43db71602534a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493441"
---
# Get-AzureRmApplicationGatewayProbeConfig

## Áttekintés
A meglévő állapot-szonda konfigurációjának beolvasása egy alkalmazás-Átjáróból.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A Get-AzureRmApplicationGatewayProbeConfig parancsmag meglévő állapot-szonda konfigurációt kap egy alkalmazás-Átjáróból.

## Példák

### Példa 1: meglévő szonda beszerzése egy alkalmazás-átjáróból
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

Ez a parancs beolvassa a Probe02 nevű biztonságiállapot-szonda az átjáró nevű alkalmazási átjáróból.

## PARAMÉTEREK

### -ApplicationGateway
Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a szonda konfigurációját kapja.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A szonda nevét adja meg.

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

### PSApplicationGateway
A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe

### System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Szonda hozzáadása meglévő alkalmazás-átjáróhoz](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[Add-AzureRmApplicationGatewayProbeConfig]()

[Új – AzureRmApplicationGatewayProbeConfig]()

[Remove-AzureRmApplicationGatewayProbeConfig]()

[Set-AzureRmApplicationGatewayProbeConfig]()


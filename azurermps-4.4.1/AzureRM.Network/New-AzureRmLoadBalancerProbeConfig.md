---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 57c0d491d5e330f45550381b099e20e5d02fd8f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679398"
---
# New-AzureRmLoadBalancerProbeConfig

## Áttekintés
A terheléselosztó beállításához létrehoz egy szonda-konfigurációt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmLoadBalancerProbeConfig** parancsmag létrehoz egy, az Azure-terheléselosztáshoz használható szonda-konfigurációt.

## Példák

### Példa 1: Probe-konfiguráció létrehozása
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

A parancs létrehoz egy MyProbe nevű szonda-konfigurációt a HTTP protokoll használatával.
Az új szonda egy terheléselosztásos szolgáltatáshoz csatlakozik a 80-on.

## PARAMÉTEREK

### -IntervalInSeconds
A szondáknak a terheléselosztási szolgáltatás egyes példányaihoz való előfordulási gyakoriságát adja meg másodpercben.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A létrehozandó szonda-konfiguráció nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port
Azt a portot adja meg, amelyen az új szonda a terheléselosztási szolgáltatáshoz csatlakozik.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeCount
Itt adhatja meg, hogy egy példánynál hány egymást követő hiba esetén legyenek egészségtelenek.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
A Probe beállításához használandó protokollt adja meg.
A paraméter elfogadható értékei a következők: TCP vagy http.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestPath
Annak az elérési útját adja meg egy terheléselosztásos szolgáltatásban, amellyel meghatározhatja az állapotot.

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

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSProbe

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmLoadBalancerProbeConfig](./Add-AzureRmLoadBalancerProbeConfig.md)

[Get-AzureRmLoadBalancerProbeConfig](./Get-AzureRmLoadBalancerProbeConfig.md)

[Remove-AzureRmLoadBalancerProbeConfig](./Remove-AzureRmLoadBalancerProbeConfig.md)

[Set-AzureRmLoadBalancerProbeConfig](./Set-AzureRmLoadBalancerProbeConfig.md)



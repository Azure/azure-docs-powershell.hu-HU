---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 622501a69632be9c9c70cfccaf4e806df94e7276
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006485"
---
# Add-AzLoadBalancerProbeConfig

## SYNOPSIS
Konfigurációt ad a terheléselosztáshoz.

## SZINTAXIS

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzLoadBalancerProbeConfig** parancsmag konfigurációt ad az Azure terheléselegyenlőjébe.

## PÉLDÁK

### 1. példa: Konfiguráció konfigurációjának hozzáadása terheléselosztáshoz
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

Ez a parancs lekérte a myLb nevű terheléselosztást, hozzáadja a megadott konfigurációt a konfigurációhoz, majd a **Set-AzLoadBalancer** parancsmagot használja a terheléselosztás frissítéséhez.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IntervalInSeconds
A terheléselosztási szolgáltatás egyes példányai közötti intervallumot adja meg másodpercben.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancer
Egy **LoadBalancer-objektumot** ad meg.
Ez a parancsmag hozzáad egy konfigurációs konfigurációt a paraméter által megadott terheléselosztáshoz.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name
Megadja a hozzáadni szükséges konfigurációs konfiguráció nevét.

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
Azt a portot adja meg, amelyen a terheléselosztású szolgáltatáshoz csatlakoznia kell.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CountCount
Az egy példányon egymást követő sikertelen példányok számát adja meg, amelyek nem megfelelőnek minősülnek.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Protocol
A vizsgálathoz használt protokollt adja meg.
A paraméter elfogadható értékei: Tcp vagy Http.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RequestPath
A terheléselosztási szolgáltatásban meghatározza az állapot megállapításához használni megfelelő elérési utat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

### System.String

### System.Int32

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzLoadBalancerProbeConfig](./Get-AzLoadBalancerProbeConfig.md)

[New-AzLoadBalancerProbeConfig](./New-AzLoadBalancerProbeConfig.md)

[Remove-AzLoadBalancerProbeConfig](./Remove-AzLoadBalancerProbeConfig.md)

[Set-AzLoadBalancer](./Set-AzLoadBalancer.md)

[Set-AzLoadBalancerProbeConfig](./Set-AzLoadBalancerProbeConfig.md)



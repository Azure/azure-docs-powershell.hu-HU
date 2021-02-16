---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144875"
---
# New-AzVmssIpConfig

## SYNOPSIS
IP-konfigurációt hoz létre a VMSS hálózati felületére.

## SZINTAXIS

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **New-AzVmssIpConfig** parancsmag IP-konfigurációs objektumot hoz létre egy virtuálisgép-mérethalmaz (VMSS) hálózati felületének.
Adja meg a parancsmag konfigurációját a Add-AzVmssNetworkInterfaceConfiguration *IPConfiguration* paramétereként.

## PÉLDÁK

### 1. példa: IP-konfigurációs objektum létrehozása VMSS-felülethez
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Ez a parancs létrehoz egy ContosoVmssInterface02 nevű IP-konfigurációs objektumot.
A parancs egy korábban definiált alhálózati azonosítót használ, amely a $SubnetId.
A parancs a konfigurációs beállításokat a $IPConfiguration változóban tárolja az **Add-AzVmssNetworkInterfaceConfiguration későbbi használatra.**

### 2. példa: NAT-készletbeállításokat tartalmazó IP-konfigurációs objektum létrehozása
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Ez a parancs létrehoz egy ContosoVmssInterface03 nevű IP-konfigurációs objektumot, majd azt a $IPConfiguration változóban tárolja későbbi használatra.
A parancs egy korábban definiált alhálózati azonosítót használ, amely a $SubnetId.
A parancs a konfigurációs beállításokat a $IPConfiguration későbbi használatra tárolja.
A parancs értékeket ad meg a *LoadBalancerInboundNatPoolsId* és *a LoadBalancerBackendAddressPoolsId* paraméterhez.

## PARAMETERS

### -ApplicationGatewayBackendAddressPoolsId
A terhelésegyenleg-kiegyenlítők háttércímkészletére mutató hivatkozásokat tartalmazó tömböt ad meg.
A méretaránykészletek hivatkozhatnak egy nyilvános és egy belső terheléselosztási készlet háttércímkészletére.
Több méretarány-készlet nem használhatja ugyanazt a terheléselosztást.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DnsSetting
A publicIP-címekre alkalmazandó DNS-beállítások.
A publicIP-címeken alkalmazandó DNS-beállítások tartománynévfelirata.
A tartománynévfelirat és a vm-index össze concatenatione a létrehoz majd egy nyilvános IP-cím típusú erőforrás tartománynevét.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
Egy azonosítót ad meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
Ip Tag-objektumok tömbje.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
A bejövő hálózati címfordítási (NAT) készletekre mutató hivatkozásokat tartalmazó tömböt ad meg a terheléselosztáshoz.
A méretaránykészletek hivatkozhatnak egy nyilvános és egy belső terheléselosztási rendszer bejövő NAT-készletére.
Több méretarány-készlet nem használhatja ugyanazt a terheléselosztást.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
A terhelésegyenleg-elosztás bejövő NAT-készletére mutató hivatkozások tömbje.
A méretaránykészletek hivatkozhatnak egy nyilvános és egy belső terheléselosztási rendszer bejövő NAT-készletére.
Több méretarány-készlet nem használhatja ugyanazt a terheléselosztást.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Az IP-konfiguráció nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Primary
Megadja az elsődleges IP-konfigurációt abban az esetben, ha a hálózati felület több IP-konfigurációval rendelkezik.

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

### -PrivateIPAddressVersion
Adja meg a privát IP-cím IP-konfigurációját.  Az alapértelmezett érték IPv4.  Lehetséges értékek: "IPv4" és "IPv6".

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

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
A nyilvános IP-cím üresjárati időkorlátja.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
A publicIP-cím konfigurációjának neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressVersion
Adja meg a nyilvános IP-cím IP-konfigurációját.  Az alapértelmezett érték IPv4.  Lehetséges értékek: "IPv4" és "IPv6".

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

### -PublicIPPrefix
A nyilvános IP-előtag azonosítója

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

### -SubnetId
Megadja azt az alhálózati azonosítót, amelyben a konfiguráció létrehozza a VMSS hálózati felületet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.String[]

### System.Int32

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]

## KIMENETEK

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)



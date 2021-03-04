---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 967e45ce124ead583a7c2f3e36a80dedb80d4e20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931761"
---
# Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript

## SYNOPSIS
Ez a parancsmag a kapcsolaterőforrást, a VPN-eszköz márkát, a modellt, a belső vezérlőprogram verzióját veszi fel, és visszaadja a megfelelő konfigurációs parancsfájlt, amit az ügyfelek közvetlenül alkalmazhatnak a helyszíni VPN-eszközeiken. A parancsfájl a kijelölt eszköz szintaxisát követi, és kitölti a szükséges paramétereket, például az Azure Gateway nyilvános IP-címét, a virtuális hálózati cím előtagját, a VPN-átjáró előre megosztott kulcsát stb., így az ügyfelek egyszerűen másolhat és illeszthet be VPN-eszközkonfigurációkat.

## SZINTAXIS

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Ez a parancsmag a kapcsolaterőforrást, a VPN-eszköz márkát, a modellt, a belső vezérlőprogram verzióját veszi fel, és visszaadja a megfelelő konfigurációs parancsfájlt, amit az ügyfelek közvetlenül alkalmazhatnak a helyszíni VPN-eszközeiken. A parancsfájl a kijelölt eszköz szintaxisát követi, és kitölti a szükséges paramétereket, például az Azure Gateway nyilvános IP-címét, a virtuális hálózati cím előtagját, a VPN-átjáró előre megosztott kulcsát stb., így az ügyfelek egyszerűen másolhat és illeszthet be VPN-eszközkonfigurációkat.

## PÉLDÁK

### 1. példa
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

A fenti példa Get-AzVirtualNetworkGatewaySupportedVpnDevice virtuális magánhálózati eszközmárkák, -modellek és belső vezérlőprogram-verziók lekértéhez.
Ezután a visszaadott modellinformációk egyikével létrehoz egy VPN-eszköz konfigurációs parancsfájlt a VirtualNetworkGatewayConnection "TestConnection" szolgáltatáshoz. A példában használt eszközben a DeviceFamily "IOS-Test", a DeviceVendor "Cisco-Test" és a FirmwareVersion 20 található.

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

### -DeviceFamily
A VPN-eszközmodell/-család neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeviceVendor
A VPN-eszköz szállítójának neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FirmwareVersion
A VPN-eszköz belső vezérlőprogram-verziója.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Annak a kapcsolatnak az erőforrásneve, amelyhez létre kell hozatni a konfigurációt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### System.String

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

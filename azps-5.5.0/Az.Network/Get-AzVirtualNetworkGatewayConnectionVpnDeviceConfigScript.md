---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151875"
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
Ez a parancsmag a kapcsolaterőforrást, a VPN-eszköz márkáját, a modellt, a belső vezérlőprogram verzióját használja, és visszaadja a megfelelő konfigurációs parancsfájlt, amit az ügyfelek közvetlenül a helyszíni VPN-eszközeiken alkalmazhatnak. A parancsfájl a kijelölt eszköz szintaxisát követi, és kitölti a szükséges paramétereket, például az Azure Gateway nyilvános IP-címét, a virtuális hálózati cím előtagját, a VPN-átjáró előre megosztott kulcsát stb., így az ügyfelek egyszerűen másolhat és illeszthet be VPN-eszközkonfigurációkat.

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
A VPN-eszköz belső vezérlőprogramjának verziója.

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

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: ec91fecd41138238bc4d89fa81d77bae4730c770
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407607"
---
# Get-AzVpnClientPackage

## SYNOPSIS
Információkat kap a VPN-ügyfélcsomagról.

## SZINTAXIS

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzVpnClientPackage** parancsmag információkat kap a virtuális hálózati átjárókból elérhető VPN-ügyfélcsomagokkal kapcsolatban.
Az ügyfélcsomagok olyan konfigurációs adatokat tartalmaznak, amelyek lehetővé teszik az ügyfélszámítógépnek, hogy VIRTUÁLIS VPN-kapcsolatot létesítsen egy Azure virtuális hálózattal; VPN-kapcsolat létrehozásához az ügyfélszámítógépeken telepítve kell lennie a megfelelő konfigurációs csomagnak.
Különböző konfigurációs csomagok érhetők el az ügyfélszámítógép Windows-verziója (például Windows 7 vagy Windows 10) és az ügyfélszámítógép processzor architektúrája (AMD64 vagy x86) alapján.
A **Get-AzVpnClientPackage** futtatásakor meg kell adnia az architektúra típusát.

## PÉLDÁK

### 1. példa: Információ a processzorarchitektúra VIRTUÁLIS magánhálózati ügyfélcsomagról
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Ez a parancs információkat kap a ContosoVirtualNetworkGateway nevű virtuális hálózati átjáróban tárolt AMD64 VPN-ügyfélcsomagról.
Az x86-os ügyfélcsomagokkal kapcsolatos információk lekérdezése érdekében állítsa a *ProcessorArchitecture* paraméter értékét x86 értékre.

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

### -ProcessorArchitecture
Az ügyfélcsomag által tervezett processzorarchitektúra típusát határozza meg.
Érvényes értékek: Amd64 és X86.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a nevét adja meg, amelyhez a virtuális hálózati átjáró hozzá van rendelve.
Az erőforráscsoportok a készletkezelés és az általános Azure-felügyelet egyszerűsítése érdekében kategorizálják az elemeket.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Annak a virtuális hálózati átjárónak a nevét adja meg, amely az ügyfélcsomag adatait tárolja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Resize-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)




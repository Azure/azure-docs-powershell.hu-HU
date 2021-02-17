---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156866"
---
# New-AzVpnClientConfiguration

## SYNOPSIS
Ezzel a paranccsal a felhasználók létrehozhatják a Vpn-profilcsomagot a VPN-átjárón előre konfigurált VPN-beállítások alapján, valamint néhány további, a felhasználók által konfigurálandó beállításon kívül (például néhány főtanúsítvány esetében).

## SZINTAXIS

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
Ez lehetővé teszi a felhasználóknak, hogy a VPN-átjárón előre konfigurált VPN-beállítások alapján létrehozták a Vpn-profilcsomagot, valamint néhány további, a felhasználóknak esetleg konfigurálható beállítást is ( például néhány főtanúsítványhoz).

## PÉLDÁK

### 1. példa
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

Ez a parancsmag egy VPN-ügyfélprofil zip fájl létrehozásához használható a "ContosoVirtualNetworkGateway" számára a ResourceGroup "ContosoResourceGroup" csoportban. A profil egy előre konfigurált sugárkiszolgálóhoz jön létre, amely úgy van konfigurálva, hogy az "EAPTLS" hitelesítési módszert használja a VpnProfileRadiusCert tanúsítványfájllal.

## PARAMETERS

### -AuthenticationMethod
A hitelesítési módszer az EAPMSCHAPv2 vagy az EAPTLS értéket is veszi fel. Az EAPMSCHAPv2 megadása után a parancsmag létrehoz egy ügyfélkonfigurációs telepítőt a felhasználónév/jelszó hitelesítéséhez, amely EAP-MSCHAPv2 hitelesítési protokollt használ. Ha az EAPTLS meg van adva, akkor a parancsmag létrehoz egy ügyfélkonfigurációs telepítőt az EAP-TLS protokollt használó tanúsítvány-hitelesítéshez. Az "EapTls" lehetőség használható a VIRTUÁLIS hálózati átjáró által a megbízható legfelső szintű hitelesítés feltöltésével végzett, a SUGÁRALAPÚ tanúsítvány-hitelesítéshez és a hitelesítés-hitelesítéshez is. A parancsmag automatikusan észleli a konfigurált adatokat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
Az ügyfél legfelső szintű tanúsítványának elérési útjai

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -Name
Az erőforrás neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProcessorArchitecture
ProcessorArchitecture

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RootRootCertificateFile
A sugárkiszolgáló gyökértanúsítványának elérési útja. Ez egy kötelező paraméter, amely meg kell, hogy legyen adva a SUGAR-hitelesítéssel használt EAP-TLS esetén. Ez annak a .cer fájlnak a teljes elérési útja, amely azt a ROOT-tanúsítványt tartalmazza, amely az ügyfél által a SUGAR-kiszolgáló hitelesítés során való érvényesítéséhez használható.

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

### System.String

### System.String[]

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSVpnProfile

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)

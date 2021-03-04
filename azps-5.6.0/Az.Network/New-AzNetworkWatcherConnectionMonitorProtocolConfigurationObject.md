---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: d6450eb7efaf7c49666cb67fe8c80def05f64678
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921850"
---
# New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject

## SYNOPSIS
Protokollkonfiguráció létrehozása a tesztelés elvégzéséhez TCP, HTTP vagy ICMP protokollon keresztül.

## SZINTAXIS

### TCP
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <UInt16>
 [-DisableTraceRoute] [-DestinationPortBehavior <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### HTTP
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <UInt16>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ICMP
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject parancsmag protokollkonfigurációt hoz létre a teszteléshez TCP, HTTP vagy ICMP protokollon keresztül.

## PÉLDÁK

### 1. példa
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

Port: 80 DisableTraceRoute: False

### 2. példa

Protokollkonfiguráció létrehozása a tesztelés elvégzéséhez TCP, HTTP vagy ICMP protokollon keresztül. (automatikusan generált)

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -IcmpProtocol
```

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

### -DestinationPortBehavior
A célportport viselkedése.
A támogatott értékek: Nincs, ListenIfAvailable.

```yaml
Type: System.String
Parameter Sets: TCP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableTraceRoute
Érték, amely azt jelzi, hogy le kell-e tiltani az útvonal-kiértékelést a nyomkövetési útvonalsal.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpProtocol
HTTP protokollkapcsoló.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IcmpProtocol
ICMP protokollkapcsoló.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Method
A http-módszer használata.

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Az URI elérési út összetevője.
Például: "/dir1/dir2".

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port
Az a port, amelyhez csatlakozni szeretne.

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreferHTTPS
Érték, amely azt jelzi, hogy a HTTPS-t a HTTP-hez előnyben részesítik-e olyan esetekben, amikor a választási lehetőség nem explicit.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestHeader
A kéréssel együtt továbbítja a HTTP-fejléceket.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TcpProtocol
TCP protokoll kapcsoló.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidStatusCodeRange
SIKERES HTTP-állapotkódok.
Például: "2xx,301-304,418".

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTcpConfiguration

### Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorHttpConfiguration

### Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorIcmpConfiguration

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

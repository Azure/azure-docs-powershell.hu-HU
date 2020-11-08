---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187871"
---
# New-AzApiManagementSslSetting

## Áttekintés
A PsApiManagementSslSetting példányának létrehozása

## SZINTAXISA

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A segítő parancs a PsApiManagementSslSetting példányának létrehozásához.
Ezt a parancsot New-AzApiManagement paranccsal kell használni.

## Példák

### 1. példa: SSL-beállítás létrehozása, amely lehetővé teszi a TLS 1,0 használatát a Backendeken és a felületeken egyaránt
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

A PsApiManagementSslSetting új példányát létrehozhatja a TLSv 1,0-ban mindkét (az ügyfél és a APIM között) és a ApiManagement átjáró (APIM és backend) között.

## PARAMÉTEREK

### -BackendProtocol
A backend biztonsági protokoll beállításai Ez a paraméter nem kötelező.
Az érvényes protokoll-beállítások a `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CipherSuite
A megadott sorrendben az SSL-titkosítási lakosztályok beállításai. Ez a paraméter nem kötelező.
Az érvényes beállítások a `TripleDes168` pacal Des 168-engedélyezése/letiltása

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -FrontendProtocol
Felület biztonsági protokolljainak beállításai Ez a paraméter nem kötelező.
Az érvényes protokoll-beállítások a `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0


```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerProtocol
A kiszolgálói protokollok beállításai, például a Http2. Ez a paraméter nem kötelező.
Az érvényes beállítások engedélyezve vannak a `Http2` http-2,0

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSslSettings

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzApiManagement](./New-AzApiManagement.md)


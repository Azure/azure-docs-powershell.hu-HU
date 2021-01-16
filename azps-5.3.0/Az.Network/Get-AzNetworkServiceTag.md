---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: c511dc6eba981708557797dc657e4626621f9131
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379957"
---
# Get-AzNetworkServiceTag

## SYNOPSIS
A szolgáltatáscímke-információs erőforrások listájának lekérte.

## SZINTAXIS

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzNetworkServiceTag parancsmag** lekérte a szolgáltatáscímke-információs erőforrások listáját.

Felhívjuk a figyelmét arra, hogy az Ön által megadott Azure-régióadatokat hivatkozásként fogja használni a verzióhoz (nem helyalapú szűrőként). Ha például megadja, akkor is meg fogja kapni az előtaggal kapcsolatos adatokat tartalmazó szolgáltatáscímkéket az összes régióban, de csak arra a felhőre korlátozódik, amelyhez az előfizetés tartozik (például nyilvános, egyesült államokbeli kormányzati, kínai vagy `-Location eastus2` németországi).

## PÉLDÁK

### 1. példa
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags

Name         : Public
Id           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/providers/Microsoft.Network/serviceTags/Public
Type         : Microsoft.Network/serviceTags
ChangeNumber : 63
Cloud        : Public
Values       : {ApiManagement, ApiManagement.AustraliaCentral, ApiManagement.AustraliaCentral2, ApiManagement.AustraliaEast...}

PS C:\> $serviceTags.Values

Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : ApiManagement.AustraliaCentral
System Service   : AzureApiManagement
Region           : australiacentral
Address Prefixes : {20.36.106.68/31, 20.36.107.176/28}
Change Number    : 2

Name             : ApiManagement.AustraliaCentral2
System Service   : AzureApiManagement
Region           : australiacentral2
Address Prefixes : {20.36.114.20/31, 20.36.115.128/28}
Change Number    : 2

Name             : ApiManagement.AustraliaEast
System Service   : AzureApiManagement
Region           : australiaeast
Address Prefixes : {13.70.72.28/31, 13.70.72.240/28, 13.75.217.184/32, 13.75.221.78/32...}
Change Number    : 3

Name             : ApiManagement.AustraliaSoutheast
System Service   : AzureApiManagement
Region           : australiasoutheast
Address Prefixes : {13.77.50.68/31, 13.77.52.224/28}
Change Number    : 2

...
```

A parancs beszerzi a szolgáltatáscímke-információforrások listáját, és változóban tárolja `serviceTags` azt.

### 2. példa: Az AzureSQL összes címelőtagja
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $sql = $serviceTags.Values | Where-Object { $_.Name -eq "Sql" }
PS C:\> $sql

Name             : Sql
System Service   : AzureSQL
Address Prefixes : {13.65.31.249/32, 13.65.39.207/32, 13.65.85.183/32, 13.65.200.105/32...}
Change Number    : 18

PS C:\> $sql.Properties.AddressPrefixes.Count
644
PS C:\> $sql.Properties.AddressPrefixes
13.65.31.249/32
13.65.39.207/32
13.65.85.183/32
13.65.200.105/32
13.65.209.243/32
...
```

Az első parancs beszerzi a szolgáltatáscímke-információforrások listáját, és változóban tárolja `serviceTags` azt.
A második parancs szűri a listát az Sql információs erőforrásának kiválasztásához.

### 3. példa: A Tárterület szolgáltatáscímke-információs erőforrásának lekérte a Nyugat-USA 2-re
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { $_.Name -eq "Storage.WestUS2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Name -like "Storage*" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Properties.SystemService -eq "AzureStorage" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5
```

Az első parancs beszerzi a szolgáltatáscímke-információforrások listáját, és változóban tárolja `serviceTags` azt.
Az alábbi parancsok a lista szűrésének különféle módjait mutatják be a 2. nyugat-amerikai 2. tárhely szolgáltatáscímke-információinak kiválasztásához.

### 4. példa: Az összes globális szolgáltatáscímke-információforrás lekérte
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { -not $_.Properties.Region }


Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : AppService
System Service   : AzureAppService
Address Prefixes : {13.64.73.110/32, 13.65.30.245/32, 13.65.37.122/32, 13.65.39.165/32...}
Change Number    : 13

Name             : AppServiceManagement
System Service   : AzureAppServiceManagement
Address Prefixes : {13.64.115.203/32, 13.66.140.0/26, 13.67.8.128/26, 13.69.64.128/26...}
Change Number    : 7

Name             : AzureActiveDirectory
System Service   : AzureAD
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.67.50.224/29...}
Change Number    : 3

Name             : AzureActiveDirectoryDomainServices
System Service   : AzureIdentity
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.69.66.160/27...}
Change Number    : 2

...
```

Az első parancs beszerzi a szolgáltatáscímke-információforrások listáját, és változóban tárolja `serviceTags` azt.
A második parancs szűri a listát, hogy csak a beállított terület nélkülieket jelölje ki.

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

### -Location
A verzió hivatkozásaként használt hely (nem helyalapú szűrőként) az összes régióra vonatkozó előtagadatokat tartalmazó szolgáltatáscímkék listáját fogja kapni, de csak arra a felhőre, amelyhez az előfizetés tartozik).

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

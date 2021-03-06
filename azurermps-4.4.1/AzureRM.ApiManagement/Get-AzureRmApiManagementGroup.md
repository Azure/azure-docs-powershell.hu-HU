---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0c28742eb3c774adb8c7b6a8d920e91377bea35f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499280"
---
# Get-AzureRmApiManagementGroup

## Áttekintés
Az API-adatkezelési csoportok teljes vagy konkrét beolvasása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Az összes csoport beolvasása (alapértelmezett)
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### A beolvasás csoport azonosítója
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Csoportok keresése felhasználó szerint
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Csoportok keresése termékenként
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmApiManagementGroup** parancsmag a teljes vagy bizonyos API-kezelési csoportokat kapja.

## Példák

### Példa 1: az összes csoport beolvasása
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext
```

Ez a parancs az összes csoportot beilleszti.

### 2. példa: csoport beszerzése AZONOSÍTÓval
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -GroupId "0123456789"
```

Ez a parancs a 0123456789 nevű csoport AZONOSÍTÓját kapja.

### 3. példa: csoport beszerzése név alapján
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -Name "Group0002"
```

Ez a parancs a Group0002 nevű csoportot kapja meg.

### 4. példa: az összes felhasználó csoportjának beolvasása
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -UserId "0123456789"
```

Ez a parancs a 0123456789 nevű felhasználói AZONOSÍTÓval minden felhasználó csoportba bekerül.

## PARAMÉTEREK

### -Környezet
A PsApiManagementContext példányát adja meg.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GroupId
A csoport AZONOSÍTÓját adja meg.
Ha meg van adva, a parancsmag megpróbálja megtalálni a csoportot az azonosítóval.

```yaml
Type: System.String
Parameter Sets: Get by group ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A felügyeleti csoport nevét adja meg.

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

### -Termékkód
A meglévő szorzat azonosítója
Ha meg van adva, akkor a rendszer minden olyan csoportot ad vissza, amelyre a terméket hozzárendeli.
Ez a paraméter nem kötelező.

```yaml
Type: System.String
Parameter Sets: Find groups by product
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserId
A meglévő szorzat azonosítóját adja meg.
Ha meg van adva, a parancsmag minden olyan csoportot ad vissza, amelyre a terméket hozzárendeli.

```yaml
Type: System.String
Parameter Sets: Find groups by user
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGroup>

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmApiManagementGroup](./New-AzureRmApiManagementGroup.md)

[Remove-AzureRmApiManagementGroup](./Remove-AzureRmApiManagementGroup.md)

[Set-AzureRmApiManagementGroup](./Set-AzureRmApiManagementGroup.md)



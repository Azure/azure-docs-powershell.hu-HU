---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 6396da138a0bafd54241f859c107601a1ce14b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935458"
---
# Set-AzDataLakeGen2ItemAclObject

## SYNOPSIS
Létrehozza/frissíti a DataLake gen2 elem ACL-objektumát, amely használható Update-AzDataLakeGen2Item parancsmagban.

## SZINTAXIS

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzDataLakeGen2ItemAclObject** parancsmag létrehoz/frissíti a DataLake gen2 elem ACL-objektumát, amely használható Update-AzDataLakeGen2Item parancsmagban.
Ha az AccessControlType/EntityId/DefaultScope típussal azonos AccessControlType/EntityId/DefaultScope típusú új ACL-bejegyzés nem létezik a bemeneti ACL-ban, új ACL-bejegyzést hoz létre, más szóval a meglévő ACL-bejegyzés frissítési engedélyét.

## PÉLDÁK

### 1. példa: ACL-objektum létrehozása 3 ACL-bejegyzéssel, és az ACL frissítése címtáron
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

Ez a parancs létrehoz egy 3 ACL-bejegyzéssel (az -InputObject paraméter használatával adjon hozzá egycl-bejegyzést a meglévő acl objektumhoz), és frissíti az ACL-t egy címtárban.

### 2. példa: ACL-objektum létrehozása 4 ACL bejegyzéssel, és meglévő ACL-bejegyzés engedélyének frissítése
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

Ez a parancs először létrehoz egy 4 ACL-bejegyzéssel rendelkező ACL-objektumot, majd futtatja újra a parancsmagot más engedéllyel, de egy meglévő ACL-bejegyzés AccessControlType/EntityId/DefaultScope objektumával.
Ezután az ACL-bejegyzés engedélye frissül, új ACL-bejegyzés azonban nem lesz hozzáadva.

## PARAMETERS

### -AccessControlType
Négy típus létezik: a "felhasználó" engedélyt ad a tulajdonosnak vagy egy megnevezett felhasználónak, a "csoport" a tulajdonos csoportnak vagy egy elnevezett csoportnak biztosít jogokat, a "maszk" korlátozza a megnevezett felhasználóknak és a csoportok tagjainak biztosított jogokat, az "egyéb" pedig minden olyan felhasználónak biztosít jogokat, aki nem található meg a többi bejegyzésben.

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultScope
Állítsa be ezt a paramétert annak jelzésére, hogy az ACE egy címtár alapértelmezett ACL-hez tartozik; ellenkező esetben a hatókör implicit, és az ACE az access ACL-hez tartozik.

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

### -EntityId
A felhasználó vagy csoport azonosítója.
Az AccessControlType "maszk" és az "egyéb" bejegyzései esetében a hiányzik.
A tulajdonosi és tulajdonosi csoport felhasználói vagy csoportazonosítója szintén hiányzik.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Ha a PSPathAccessControlEntry objektumot adja meg, az új ACL a bemeneti \[ \] PSPathAccessControlEntry objektum új eleme \[ \] lesz.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Engedély
Az engedélymező egy 3 karakterből áll, amelyben az első karakter "r", a második pedig "w", a harmadik pedig "x" a végrehajtási engedély megadásához.
Ha nem ad meg hozzáférést, a "-" karakter jelzi, hogy az engedély megtagadva.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

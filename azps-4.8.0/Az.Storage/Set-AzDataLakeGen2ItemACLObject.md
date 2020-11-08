---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180768"
---
# Set-AzDataLakeGen2ItemAclObject

## Áttekintés
Létrehozza/frissíti a DataLake Gen2-objektum ACL-objektumát, amelyet az Update-AzDataLakeGen2Item parancsmagban használhat.

## SZINTAXISA

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## Leírás
A **set-AzDataLakeGen2ItemAclObject** parancsmag létrehoz/frissít egy DataLake GEN2 elem ACL-objektumát, amelyet az Update-AzDataLakeGen2Item parancsmagban használhat.
Ha az új ACL-bejegyzés ugyanazokkal a AccessControlType/EntityId/DefaultScope nem létezik a beviteli ACL-ben, új ACL-bejegyzést hoz létre, különben a meglévő ACL-bejegyzés engedélye van.

## Példák

### 1. példa: ACL-objektum létrehozása 3 hozzáférés-vezérlési bejegyzéssel és az ACL frissítése egy címtárban
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

Ez a parancs egy ACL-objektumot hoz létre, amelyben 3 ACL-bejegyzés található (a-InputObject paraméterrel ACL-bejegyzést adhat hozzá a meglévő ACL-objektumokhoz), és frissíti a címtárban lévő ACL-t.

### 2. példa: ACL-objektum létrehozása 4 ACL-bejegyzéssel és meglévő ACL-bejegyzés engedélyével
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

Ez a parancs először létrehoz egy ACL-objektumot négy ACL-bejegyzéssel, majd ismét futtatja a parancsmagot, de a AccessControlType/EntityId/DefaultScope egy meglévő ACL-bejegyzést.
Ezután a program frissíti az ACL-bejegyzés engedélyét, de nem ad hozzá új ACL-bejegyzést.

## PARAMÉTEREK

### -AccessControlType
Négy típusa van: a "felhasználó" engedélyt ad a tulajdonosnak vagy egy névvel ellátott felhasználónak, a "csoport" jogosultságokat ad a tulajdonosi csoport vagy egy névvel ellátott csoport számára, a "maszk" korlátozza a névvel ellátott felhasználók és a csoportok tagjainak nyújtott jogosultságokat, valamint az "egyéb" engedélyeket minden felhasználó számára, amely nem található meg a többi bejegyzésben.

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
Ezt a paramétert akkor adja meg, ha az ász az alapértelmezett hozzáférés-vezérlési lista egy könyvtárhoz tartozik. Máskülönben a hatókör implicit, és az ACE az Access-ACL-hez tartozik.

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
A felhasználó vagy csoportazonosító.
A "maszk" és a "többi" AccessControlType bejegyzése hiányzik.
A felhasználó vagy csoportazonosító kimarad a tulajdonos és a tulajdonos csoport számára is.

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
Ha a PSPathAccessControlEntry objektum bemenete \[ \] , a program hozzáadja az új ACL-t a beviteli PSPathAccessControlEntry objektum új elemeként \[ \] .

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

### – Engedély
Az engedély mező egy 3 karakterből álló szekvencia, ahol az első karakter "r" az olvasási hozzáférés megadásához, a második karakter "w" az írási hozzáférés megadásához, a harmadik karakter pedig "x" a végrehajtási engedély megadásához.
Ha a hozzáférés nincs megítélve, a "-" karakter jelzi, hogy az engedély megtagadva van.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSPathAccessControlEntry

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

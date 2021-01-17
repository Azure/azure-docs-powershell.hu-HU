---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466891"
---
# <span data-ttu-id="d526b-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="d526b-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="d526b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d526b-102">SYNOPSIS</span></span>
<span data-ttu-id="d526b-103">Létrehozza/frissíti a DataLake gen2 elem ACL-objektumát, amely használható Update-AzDataLakeGen2Item parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="d526b-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="d526b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d526b-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="d526b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d526b-105">DESCRIPTION</span></span>
<span data-ttu-id="d526b-106">A **Set-AzDataLakeGen2ItemAclObject** parancsmag létrehoz/frissíti a DataLake gen2 elem ACL-objektumát, amely használható Update-AzDataLakeGen2Item parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="d526b-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="d526b-107">Ha az AccessControlType/EntityId/DefaultScope adattípussal rendelkező új ACL-bejegyzés nem létezik a bemeneti ACL-fájlban, új ACL-bejegyzést hoz létre, más szóval a meglévő ACL-bejegyzésre vonatkozó frissítési engedélyt.</span><span class="sxs-lookup"><span data-stu-id="d526b-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="d526b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d526b-108">EXAMPLES</span></span>

### <span data-ttu-id="d526b-109">1. példa: ACL-objektum létrehozása 3 ACL-bejegyzéssel, és az ACL frissítése címtáron</span><span class="sxs-lookup"><span data-stu-id="d526b-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
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

<span data-ttu-id="d526b-110">Ez a parancs létrehoz egy ACL-objektumot 3 ACL bejegyzéssel (az -InputObject paramétert használva adjon hozzá egycl-bejegyzést a meglévő acl objektumhoz), és frissíti az ACL-t egy címtárban.</span><span class="sxs-lookup"><span data-stu-id="d526b-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="d526b-111">2. példa: ACL-objektum létrehozása 4 ACL bejegyzéssel, és meglévő ACL-bejegyzés frissítési engedélye</span><span class="sxs-lookup"><span data-stu-id="d526b-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
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

<span data-ttu-id="d526b-112">Ez a parancs először létrehoz egy 4 ACL-bejegyzéssel rendelkező ACL-objektumot, majd futtatja újra a parancsmagot más engedéllyel, de egy meglévő ACL-bejegyzés AccessControlType/EntityId/DefaultScope típusú objektumával.</span><span class="sxs-lookup"><span data-stu-id="d526b-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="d526b-113">Ezután az ACL-bejegyzés engedélye frissül, új ACL-bejegyzés azonban nem lesz hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d526b-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="d526b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d526b-114">PARAMETERS</span></span>

### <span data-ttu-id="d526b-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="d526b-115">-AccessControlType</span></span>
<span data-ttu-id="d526b-116">Négy típus létezik: a "felhasználó" jogokat biztosít a tulajdonosnak vagy egy megnevezett felhasználónak, a "csoport" a tulajdonos csoportnak vagy egy megnevezett csoportnak biztosít jogokat, a "maszk" korlátozza a megnevezett felhasználóknak és a csoportok tagjainak biztosított jogokat, az "egyéb" pedig minden olyan felhasználónak biztosít jogokat, aki nem található meg a többi bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="d526b-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

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

### <span data-ttu-id="d526b-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="d526b-117">-DefaultScope</span></span>
<span data-ttu-id="d526b-118">Állítsa be ezt a paramétert annak jelzésére, hogy az ACE egy címtár alapértelmezett ACL-hez tartozik; ellenkező esetben a hatókör implicit, és az ACE az access ACL-hez tartozik.</span><span class="sxs-lookup"><span data-stu-id="d526b-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="d526b-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="d526b-119">-EntityId</span></span>
<span data-ttu-id="d526b-120">A felhasználó vagy csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d526b-120">The user or group identifier.</span></span>
<span data-ttu-id="d526b-121">Az AccessControlType "maszk" és az "egyéb" bejegyzései nem szerepelnek benne.</span><span class="sxs-lookup"><span data-stu-id="d526b-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="d526b-122">A tulajdonosi és tulajdonosi csoport felhasználói vagy csoportazonosítója szintén hiányzik.</span><span class="sxs-lookup"><span data-stu-id="d526b-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="d526b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d526b-123">-InputObject</span></span>
<span data-ttu-id="d526b-124">Ha a PSPathAccessControlEntry objektumot adja meg, az új \[ \] ACL-t a bemeneti PSPathAccessControlEntry objektum új elemeként fogja \[ \] hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="d526b-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

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

### <span data-ttu-id="d526b-125">-Engedély</span><span class="sxs-lookup"><span data-stu-id="d526b-125">-Permission</span></span>
<span data-ttu-id="d526b-126">Az engedélymező egy 3 karakterből áll, amelyben az első karakter az "r", a második pedig "w", a harmadik pedig "x" a végrehajtási engedély megadásához.</span><span class="sxs-lookup"><span data-stu-id="d526b-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="d526b-127">Ha nem ad meg hozzáférést, a "-" karakter jelzi, hogy az engedély megtagadva.</span><span class="sxs-lookup"><span data-stu-id="d526b-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="d526b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d526b-128">CommonParameters</span></span>
<span data-ttu-id="d526b-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d526b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d526b-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d526b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d526b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d526b-131">INPUTS</span></span>

### <span data-ttu-id="d526b-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="d526b-132">None</span></span>

## <span data-ttu-id="d526b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d526b-133">OUTPUTS</span></span>

### <span data-ttu-id="d526b-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="d526b-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="d526b-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d526b-135">NOTES</span></span>

## <span data-ttu-id="d526b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d526b-136">RELATED LINKS</span></span>

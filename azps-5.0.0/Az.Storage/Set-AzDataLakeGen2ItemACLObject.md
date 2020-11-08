---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185781"
---
# <span data-ttu-id="cec3e-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="cec3e-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="cec3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cec3e-102">SYNOPSIS</span></span>
<span data-ttu-id="cec3e-103">Létrehozza/frissíti a DataLake Gen2-objektum ACL-objektumát, amelyet az Update-AzDataLakeGen2Item parancsmagban használhat.</span><span class="sxs-lookup"><span data-stu-id="cec3e-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="cec3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cec3e-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="cec3e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cec3e-105">DESCRIPTION</span></span>
<span data-ttu-id="cec3e-106">A **set-AzDataLakeGen2ItemAclObject** parancsmag létrehoz/frissít egy DataLake GEN2 elem ACL-objektumát, amelyet az Update-AzDataLakeGen2Item parancsmagban használhat.</span><span class="sxs-lookup"><span data-stu-id="cec3e-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="cec3e-107">Ha az új ACL-bejegyzés ugyanazokkal a AccessControlType/EntityId/DefaultScope nem létezik a beviteli ACL-ben, új ACL-bejegyzést hoz létre, különben a meglévő ACL-bejegyzés engedélye van.</span><span class="sxs-lookup"><span data-stu-id="cec3e-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="cec3e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cec3e-108">EXAMPLES</span></span>

### <span data-ttu-id="cec3e-109">1. példa: ACL-objektum létrehozása 3 hozzáférés-vezérlési bejegyzéssel és az ACL frissítése egy címtárban</span><span class="sxs-lookup"><span data-stu-id="cec3e-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
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

<span data-ttu-id="cec3e-110">Ez a parancs egy ACL-objektumot hoz létre, amelyben 3 ACL-bejegyzés található (a-InputObject paraméterrel ACL-bejegyzést adhat hozzá a meglévő ACL-objektumokhoz), és frissíti a címtárban lévő ACL-t.</span><span class="sxs-lookup"><span data-stu-id="cec3e-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="cec3e-111">2. példa: ACL-objektum létrehozása 4 ACL-bejegyzéssel és meglévő ACL-bejegyzés engedélyével</span><span class="sxs-lookup"><span data-stu-id="cec3e-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
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

<span data-ttu-id="cec3e-112">Ez a parancs először létrehoz egy ACL-objektumot négy ACL-bejegyzéssel, majd ismét futtatja a parancsmagot, de a AccessControlType/EntityId/DefaultScope egy meglévő ACL-bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="cec3e-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="cec3e-113">Ezután a program frissíti az ACL-bejegyzés engedélyét, de nem ad hozzá új ACL-bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="cec3e-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="cec3e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cec3e-114">PARAMETERS</span></span>

### <span data-ttu-id="cec3e-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="cec3e-115">-AccessControlType</span></span>
<span data-ttu-id="cec3e-116">Négy típusa van: a "felhasználó" engedélyt ad a tulajdonosnak vagy egy névvel ellátott felhasználónak, a "csoport" jogosultságokat ad a tulajdonosi csoport vagy egy névvel ellátott csoport számára, a "maszk" korlátozza a névvel ellátott felhasználók és a csoportok tagjainak nyújtott jogosultságokat, valamint az "egyéb" engedélyeket minden felhasználó számára, amely nem található meg a többi bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="cec3e-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

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

### <span data-ttu-id="cec3e-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="cec3e-117">-DefaultScope</span></span>
<span data-ttu-id="cec3e-118">Ezt a paramétert akkor adja meg, ha az ász az alapértelmezett hozzáférés-vezérlési lista egy könyvtárhoz tartozik. Máskülönben a hatókör implicit, és az ACE az Access-ACL-hez tartozik.</span><span class="sxs-lookup"><span data-stu-id="cec3e-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="cec3e-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="cec3e-119">-EntityId</span></span>
<span data-ttu-id="cec3e-120">A felhasználó vagy csoportazonosító.</span><span class="sxs-lookup"><span data-stu-id="cec3e-120">The user or group identifier.</span></span>
<span data-ttu-id="cec3e-121">A "maszk" és a "többi" AccessControlType bejegyzése hiányzik.</span><span class="sxs-lookup"><span data-stu-id="cec3e-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="cec3e-122">A felhasználó vagy csoportazonosító kimarad a tulajdonos és a tulajdonos csoport számára is.</span><span class="sxs-lookup"><span data-stu-id="cec3e-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="cec3e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cec3e-123">-InputObject</span></span>
<span data-ttu-id="cec3e-124">Ha a PSPathAccessControlEntry objektum bemenete \[ \] , a program hozzáadja az új ACL-t a beviteli PSPathAccessControlEntry objektum új elemeként \[ \] .</span><span class="sxs-lookup"><span data-stu-id="cec3e-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

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

### <span data-ttu-id="cec3e-125">– Engedély</span><span class="sxs-lookup"><span data-stu-id="cec3e-125">-Permission</span></span>
<span data-ttu-id="cec3e-126">Az engedély mező egy 3 karakterből álló szekvencia, ahol az első karakter "r" az olvasási hozzáférés megadásához, a második karakter "w" az írási hozzáférés megadásához, a harmadik karakter pedig "x" a végrehajtási engedély megadásához.</span><span class="sxs-lookup"><span data-stu-id="cec3e-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="cec3e-127">Ha a hozzáférés nincs megítélve, a "-" karakter jelzi, hogy az engedély megtagadva van.</span><span class="sxs-lookup"><span data-stu-id="cec3e-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="cec3e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec3e-128">CommonParameters</span></span>
<span data-ttu-id="cec3e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cec3e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec3e-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cec3e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec3e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cec3e-131">INPUTS</span></span>

### <span data-ttu-id="cec3e-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="cec3e-132">None</span></span>

## <span data-ttu-id="cec3e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cec3e-133">OUTPUTS</span></span>

### <span data-ttu-id="cec3e-134">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="cec3e-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="cec3e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cec3e-135">NOTES</span></span>

## <span data-ttu-id="cec3e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cec3e-136">RELATED LINKS</span></span>

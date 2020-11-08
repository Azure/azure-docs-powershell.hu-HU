---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182045"
---
# <span data-ttu-id="70116-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="70116-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="70116-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70116-102">SYNOPSIS</span></span>
<span data-ttu-id="70116-103">Frissítsen egy fájlt vagy könyvtárat a tulajdonságok, a metaadatok, az engedély, az ACL és a tulajdonos lapon.</span><span class="sxs-lookup"><span data-stu-id="70116-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="70116-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70116-104">SYNTAX</span></span>

### <span data-ttu-id="70116-105">ReceiveManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70116-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70116-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="70116-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70116-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="70116-107">DESCRIPTION</span></span>
<span data-ttu-id="70116-108">Az **Update-AzDataLakeGen2Item** parancsmag frissíti a tulajdonságokat, a metaadatokat, az engedélyeket, az ACL-t és a tulajdonosokat tartalmazó fájlt vagy könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="70116-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="70116-109">Ez a parancsmag csak akkor működik, ha a tároló fiókhoz engedélyezve van a hierarchikus névtér.</span><span class="sxs-lookup"><span data-stu-id="70116-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="70116-110">Ezt a típusú fiókot úgy hozhatja létre, hogy a "New-AzStorageAccount" parancsmagot futtatja a "-EnableHierarchicalNamespace $true" paranccsal.</span><span class="sxs-lookup"><span data-stu-id="70116-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="70116-111">Példák</span><span class="sxs-lookup"><span data-stu-id="70116-111">EXAMPLES</span></span>

### <span data-ttu-id="70116-112">1. példa: ACL-objektum létrehozása 3 ACL-bejegyzéssel és az ACL frissítése a fájlrendszer összes eleméhez rekurzívan</span><span class="sxs-lookup"><span data-stu-id="70116-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Recurse | Update-AzDataLakeGen2Item -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser           
dir1/file1           False        1024            2020-03-23 09:29:18Z rwxrw-rw-    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="70116-113">Ez a parancs először egy ACL-objektumot hoz létre a 3 ACL-bejegyzéssel (a-InputObject paraméterrel az ACL-bejegyzést a meglévő ACL-objektumhoz), majd beolvashatja a fájlrendszer összes elemét, és frissítheti az ACL-elemeket.</span><span class="sxs-lookup"><span data-stu-id="70116-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="70116-114">2. példa: a fájl összes tulajdonságának frissítése és megjelenítése</span><span class="sxs-lookup"><span data-stu-id="70116-114">Example 2: Update all properties on a file, and show them</span></span>
```
PS C:\> $file = Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" `
                 -Acl $acl `
                 -Property @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="; "ContentEncoding" = "UDF8"; "CacheControl" = "READ"; "ContentDisposition" = "True"; "ContentLanguage" = "EN-US"} `
                 -Metadata  @{"tag1" = "value1"; "tag2" = "value2" } `
                 -Permission rw-rw-rwx `
                 -Owner '$superuser' `
                 -Group '$superuser'

PS C:\> $file

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser          

PS C:\> $file.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      rw-        
False        Other                      rw-        

PS C:\> $file.Permissions

Owner        : Execute, Write, Read
Group        : Write, Read
Other        : Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\> $file.Properties.Metadata

Key  Value 
---  ----- 
tag2 value2
tag1 value1

PS C:\> $file.Properties


LastModified          : 3/23/2020 9:57:33 AM +00:00
CreatedOn             : 3/23/2020 9:29:18 AM +00:00
Metadata              : {[tag2, value2], [tag1, value1]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 1024
ContentType           : image/jpeg
ETag                  : "0x8D7CF109B9878CC"
ContentHash           : {139, 189, 187, 176...}
ContentEncoding       : UDF8
ContentDisposition    : True
ContentLanguage       : EN-US
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="70116-115">Ez a parancs a fájl összes tulajdonságát frissíti (ACL, engedély, tulajdonos, csoport, metaadatok, tulajdonság frissíthető bármely conbination), és megjelenítheti őket a PowerShell-konzolban.</span><span class="sxs-lookup"><span data-stu-id="70116-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="70116-116">3. példa: ACL-bejegyzés hozzáadása egy címtárhoz</span><span class="sxs-lookup"><span data-stu-id="70116-116">Example 3: Add an ACL entry to a directory</span></span>
```
## Get the origin ACL
PS C:\> $acl = (Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/').ACL

# Update permission of a new ACL entry (if ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry)
PS C:\> $acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rw- -InputObject $acl  

# set the new acl to the directory
PS C:\> update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/' -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="70116-117">Ez a parancs beolvassa az ACL-t egy címtárból, frissítéseket/egy ACL-bejegyzést, és visszaállítja a címtárat.</span><span class="sxs-lookup"><span data-stu-id="70116-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="70116-118">Ha az ACL-bejegyzés ugyanazzal a AccessControlType/EntityId/DefaultScope nem létezik, akkor új ACL-bejegyzést fog hozzáadni, különben a meglévő ACL-bejegyzés engedélye.</span><span class="sxs-lookup"><span data-stu-id="70116-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="70116-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70116-119">PARAMETERS</span></span>

### <span data-ttu-id="70116-120">-ACL</span><span class="sxs-lookup"><span data-stu-id="70116-120">-Acl</span></span>
<span data-ttu-id="70116-121">A POSIX hozzáférés-vezérlési jogosultságait fájlok és könyvtárak esetében állítja be.</span><span class="sxs-lookup"><span data-stu-id="70116-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="70116-122">Hozza létre ezt az objektumot új AzDataLakeGen2ItemAclObject.</span><span class="sxs-lookup"><span data-stu-id="70116-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

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

### <span data-ttu-id="70116-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="70116-123">-Context</span></span>
<span data-ttu-id="70116-124">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="70116-124">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70116-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70116-125">-DefaultProfile</span></span>
<span data-ttu-id="70116-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70116-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70116-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="70116-127">-FileSystem</span></span>
<span data-ttu-id="70116-128">FileSystem neve</span><span class="sxs-lookup"><span data-stu-id="70116-128">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70116-129">-Csoport</span><span class="sxs-lookup"><span data-stu-id="70116-129">-Group</span></span>
<span data-ttu-id="70116-130">Beállítja a blob tulajdonosi csoportját.</span><span class="sxs-lookup"><span data-stu-id="70116-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="70116-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70116-131">-InputObject</span></span>
<span data-ttu-id="70116-132">Azure Datalake Gen2 elem objektum frissítése</span><span class="sxs-lookup"><span data-stu-id="70116-132">Azure Datalake Gen2 Item Object to update</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70116-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="70116-133">-Metadata</span></span>
<span data-ttu-id="70116-134">A címtár vagy a fájl metaadatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="70116-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="70116-135">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="70116-135">-Owner</span></span>
<span data-ttu-id="70116-136">Beállítja a blob tulajdonosát.</span><span class="sxs-lookup"><span data-stu-id="70116-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="70116-137">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="70116-137">-Path</span></span>
<span data-ttu-id="70116-138">A megadott fájlrendszerben frissítendő elérési út.</span><span class="sxs-lookup"><span data-stu-id="70116-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="70116-139">A "címtár/file.txt" vagy a "directory1/directory2/" formátumban lehet fájl vagy könyvtár.</span><span class="sxs-lookup"><span data-stu-id="70116-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="70116-140">Nem adja meg, hogy ez a paraméter frissíti a fájlrendszer gyökérkönyvtárát.</span><span class="sxs-lookup"><span data-stu-id="70116-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70116-141">– Engedély</span><span class="sxs-lookup"><span data-stu-id="70116-141">-Permission</span></span>
<span data-ttu-id="70116-142">A fájl tulajdonosának, a fájl tulajdonosi csoportjának és a többieknek a POSIX-hozzáférési engedélyének beállítása.</span><span class="sxs-lookup"><span data-stu-id="70116-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="70116-143">Minden osztály olvasási, írási vagy végrehajtási engedélyt kaphat.</span><span class="sxs-lookup"><span data-stu-id="70116-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="70116-144">A szimbolikus (rwxrw-RW-) támogatott.</span><span class="sxs-lookup"><span data-stu-id="70116-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="70116-145">Érvénytelen az ACL-vel együtt.</span><span class="sxs-lookup"><span data-stu-id="70116-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="70116-146">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="70116-146">-Property</span></span>
<span data-ttu-id="70116-147">A címtár vagy a fájl tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="70116-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="70116-148">A fájlok támogatott tulajdonságai: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="70116-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="70116-149">A címtár támogatott tulajdonságai: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="70116-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="70116-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70116-150">-Confirm</span></span>
<span data-ttu-id="70116-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70116-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70116-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70116-152">-WhatIf</span></span>
<span data-ttu-id="70116-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70116-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70116-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70116-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70116-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70116-155">CommonParameters</span></span>
<span data-ttu-id="70116-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70116-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70116-157">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70116-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70116-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70116-158">INPUTS</span></span>

### <span data-ttu-id="70116-159">System. String</span><span class="sxs-lookup"><span data-stu-id="70116-159">System.String</span></span>

### <span data-ttu-id="70116-160">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="70116-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="70116-161">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="70116-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="70116-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70116-162">OUTPUTS</span></span>

### <span data-ttu-id="70116-163">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="70116-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="70116-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70116-164">NOTES</span></span>

## <span data-ttu-id="70116-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70116-165">RELATED LINKS</span></span>

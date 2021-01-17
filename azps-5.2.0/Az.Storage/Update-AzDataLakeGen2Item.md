---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335165"
---
# <span data-ttu-id="df21a-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="df21a-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="df21a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df21a-102">SYNOPSIS</span></span>
<span data-ttu-id="df21a-103">Frissítheti a tulajdonságokat, metaadatokat, engedélyeket, ACL-et és tulajdonost tároló fájlokat vagy címtárat.</span><span class="sxs-lookup"><span data-stu-id="df21a-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="df21a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df21a-104">SYNTAX</span></span>

### <span data-ttu-id="df21a-105">ReceiveManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df21a-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df21a-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="df21a-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df21a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df21a-107">DESCRIPTION</span></span>
<span data-ttu-id="df21a-108">Az **Update-AzDataLakeGen2Item** parancsmag frissíti a tulajdonságokat, metaadatokat, engedélyeket, ACL-et és tulajdonost tároló fájlokat vagy címtárat.</span><span class="sxs-lookup"><span data-stu-id="df21a-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="df21a-109">Ez a parancsmag csak akkor működik, ha engedélyezve van a Hierarchikus névtér a Tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="df21a-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="df21a-110">Az ilyen típusú fiók az "-EnableHierarchicalNamespace $true" parancsmag futtatásával $true.</span><span class="sxs-lookup"><span data-stu-id="df21a-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="df21a-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df21a-111">EXAMPLES</span></span>

### <span data-ttu-id="df21a-112">1. példa: ACL-objektum létrehozása 3 ACL bejegyzéssel, és az ACL frissítése a fájlrendszer összes elemére rekurzív módon</span><span class="sxs-lookup"><span data-stu-id="df21a-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
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

<span data-ttu-id="df21a-113">Ez a parancs először létrehoz egy 3 acl bejegyzésű ACL-objektumot (az -InputObject paramétert használva adjon hozzá egycl bejegyzést a meglévő acl objektumhoz), majd szerezze be a fájlrendszer összes elemét, és frissítse az elemekcl-ét.</span><span class="sxs-lookup"><span data-stu-id="df21a-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="df21a-114">2. példa: Egy fájl összes tulajdonságának frissítése és megjelenítése</span><span class="sxs-lookup"><span data-stu-id="df21a-114">Example 2: Update all properties on a file, and show them</span></span>
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

<span data-ttu-id="df21a-115">Ez a parancs frissíti a fájl összes tulajdonságát (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span><span class="sxs-lookup"><span data-stu-id="df21a-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="df21a-116">3. példa: ACL-bejegyzés hozzáadása címtárhoz</span><span class="sxs-lookup"><span data-stu-id="df21a-116">Example 3: Add an ACL entry to a directory</span></span>
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

<span data-ttu-id="df21a-117">Ez a parancs ACL-t kap egy címtárból, frissíti/hozzáad egy ACL-bejegyzést, és visszaállítja a címtárat.</span><span class="sxs-lookup"><span data-stu-id="df21a-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="df21a-118">Ha az AccessControlType/EntityId/DefaultScope adattípusú ACL-bejegyzés nem létezik, új ACL-bejegyzést ad hozzá, különben frissíti a meglévő ACL-bejegyzés engedélyét.</span><span class="sxs-lookup"><span data-stu-id="df21a-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="df21a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df21a-119">PARAMETERS</span></span>

### <span data-ttu-id="df21a-120">-Acl</span><span class="sxs-lookup"><span data-stu-id="df21a-120">-Acl</span></span>
<span data-ttu-id="df21a-121">Beállítja a POSIX-hozzáférés-vezérlési jogokat a fájlokon és a könyvtárakon.</span><span class="sxs-lookup"><span data-stu-id="df21a-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="df21a-122">Hozza létre ezt az objektumot a New-AzDataLakeGen2ItemAclObject objektummal.</span><span class="sxs-lookup"><span data-stu-id="df21a-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

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

### <span data-ttu-id="df21a-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="df21a-123">-Context</span></span>
<span data-ttu-id="df21a-124">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="df21a-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="df21a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df21a-125">-DefaultProfile</span></span>
<span data-ttu-id="df21a-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df21a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df21a-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="df21a-127">-FileSystem</span></span>
<span data-ttu-id="df21a-128">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="df21a-128">FileSystem name</span></span>

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

### <span data-ttu-id="df21a-129">-Group</span><span class="sxs-lookup"><span data-stu-id="df21a-129">-Group</span></span>
<span data-ttu-id="df21a-130">Beállítja a blob tulajdonában lévő csoportot.</span><span class="sxs-lookup"><span data-stu-id="df21a-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="df21a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df21a-131">-InputObject</span></span>
<span data-ttu-id="df21a-132">Frissítend kell az Azure Datalake Gen2 elemobjektumot</span><span class="sxs-lookup"><span data-stu-id="df21a-132">Azure Datalake Gen2 Item Object to update</span></span>

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

### <span data-ttu-id="df21a-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="df21a-133">-Metadata</span></span>
<span data-ttu-id="df21a-134">A címtár vagy fájl metaadatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="df21a-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="df21a-135">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="df21a-135">-Owner</span></span>
<span data-ttu-id="df21a-136">Beállítja a blob tulajdonosát.</span><span class="sxs-lookup"><span data-stu-id="df21a-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="df21a-137">-Path</span><span class="sxs-lookup"><span data-stu-id="df21a-137">-Path</span></span>
<span data-ttu-id="df21a-138">A megadott fájlrendszerben frissíteni kívánt elérési út.</span><span class="sxs-lookup"><span data-stu-id="df21a-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="df21a-139">Fájl vagy címtár lehet "directory/file.txt" vagy "directory1/directory2/".</span><span class="sxs-lookup"><span data-stu-id="df21a-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="df21a-140">Ha nem adja meg ezt a paramétert, a rendszer frissíti a Fájlrendszer gyökérkönyvtárát.</span><span class="sxs-lookup"><span data-stu-id="df21a-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="df21a-141">-Engedély</span><span class="sxs-lookup"><span data-stu-id="df21a-141">-Permission</span></span>
<span data-ttu-id="df21a-142">Beállítja a POSIX-hozzáférési engedélyeket a fájltulajdonos, a fájltulajdonos csoport és mások számára.</span><span class="sxs-lookup"><span data-stu-id="df21a-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="df21a-143">Minden osztály olvasási, írási vagy végrehajtási engedélyt kap.</span><span class="sxs-lookup"><span data-stu-id="df21a-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="df21a-144">A szimbolikus (rwxrw-rw-) formátum támogatott.</span><span class="sxs-lookup"><span data-stu-id="df21a-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="df21a-145">Érvénytelen az Acl-sel együtt.</span><span class="sxs-lookup"><span data-stu-id="df21a-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="df21a-146">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="df21a-146">-Property</span></span>
<span data-ttu-id="df21a-147">Megadja a címtár vagy a fájl tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="df21a-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="df21a-148">A fájlok támogatott tulajdonságai: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="df21a-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="df21a-149">A címtár támogatott tulajdonságai: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="df21a-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="df21a-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df21a-150">-Confirm</span></span>
<span data-ttu-id="df21a-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="df21a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df21a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df21a-152">-WhatIf</span></span>
<span data-ttu-id="df21a-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="df21a-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df21a-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df21a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df21a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df21a-155">CommonParameters</span></span>
<span data-ttu-id="df21a-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df21a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df21a-157">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df21a-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df21a-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df21a-158">INPUTS</span></span>

### <span data-ttu-id="df21a-159">System.String</span><span class="sxs-lookup"><span data-stu-id="df21a-159">System.String</span></span>

### <span data-ttu-id="df21a-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="df21a-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="df21a-161">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="df21a-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="df21a-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df21a-162">OUTPUTS</span></span>

### <span data-ttu-id="df21a-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="df21a-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="df21a-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df21a-164">NOTES</span></span>

## <span data-ttu-id="df21a-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df21a-165">RELATED LINKS</span></span>

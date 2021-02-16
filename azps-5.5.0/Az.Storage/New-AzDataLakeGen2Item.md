---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158106"
---
# <span data-ttu-id="98158-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="98158-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="98158-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98158-102">SYNOPSIS</span></span>
<span data-ttu-id="98158-103">Hozzon létre egy fájlt vagy címtárat egy fájlrendszerben.</span><span class="sxs-lookup"><span data-stu-id="98158-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="98158-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="98158-104">SYNTAX</span></span>

### <span data-ttu-id="98158-105">Fájl (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98158-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98158-106">Címtár</span><span class="sxs-lookup"><span data-stu-id="98158-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98158-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="98158-107">DESCRIPTION</span></span>
<span data-ttu-id="98158-108">A **New-AzDataLakeGen2Item** parancsmag létrehoz egy fájlt vagy címtárat egy Fájlrendszerben egy Azure-tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="98158-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="98158-109">Ez a parancsmag csak akkor működik, ha engedélyezve van a Hierarchikus névtér a Tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="98158-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="98158-110">Az ilyen típusú fiók az "-EnableHierarchicalNamespace $true" parancsmag futtatásával $true.</span><span class="sxs-lookup"><span data-stu-id="98158-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="98158-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="98158-111">EXAMPLES</span></span>

### <span data-ttu-id="98158-112">1. példa: Címtár létrehozása megadott engedéllyel, Umask-fájlokkal, tulajdonságokkal és metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="98158-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="98158-113">Ez a parancs létrehoz egy adott Engedély, Umask, tulajdonságok és metaadatok alapján létrehozott címtárat.</span><span class="sxs-lookup"><span data-stu-id="98158-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="98158-114">2. példa: Adattavat-fájl létrehozása(feltöltése) helyi forrásfájlból, és a parancsmag a háttérben fut</span><span class="sxs-lookup"><span data-stu-id="98158-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="98158-115">Ez a parancs létrehoz(feltölt) egy adattavat fájlt egy helyi forrásfájlból, és a parancsmag a háttérben fut.</span><span class="sxs-lookup"><span data-stu-id="98158-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="98158-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98158-116">PARAMETERS</span></span>

### <span data-ttu-id="98158-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98158-117">-AsJob</span></span>
<span data-ttu-id="98158-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="98158-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98158-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="98158-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="98158-120">Az egyidejű aszinkron feladatok teljes mennyisége.</span><span class="sxs-lookup"><span data-stu-id="98158-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="98158-121">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="98158-121">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98158-122">-Környezet</span><span class="sxs-lookup"><span data-stu-id="98158-122">-Context</span></span>
<span data-ttu-id="98158-123">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="98158-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="98158-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98158-124">-DefaultProfile</span></span>
<span data-ttu-id="98158-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98158-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98158-126">-Directory</span><span class="sxs-lookup"><span data-stu-id="98158-126">-Directory</span></span>
<span data-ttu-id="98158-127">Azt jelzi, hogy ez az új elem nem fájl, de egy könyvtár.</span><span class="sxs-lookup"><span data-stu-id="98158-127">Indicates that this new item is a directory and not a file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Directory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98158-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="98158-128">-FileSystem</span></span>
<span data-ttu-id="98158-129">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="98158-129">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98158-130">-Force</span><span class="sxs-lookup"><span data-stu-id="98158-130">-Force</span></span>
<span data-ttu-id="98158-131">Ha átadott, akkor az új elem kérés nélkül jön létre</span><span class="sxs-lookup"><span data-stu-id="98158-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="98158-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="98158-132">-Metadata</span></span>
<span data-ttu-id="98158-133">A létrehozott címtár vagy fájl metaadatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="98158-133">Specifies metadata for the created directory or file.</span></span>

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

### <span data-ttu-id="98158-134">-Path</span><span class="sxs-lookup"><span data-stu-id="98158-134">-Path</span></span>
<span data-ttu-id="98158-135">A létrehozni kívánt elérési út a megadott fájlrendszerben.</span><span class="sxs-lookup"><span data-stu-id="98158-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="98158-136">Fájl vagy címtár lehet "directory/file.txt" vagy "directory1/directory2/"</span><span class="sxs-lookup"><span data-stu-id="98158-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98158-137">-Permission</span><span class="sxs-lookup"><span data-stu-id="98158-137">-Permission</span></span>
<span data-ttu-id="98158-138">Beállítja a POSIX-hozzáférési engedélyeket a fájltulajdonos, a fájltulajdonos csoport és mások számára.</span><span class="sxs-lookup"><span data-stu-id="98158-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="98158-139">Minden osztály olvasási, írási vagy végrehajtási engedélyt kap.</span><span class="sxs-lookup"><span data-stu-id="98158-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="98158-140">A szimbolikus (rwxrw-rw-) formátum támogatott.</span><span class="sxs-lookup"><span data-stu-id="98158-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="98158-141">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="98158-141">-Property</span></span>
<span data-ttu-id="98158-142">Megadja a létrehozott könyvtár vagy fájl tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="98158-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="98158-143">A fájlok támogatott tulajdonságai: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="98158-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="98158-144">A címtár támogatott tulajdonságai: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="98158-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="98158-145">-Source</span><span class="sxs-lookup"><span data-stu-id="98158-145">-Source</span></span>
<span data-ttu-id="98158-146">Adja meg azt a helyi forrásfájl elérési útját, amelyet egy Datalake Gen2-fájlba fog feltölteni.</span><span class="sxs-lookup"><span data-stu-id="98158-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98158-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="98158-147">-Umask</span></span>
<span data-ttu-id="98158-148">Amikor új elemet hoz létre, és a szülőcímtár nem rendelkezik alapértelmezett ACL-vel, az umask korlátozza a létrehozni kívánt fájl vagy címtár engedélyét.</span><span class="sxs-lookup"><span data-stu-id="98158-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="98158-149">Az így kapott engedélyt a p & ^u, ahol p az engedély, Ön pedig az umask.</span><span class="sxs-lookup"><span data-stu-id="98158-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="98158-150">A szimbolikus (rwxrw-rw-) formátum támogatott.</span><span class="sxs-lookup"><span data-stu-id="98158-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="98158-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98158-151">-Confirm</span></span>
<span data-ttu-id="98158-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="98158-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98158-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98158-153">-WhatIf</span></span>
<span data-ttu-id="98158-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="98158-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98158-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98158-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98158-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98158-156">CommonParameters</span></span>
<span data-ttu-id="98158-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98158-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98158-158">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98158-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98158-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98158-159">INPUTS</span></span>

### <span data-ttu-id="98158-160">System.String</span><span class="sxs-lookup"><span data-stu-id="98158-160">System.String</span></span>

### <span data-ttu-id="98158-161">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="98158-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="98158-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98158-162">OUTPUTS</span></span>

### <span data-ttu-id="98158-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="98158-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="98158-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="98158-164">NOTES</span></span>

## <span data-ttu-id="98158-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98158-165">RELATED LINKS</span></span>

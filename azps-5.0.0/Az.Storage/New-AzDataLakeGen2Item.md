---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185809"
---
# <span data-ttu-id="b5d3e-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b5d3e-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="b5d3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d3e-103">Fájl vagy könyvtár létrehozása a fájlrendszerben.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="b5d3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5d3e-104">SYNTAX</span></span>

### <span data-ttu-id="b5d3e-105">Fájl (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5d3e-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5d3e-106">Directory</span><span class="sxs-lookup"><span data-stu-id="b5d3e-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5d3e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5d3e-107">DESCRIPTION</span></span>
<span data-ttu-id="b5d3e-108">A **New-AzDataLakeGen2Item** parancsmag egy Azure Storage-fiókban lévő fájlrendszerben hoz létre fájlt vagy könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="b5d3e-109">Ez a parancsmag csak akkor működik, ha a tároló fiókhoz engedélyezve van a hierarchikus névtér.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="b5d3e-110">Ezt a típusú fiókot úgy hozhatja létre, hogy a "New-AzStorageAccount" parancsmagot futtatja a "-EnableHierarchicalNamespace $true" paranccsal.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="b5d3e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b5d3e-111">EXAMPLES</span></span>

### <span data-ttu-id="b5d3e-112">Példa 1: címtár létrehozása meghatározott engedélyekkel, umask, tulajdonságokkal és metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="b5d3e-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="b5d3e-113">Ez a parancs egy olyan könyvtárat hoz létre, amely meghatározott engedélyekkel, umask, tulajdonságokkal és metaadatokkal rendelkezik</span><span class="sxs-lookup"><span data-stu-id="b5d3e-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="b5d3e-114">2. példa: adattó-fájl létrehozása (feltöltése) helyi forrásból származó fájl, és a parancsmag a háttérben fut</span><span class="sxs-lookup"><span data-stu-id="b5d3e-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="b5d3e-115">Ezzel a paranccsal létrehozhatja az adattó fájljait egy helyi forrásfájlban, és a parancsmag a háttérben fut.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="b5d3e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5d3e-116">PARAMETERS</span></span>

### <span data-ttu-id="b5d3e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5d3e-117">-AsJob</span></span>
<span data-ttu-id="b5d3e-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b5d3e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5d3e-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b5d3e-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b5d3e-120">Az egyidejű aszinkron feladatok teljes összege.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="b5d3e-121">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-121">The default value is 10.</span></span>

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

### <span data-ttu-id="b5d3e-122">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b5d3e-122">-Context</span></span>
<span data-ttu-id="b5d3e-123">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="b5d3e-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b5d3e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d3e-124">-DefaultProfile</span></span>
<span data-ttu-id="b5d3e-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5d3e-126">-Címtár</span><span class="sxs-lookup"><span data-stu-id="b5d3e-126">-Directory</span></span>
<span data-ttu-id="b5d3e-127">Azt jelzi, hogy ez az új elem egy címtár, és nem a fájl.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-127">Indicates that this new item is a directory and not a file.</span></span>

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

### <span data-ttu-id="b5d3e-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b5d3e-128">-FileSystem</span></span>
<span data-ttu-id="b5d3e-129">FileSystem neve</span><span class="sxs-lookup"><span data-stu-id="b5d3e-129">FileSystem name</span></span>

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

### <span data-ttu-id="b5d3e-130">-Force</span><span class="sxs-lookup"><span data-stu-id="b5d3e-130">-Force</span></span>
<span data-ttu-id="b5d3e-131">Ha a továbbítás után az új elem minden kérdés nélkül létrejön</span><span class="sxs-lookup"><span data-stu-id="b5d3e-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="b5d3e-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b5d3e-132">-Metadata</span></span>
<span data-ttu-id="b5d3e-133">A létrehozott könyvtár vagy fájl metaadatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-133">Specifies metadata for the created directory or file.</span></span>

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

### <span data-ttu-id="b5d3e-134">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="b5d3e-134">-Path</span></span>
<span data-ttu-id="b5d3e-135">A meghatározott fájlrendszerben létrehozandó elérési út.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="b5d3e-136">Fájl vagy könyvtár lehet a "címtár/file.txt" vagy a "directory1/directory2/" formátummal.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="b5d3e-137">– Engedély</span><span class="sxs-lookup"><span data-stu-id="b5d3e-137">-Permission</span></span>
<span data-ttu-id="b5d3e-138">A fájl tulajdonosának, a fájl tulajdonosi csoportjának és a többieknek a POSIX-hozzáférési engedélyének beállítása.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="b5d3e-139">Minden osztály olvasási, írási vagy végrehajtási engedélyt kaphat.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="b5d3e-140">A szimbolikus (rwxrw-RW-) támogatott.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="b5d3e-141">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="b5d3e-141">-Property</span></span>
<span data-ttu-id="b5d3e-142">A létrehozott könyvtár vagy fájl tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="b5d3e-143">A fájlok támogatott tulajdonságai: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="b5d3e-144">A címtár támogatott tulajdonságai: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="b5d3e-145">-Forrás</span><span class="sxs-lookup"><span data-stu-id="b5d3e-145">-Source</span></span>
<span data-ttu-id="b5d3e-146">Adja meg azt a helyi forrásfájl-elérési utat, amelyet fel szeretne tölteni egy Datalake-Gen2-fájlba.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

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

### <span data-ttu-id="b5d3e-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="b5d3e-147">-Umask</span></span>
<span data-ttu-id="b5d3e-148">Új elem létrehozásakor a szülőmappa nem rendelkezik alapértelmezett ACL-vel, a umask korlátozza a létrehozandó fájl vagy könyvtár engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="b5d3e-149">Az eredményül kapott engedélyt a p & ^ u adja meg, ahol a p az engedély, és Ön a umask.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="b5d3e-150">A szimbolikus (rwxrw-RW-) támogatott.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="b5d3e-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b5d3e-151">-Confirm</span></span>
<span data-ttu-id="b5d3e-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5d3e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5d3e-153">-WhatIf</span></span>
<span data-ttu-id="b5d3e-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5d3e-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5d3e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d3e-156">CommonParameters</span></span>
<span data-ttu-id="b5d3e-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5d3e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d3e-158">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5d3e-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d3e-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5d3e-159">INPUTS</span></span>

### <span data-ttu-id="b5d3e-160">System. String</span><span class="sxs-lookup"><span data-stu-id="b5d3e-160">System.String</span></span>

### <span data-ttu-id="b5d3e-161">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5d3e-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b5d3e-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5d3e-162">OUTPUTS</span></span>

### <span data-ttu-id="b5d3e-163">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b5d3e-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="b5d3e-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5d3e-164">NOTES</span></span>

## <span data-ttu-id="b5d3e-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5d3e-165">RELATED LINKS</span></span>

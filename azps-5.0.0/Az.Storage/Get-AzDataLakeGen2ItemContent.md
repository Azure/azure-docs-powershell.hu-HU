---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195067"
---
# <span data-ttu-id="0f817-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="0f817-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="0f817-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f817-102">SYNOPSIS</span></span>
<span data-ttu-id="0f817-103">Fájl letöltése</span><span class="sxs-lookup"><span data-stu-id="0f817-103">Download a file.</span></span>

## <span data-ttu-id="0f817-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f817-104">SYNTAX</span></span>

### <span data-ttu-id="0f817-105">ReceiveManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f817-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f817-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="0f817-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f817-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f817-107">DESCRIPTION</span></span>
<span data-ttu-id="0f817-108">A **Get-AzDataLakeGen2ItemContent** parancsmag az Azure-alapú tárterület-fiókban lévő fájlok letöltését.</span><span class="sxs-lookup"><span data-stu-id="0f817-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="0f817-109">Ez a parancsmag csak akkor működik, ha a tároló fiókhoz engedélyezve van a hierarchikus névtér.</span><span class="sxs-lookup"><span data-stu-id="0f817-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="0f817-110">Ezt a típusú fiókot úgy hozhatja létre, hogy a "New-AzStorageAccount" parancsmagot futtatja a "-EnableHierarchicalNamespace $true" paranccsal.</span><span class="sxs-lookup"><span data-stu-id="0f817-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="0f817-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0f817-111">EXAMPLES</span></span>

### <span data-ttu-id="0f817-112">1. példa: fájl letöltése kérés nélkül</span><span class="sxs-lookup"><span data-stu-id="0f817-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="0f817-113">Ez a parancs nem kér fájlt egy helyi fájlra.</span><span class="sxs-lookup"><span data-stu-id="0f817-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="0f817-114">2. példa: fájl beszerzése, majd a pipeline parancs a fájl helyi fájlba való letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="0f817-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="0f817-115">Ez a parancs először kap egy fájlt, majd a csővezetéket a fájl helyi fájlba való letöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="0f817-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="0f817-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f817-116">PARAMETERS</span></span>

### <span data-ttu-id="0f817-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f817-117">-AsJob</span></span>
<span data-ttu-id="0f817-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0f817-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f817-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="0f817-119">-CheckMd5</span></span>
<span data-ttu-id="0f817-120">az md5sum ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="0f817-120">check the md5sum</span></span>

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

### <span data-ttu-id="0f817-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0f817-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0f817-122">Az egyidejű aszinkron feladatok teljes összege.</span><span class="sxs-lookup"><span data-stu-id="0f817-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="0f817-123">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="0f817-123">The default value is 10.</span></span>

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

### <span data-ttu-id="0f817-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0f817-124">-Context</span></span>
<span data-ttu-id="0f817-125">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="0f817-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="0f817-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f817-126">-DefaultProfile</span></span>
<span data-ttu-id="0f817-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f817-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f817-128">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="0f817-128">-Destination</span></span>
<span data-ttu-id="0f817-129">Cél helyi fájlelérési útja</span><span class="sxs-lookup"><span data-stu-id="0f817-129">Destination local file path.</span></span>

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

### <span data-ttu-id="0f817-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="0f817-130">-FileSystem</span></span>
<span data-ttu-id="0f817-131">FileSystem neve</span><span class="sxs-lookup"><span data-stu-id="0f817-131">FileSystem name</span></span>

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

### <span data-ttu-id="0f817-132">-Force</span><span class="sxs-lookup"><span data-stu-id="0f817-132">-Force</span></span>
<span data-ttu-id="0f817-133">A meglévő blob vagy fájl felülírásának kényszerítése</span><span class="sxs-lookup"><span data-stu-id="0f817-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="0f817-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f817-134">-InputObject</span></span>
<span data-ttu-id="0f817-135">Azure Datalake Gen2 letöltendő elem</span><span class="sxs-lookup"><span data-stu-id="0f817-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="0f817-136">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="0f817-136">-Path</span></span>
<span data-ttu-id="0f817-137">A megadott fájlrendszerben eltávolítandó elérési út.</span><span class="sxs-lookup"><span data-stu-id="0f817-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="0f817-138">Fájl vagy könyvtár lehet a "címtár/file.txt" vagy a "directory1/directory2/" formátummal.</span><span class="sxs-lookup"><span data-stu-id="0f817-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f817-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f817-139">-Confirm</span></span>
<span data-ttu-id="0f817-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f817-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f817-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f817-141">-WhatIf</span></span>
<span data-ttu-id="0f817-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f817-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f817-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f817-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f817-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f817-144">CommonParameters</span></span>
<span data-ttu-id="0f817-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f817-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f817-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f817-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f817-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f817-147">INPUTS</span></span>

### <span data-ttu-id="0f817-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0f817-148">System.String</span></span>

### <span data-ttu-id="0f817-149">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="0f817-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="0f817-150">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0f817-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0f817-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f817-151">OUTPUTS</span></span>

### <span data-ttu-id="0f817-152">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="0f817-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="0f817-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f817-153">NOTES</span></span>

## <span data-ttu-id="0f817-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f817-154">RELATED LINKS</span></span>

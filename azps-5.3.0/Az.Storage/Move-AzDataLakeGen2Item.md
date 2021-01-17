---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467958"
---
# <span data-ttu-id="1783d-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="1783d-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="1783d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1783d-102">SYNOPSIS</span></span>
<span data-ttu-id="1783d-103">Helyezzen át egy fájlt vagy címtárat egy másik fájlba vagy címtárba ugyanabban a Tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="1783d-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="1783d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1783d-104">SYNTAX</span></span>

### <span data-ttu-id="1783d-105">ReceiveManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1783d-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1783d-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="1783d-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1783d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1783d-107">DESCRIPTION</span></span>
<span data-ttu-id="1783d-108">A **Move-AzDataLakeGen2Item** parancsmag egy fájlt vagy tárat áthelyez egy másik fájlba vagy címtárba ugyanabban a Tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="1783d-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="1783d-109">Ez a parancsmag csak akkor működik, ha engedélyezve van a Hierarchikus névtér a Tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="1783d-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="1783d-110">Az ilyen típusú fiók az "-EnableHierarchicalNamespace $true" parancsmag futtatásával $true.</span><span class="sxs-lookup"><span data-stu-id="1783d-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="1783d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1783d-111">EXAMPLES</span></span>

### <span data-ttu-id="1783d-112">1. példa: Hajtás áthelyezése ugyanabban a fájlrendszerben</span><span class="sxs-lookup"><span data-stu-id="1783d-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="1783d-113">Ez a parancs a címtár "dir1" könyvtárát ugyanabban a fájlrendszerben áthelyezi a "dir3" címtárba.</span><span class="sxs-lookup"><span data-stu-id="1783d-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="1783d-114">2. példa: Fájl áthelyezése folyamat szerint egy másik fájlrendszerbe ugyanabban a Tárfiókban kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="1783d-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="1783d-115">Ez a parancs a "filesystem1" fájlban a "dir1/file1" fájlt "dir2/file2" fájlba áthelyezi a "filesystem2" fájlba ugyanabban a Tárfiókban, kérdés nélkül.</span><span class="sxs-lookup"><span data-stu-id="1783d-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="1783d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1783d-116">PARAMETERS</span></span>

### <span data-ttu-id="1783d-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1783d-117">-Context</span></span>
<span data-ttu-id="1783d-118">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="1783d-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="1783d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1783d-119">-DefaultProfile</span></span>
<span data-ttu-id="1783d-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1783d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1783d-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="1783d-121">-DestFileSystem</span></span>
<span data-ttu-id="1783d-122">Dest FileSystem name</span><span class="sxs-lookup"><span data-stu-id="1783d-122">Dest FileSystem name</span></span>

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

### <span data-ttu-id="1783d-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="1783d-123">-DestPath</span></span>
<span data-ttu-id="1783d-124">Dest Blob path</span><span class="sxs-lookup"><span data-stu-id="1783d-124">Dest Blob path</span></span>

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

### <span data-ttu-id="1783d-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="1783d-125">-FileSystem</span></span>
<span data-ttu-id="1783d-126">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="1783d-126">FileSystem name</span></span>

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

### <span data-ttu-id="1783d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="1783d-127">-Force</span></span>
<span data-ttu-id="1783d-128">Kényszerítsen, hogy írja meg a célhelyet.</span><span class="sxs-lookup"><span data-stu-id="1783d-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="1783d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1783d-129">-InputObject</span></span>
<span data-ttu-id="1783d-130">Azure Datalake Gen2 item object to move from.</span><span class="sxs-lookup"><span data-stu-id="1783d-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="1783d-131">-Path</span><span class="sxs-lookup"><span data-stu-id="1783d-131">-Path</span></span>
<span data-ttu-id="1783d-132">A megadott fájlrendszerben annak az elérési útnak a neve, amelyből át kell lépni.</span><span class="sxs-lookup"><span data-stu-id="1783d-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="1783d-133">Fájl vagy címtár lehet "directory/file.txt" vagy "directory1/directory2/" formátumban.</span><span class="sxs-lookup"><span data-stu-id="1783d-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="1783d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1783d-134">-Confirm</span></span>
<span data-ttu-id="1783d-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1783d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1783d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1783d-136">-WhatIf</span></span>
<span data-ttu-id="1783d-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1783d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1783d-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1783d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1783d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1783d-139">CommonParameters</span></span>
<span data-ttu-id="1783d-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1783d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1783d-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1783d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1783d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1783d-142">INPUTS</span></span>

### <span data-ttu-id="1783d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1783d-143">System.String</span></span>

### <span data-ttu-id="1783d-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="1783d-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="1783d-145">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1783d-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1783d-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1783d-146">OUTPUTS</span></span>

### <span data-ttu-id="1783d-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="1783d-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="1783d-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1783d-148">NOTES</span></span>

## <span data-ttu-id="1783d-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1783d-149">RELATED LINKS</span></span>

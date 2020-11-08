---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013153"
---
# <span data-ttu-id="f1f3b-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f1f3b-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="f1f3b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f3b-103">Fájlok vagy könyvtárak áthelyezése egy másik fájlba vagy könyvtárba ugyanabba a tárterület-fiókba.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="f1f3b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1f3b-104">SYNTAX</span></span>

### <span data-ttu-id="f1f3b-105">ReceiveManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1f3b-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1f3b-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="f1f3b-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1f3b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1f3b-107">DESCRIPTION</span></span>
<span data-ttu-id="f1f3b-108">A **Move-AzDataLakeGen2Item** parancsmag egy fájlt vagy könyvtárat áthelyez egy másik fájlba vagy könyvtárba ugyanabba a tárterület-fiókba.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="f1f3b-109">Ez a parancsmag csak akkor működik, ha a tároló fiókhoz engedélyezve van a hierarchikus névtér.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="f1f3b-110">Ezt a típusú fiókot úgy hozhatja létre, hogy a "New-AzStorageAccount" parancsmagot futtatja a "-EnableHierarchicalNamespace $true" paranccsal.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="f1f3b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f1f3b-111">EXAMPLES</span></span>

### <span data-ttu-id="f1f3b-112">Példa 1: fold áthelyezése ugyanazon a fájlrendszerben</span><span class="sxs-lookup"><span data-stu-id="f1f3b-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="f1f3b-113">Ez a parancs a "dir1" könyvtárat a "dir3" könyvtárba helyezi ugyanabba a fájlrendszerbe.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="f1f3b-114">2. példa: fájlok áthúzása egy másik, azonos tárterületet tartalmazó fájlrendszerre az üzenet nélkül</span><span class="sxs-lookup"><span data-stu-id="f1f3b-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="f1f3b-115">Ez a parancs az "filesystem1" fájl "dir1/fájl1" fájljának "" fájljába helyezi az "dir2/fájl2" parancsot a "filesystem2"-ban az ""-ban.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="f1f3b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1f3b-116">PARAMETERS</span></span>

### <span data-ttu-id="f1f3b-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f1f3b-117">-Context</span></span>
<span data-ttu-id="f1f3b-118">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="f1f3b-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="f1f3b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f3b-119">-DefaultProfile</span></span>
<span data-ttu-id="f1f3b-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f3b-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="f1f3b-121">-DestFileSystem</span></span>
<span data-ttu-id="f1f3b-122">Cél FileSystem neve</span><span class="sxs-lookup"><span data-stu-id="f1f3b-122">Dest FileSystem name</span></span>

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

### <span data-ttu-id="f1f3b-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="f1f3b-123">-DestPath</span></span>
<span data-ttu-id="f1f3b-124">Cél blob elérési útja</span><span class="sxs-lookup"><span data-stu-id="f1f3b-124">Dest Blob path</span></span>

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

### <span data-ttu-id="f1f3b-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="f1f3b-125">-FileSystem</span></span>
<span data-ttu-id="f1f3b-126">FileSystem neve</span><span class="sxs-lookup"><span data-stu-id="f1f3b-126">FileSystem name</span></span>

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

### <span data-ttu-id="f1f3b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f1f3b-127">-Force</span></span>
<span data-ttu-id="f1f3b-128">Kényszerítés a cél megírására.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="f1f3b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1f3b-129">-InputObject</span></span>
<span data-ttu-id="f1f3b-130">Azure Datalake Gen2 elem objektumának áthelyezése.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="f1f3b-131">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="f1f3b-131">-Path</span></span>
<span data-ttu-id="f1f3b-132">A megadott filesystem elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="f1f3b-133">Fájl vagy könyvtár lehet a "címtár/file.txt" vagy a "directory1/directory2/" formátummal.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="f1f3b-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1f3b-134">-Confirm</span></span>
<span data-ttu-id="f1f3b-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1f3b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1f3b-136">-WhatIf</span></span>
<span data-ttu-id="f1f3b-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1f3b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1f3b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f3b-139">CommonParameters</span></span>
<span data-ttu-id="f1f3b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1f3b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f3b-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f3b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f3b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1f3b-142">INPUTS</span></span>

### <span data-ttu-id="f1f3b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f1f3b-143">System.String</span></span>

### <span data-ttu-id="f1f3b-144">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f1f3b-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="f1f3b-145">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f1f3b-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f1f3b-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1f3b-146">OUTPUTS</span></span>

### <span data-ttu-id="f1f3b-147">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f1f3b-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="f1f3b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1f3b-148">NOTES</span></span>

## <span data-ttu-id="f1f3b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1f3b-149">RELATED LINKS</span></span>

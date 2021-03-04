---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 2d3db18c49d29cabb8f6459adcd46a9c0242c02f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933601"
---
# <span data-ttu-id="f46f6-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f46f6-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="f46f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f46f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f46f6-103">Fájl vagy címtár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f46f6-103">Remove a file or directory.</span></span>

## <span data-ttu-id="f46f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f46f6-104">SYNTAX</span></span>

### <span data-ttu-id="f46f6-105">ReceiveManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f46f6-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f46f6-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="f46f6-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f46f6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f46f6-107">DESCRIPTION</span></span>
<span data-ttu-id="f46f6-108">A **Remove-AzDataLakeGen2Item** parancsmag eltávolít egy fájlt vagy címtárat egy tárfiókból.</span><span class="sxs-lookup"><span data-stu-id="f46f6-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="f46f6-109">Ez a parancsmag csak akkor működik, ha engedélyezve van a Hierarchikus névtér a Tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f46f6-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="f46f6-110">Az ilyen típusú fiók az "-EnableHierarchicalNamespace $true" parancsmag futtatásával $true.</span><span class="sxs-lookup"><span data-stu-id="f46f6-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="f46f6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f46f6-111">EXAMPLES</span></span>

### <span data-ttu-id="f46f6-112">1. példa: Címtár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f46f6-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="f46f6-113">Ez a parancs eltávolítja a címtárat a fájlrendszerből.</span><span class="sxs-lookup"><span data-stu-id="f46f6-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="f46f6-114">2. példa: Fájl eltávolítása kérdés nélkül</span><span class="sxs-lookup"><span data-stu-id="f46f6-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="f46f6-115">Ez a parancs kérés nélkül eltávolítja a címtárat a fájlrendszerből.</span><span class="sxs-lookup"><span data-stu-id="f46f6-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="f46f6-116">3. példa: A fájlrendszer összes elemének eltávolítása folyamatban</span><span class="sxs-lookup"><span data-stu-id="f46f6-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="f46f6-117">Ez a parancs eltávolítja az összes elemet a filesystem with pipeline.</span><span class="sxs-lookup"><span data-stu-id="f46f6-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="f46f6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f46f6-118">PARAMETERS</span></span>

### <span data-ttu-id="f46f6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f46f6-119">-AsJob</span></span>
<span data-ttu-id="f46f6-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f46f6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f46f6-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f46f6-121">-Context</span></span>
<span data-ttu-id="f46f6-122">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="f46f6-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="f46f6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46f6-123">-DefaultProfile</span></span>
<span data-ttu-id="f46f6-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f46f6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f46f6-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="f46f6-125">-FileSystem</span></span>
<span data-ttu-id="f46f6-126">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="f46f6-126">FileSystem name</span></span>

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

### <span data-ttu-id="f46f6-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f46f6-127">-Force</span></span>
<span data-ttu-id="f46f6-128">A Fájlrendszer és a benne található összes tartalom eltávolításának kényszerítve</span><span class="sxs-lookup"><span data-stu-id="f46f6-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="f46f6-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f46f6-129">-InputObject</span></span>
<span data-ttu-id="f46f6-130">Eltávolítható Azure Datalake Gen2-elemobjektum.</span><span class="sxs-lookup"><span data-stu-id="f46f6-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="f46f6-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f46f6-131">-PassThru</span></span>
<span data-ttu-id="f46f6-132">Annak visszaadése, hogy a megadott fájlrendszer eltávolítása sikeresen megtörtént-e</span><span class="sxs-lookup"><span data-stu-id="f46f6-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="f46f6-133">-Path</span><span class="sxs-lookup"><span data-stu-id="f46f6-133">-Path</span></span>
<span data-ttu-id="f46f6-134">A megadott fájlrendszer eltávolítható elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f46f6-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="f46f6-135">Fájl vagy címtár lehet "directory/file.txt" vagy "directory1/directory2/" formátumban.</span><span class="sxs-lookup"><span data-stu-id="f46f6-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="f46f6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f46f6-136">-Confirm</span></span>
<span data-ttu-id="f46f6-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f46f6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f46f6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f46f6-138">-WhatIf</span></span>
<span data-ttu-id="f46f6-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f46f6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f46f6-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f46f6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f46f6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46f6-141">CommonParameters</span></span>
<span data-ttu-id="f46f6-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46f6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46f6-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f46f6-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46f6-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f46f6-144">INPUTS</span></span>

### <span data-ttu-id="f46f6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f46f6-145">System.String</span></span>

### <span data-ttu-id="f46f6-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f46f6-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="f46f6-147">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f46f6-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f46f6-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f46f6-148">OUTPUTS</span></span>

### <span data-ttu-id="f46f6-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f46f6-149">System.Boolean</span></span>

## <span data-ttu-id="f46f6-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f46f6-150">NOTES</span></span>

## <span data-ttu-id="f46f6-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f46f6-151">RELATED LINKS</span></span>

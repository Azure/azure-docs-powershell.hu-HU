---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182073"
---
# <span data-ttu-id="07cb8-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="07cb8-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="07cb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="07cb8-103">Fájlok vagy könyvtárak eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="07cb8-103">Remove a file or directory.</span></span>

## <span data-ttu-id="07cb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07cb8-104">SYNTAX</span></span>

### <span data-ttu-id="07cb8-105">ReceiveManual (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07cb8-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07cb8-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="07cb8-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07cb8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="07cb8-107">DESCRIPTION</span></span>
<span data-ttu-id="07cb8-108">A **Remove-AzDataLakeGen2Item** parancsmag eltávolít egy fájlt vagy könyvtárat egy tárterület-fiókból.</span><span class="sxs-lookup"><span data-stu-id="07cb8-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="07cb8-109">Ez a parancsmag csak akkor működik, ha a tároló fiókhoz engedélyezve van a hierarchikus névtér.</span><span class="sxs-lookup"><span data-stu-id="07cb8-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="07cb8-110">Ezt a típusú fiókot úgy hozhatja létre, hogy a "New-AzStorageAccount" parancsmagot futtatja a "-EnableHierarchicalNamespace $true" paranccsal.</span><span class="sxs-lookup"><span data-stu-id="07cb8-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="07cb8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="07cb8-111">EXAMPLES</span></span>

### <span data-ttu-id="07cb8-112">Példa 1: címtár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="07cb8-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="07cb8-113">Ez a parancs eltávolítja a könyvtárat egy fájlrendszerből.</span><span class="sxs-lookup"><span data-stu-id="07cb8-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="07cb8-114">2. példa: fájl eltávolítása üzenet nélkül</span><span class="sxs-lookup"><span data-stu-id="07cb8-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="07cb8-115">Ez a parancs a könyvtárt a fájlrendszerből, a kérdés nélkül távolítja el.</span><span class="sxs-lookup"><span data-stu-id="07cb8-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="07cb8-116">3. példa: a fájlrendszer minden elemének eltávolítása a csővezetéktel</span><span class="sxs-lookup"><span data-stu-id="07cb8-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="07cb8-117">Ezzel a paranccsal a fájlrendszer minden elemét eltávolítja a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="07cb8-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="07cb8-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07cb8-118">PARAMETERS</span></span>

### <span data-ttu-id="07cb8-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07cb8-119">-AsJob</span></span>
<span data-ttu-id="07cb8-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="07cb8-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07cb8-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="07cb8-121">-Context</span></span>
<span data-ttu-id="07cb8-122">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="07cb8-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="07cb8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07cb8-123">-DefaultProfile</span></span>
<span data-ttu-id="07cb8-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07cb8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07cb8-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="07cb8-125">-FileSystem</span></span>
<span data-ttu-id="07cb8-126">FileSystem neve</span><span class="sxs-lookup"><span data-stu-id="07cb8-126">FileSystem name</span></span>

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

### <span data-ttu-id="07cb8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="07cb8-127">-Force</span></span>
<span data-ttu-id="07cb8-128">A fájlrendszer és a benne lévő összes tartalom eltávolításának kényszerítése</span><span class="sxs-lookup"><span data-stu-id="07cb8-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="07cb8-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07cb8-129">-InputObject</span></span>
<span data-ttu-id="07cb8-130">Az Azure Datalake Gen2 elem objektuma eltávolítandó.</span><span class="sxs-lookup"><span data-stu-id="07cb8-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="07cb8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07cb8-131">-PassThru</span></span>
<span data-ttu-id="07cb8-132">A megadott fájlrendszer sikeres eltávolításának visszaadása</span><span class="sxs-lookup"><span data-stu-id="07cb8-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="07cb8-133">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="07cb8-133">-Path</span></span>
<span data-ttu-id="07cb8-134">A megadott fájlrendszerben eltávolítandó elérési út.</span><span class="sxs-lookup"><span data-stu-id="07cb8-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="07cb8-135">Fájl vagy könyvtár lehet a "címtár/file.txt" vagy a "directory1/directory2/" formátummal.</span><span class="sxs-lookup"><span data-stu-id="07cb8-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="07cb8-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="07cb8-136">-Confirm</span></span>
<span data-ttu-id="07cb8-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07cb8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07cb8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07cb8-138">-WhatIf</span></span>
<span data-ttu-id="07cb8-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="07cb8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07cb8-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07cb8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07cb8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07cb8-141">CommonParameters</span></span>
<span data-ttu-id="07cb8-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07cb8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07cb8-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07cb8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07cb8-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07cb8-144">INPUTS</span></span>

### <span data-ttu-id="07cb8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="07cb8-145">System.String</span></span>

### <span data-ttu-id="07cb8-146">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="07cb8-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="07cb8-147">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="07cb8-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="07cb8-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07cb8-148">OUTPUTS</span></span>

### <span data-ttu-id="07cb8-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="07cb8-149">System.Boolean</span></span>

## <span data-ttu-id="07cb8-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07cb8-150">NOTES</span></span>

## <span data-ttu-id="07cb8-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07cb8-151">RELATED LINKS</span></span>

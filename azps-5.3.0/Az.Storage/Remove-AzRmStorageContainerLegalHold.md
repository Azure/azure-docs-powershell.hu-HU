---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376192"
---
# <span data-ttu-id="12477-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="12477-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="12477-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12477-102">SYNOPSIS</span></span>
<span data-ttu-id="12477-103">Jogi holdcímkék eltávolítása egy tároló blobtárolóból</span><span class="sxs-lookup"><span data-stu-id="12477-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="12477-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="12477-104">SYNTAX</span></span>

### <span data-ttu-id="12477-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12477-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12477-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="12477-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12477-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="12477-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12477-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="12477-108">DESCRIPTION</span></span>
<span data-ttu-id="12477-109">A **Remove-AzRmStorageContainerLegalHold** parancsmag eltávolítja a jogi visszatartás címkéit egy tároló blobtárolóból</span><span class="sxs-lookup"><span data-stu-id="12477-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="12477-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="12477-110">EXAMPLES</span></span>

### <span data-ttu-id="12477-111">1. példa: Jogi holdcímkék eltávolítása tárterület blobtárolóból tárfióknévvel és tárolónévvel</span><span class="sxs-lookup"><span data-stu-id="12477-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="12477-112">Ez a parancs eltávolítja a jogi tárolási címkéket egy tárfiók nevét és tárolónevét tartalmazó tár blobtárolóból.</span><span class="sxs-lookup"><span data-stu-id="12477-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="12477-113">2. példa: Jogi holdcímkék eltávolítása tárterület blobtárolóból Tárfiók-objektummal és tárolónévvel</span><span class="sxs-lookup"><span data-stu-id="12477-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="12477-114">Ez a parancs eltávolítja a jogi tárolási címkéket egy Tárfiók-objektumot és tároló nevét tartalmazó tár blobtárolóból.</span><span class="sxs-lookup"><span data-stu-id="12477-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="12477-115">3. példa: Jogi holdcímkék eltávolítása egy folyamatban lévő tárfiók összes tár blobtárolóból</span><span class="sxs-lookup"><span data-stu-id="12477-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="12477-116">Ez a parancs eltávolítja a jogi tárterületcímkéket egy folyamatban lévő tárfiók összes tárterület-blobtárolóból.</span><span class="sxs-lookup"><span data-stu-id="12477-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="12477-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12477-117">PARAMETERS</span></span>

### <span data-ttu-id="12477-118">-Container</span><span class="sxs-lookup"><span data-stu-id="12477-118">-Container</span></span>
<span data-ttu-id="12477-119">Tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="12477-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12477-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12477-120">-DefaultProfile</span></span>
<span data-ttu-id="12477-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12477-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12477-122">-Name</span><span class="sxs-lookup"><span data-stu-id="12477-122">-Name</span></span>
<span data-ttu-id="12477-123">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="12477-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12477-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12477-124">-ResourceGroupName</span></span>
<span data-ttu-id="12477-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="12477-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12477-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="12477-126">-StorageAccount</span></span>
<span data-ttu-id="12477-127">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="12477-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12477-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="12477-128">-StorageAccountName</span></span>
<span data-ttu-id="12477-129">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="12477-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12477-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="12477-130">-Tag</span></span>
<span data-ttu-id="12477-131">Container LegalHold Tags</span><span class="sxs-lookup"><span data-stu-id="12477-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12477-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12477-132">-Confirm</span></span>
<span data-ttu-id="12477-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="12477-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12477-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12477-134">-WhatIf</span></span>
<span data-ttu-id="12477-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="12477-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12477-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12477-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12477-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12477-137">CommonParameters</span></span>
<span data-ttu-id="12477-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12477-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12477-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12477-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12477-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12477-140">INPUTS</span></span>

### <span data-ttu-id="12477-141">System.String</span><span class="sxs-lookup"><span data-stu-id="12477-141">System.String</span></span>

### <span data-ttu-id="12477-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="12477-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="12477-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="12477-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="12477-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12477-144">OUTPUTS</span></span>

### <span data-ttu-id="12477-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="12477-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="12477-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="12477-146">NOTES</span></span>

## <span data-ttu-id="12477-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12477-147">RELATED LINKS</span></span>

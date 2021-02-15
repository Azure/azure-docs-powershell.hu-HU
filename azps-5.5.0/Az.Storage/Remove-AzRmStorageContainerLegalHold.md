---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158026"
---
# <span data-ttu-id="cb6a2-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="cb6a2-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="cb6a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb6a2-102">SYNOPSIS</span></span>
<span data-ttu-id="cb6a2-103">Jogi holdcímkék eltávolítása egy tároló blobtárolóból</span><span class="sxs-lookup"><span data-stu-id="cb6a2-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="cb6a2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb6a2-104">SYNTAX</span></span>

### <span data-ttu-id="cb6a2-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb6a2-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb6a2-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cb6a2-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb6a2-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="cb6a2-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb6a2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb6a2-108">DESCRIPTION</span></span>
<span data-ttu-id="cb6a2-109">A **Remove-AzRmStorageContainerLegalHold** parancsmag eltávolítja a jogi visszatartás címkéit egy tároló blobtárolóból</span><span class="sxs-lookup"><span data-stu-id="cb6a2-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="cb6a2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb6a2-110">EXAMPLES</span></span>

### <span data-ttu-id="cb6a2-111">1. példa: Jogi holdcímkék eltávolítása egy tár blobtárolóból tárfiók nevével és tárolónévvel</span><span class="sxs-lookup"><span data-stu-id="cb6a2-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="cb6a2-112">Ez a parancs eltávolítja a jogi tárolási címkéket egy tárfiók nevét és tárolónevét tartalmazó tár blobtárolóból.</span><span class="sxs-lookup"><span data-stu-id="cb6a2-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="cb6a2-113">2. példa: Jogi holdcímkék eltávolítása egy Tárfiók-objektummal és tárolónévvel egy tároló blobtárolóból</span><span class="sxs-lookup"><span data-stu-id="cb6a2-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="cb6a2-114">Ez a parancs eltávolítja a jogi tárolási címkéket egy Tárfiók-objektumot és tároló nevét tartalmazó tár blobtárolóból.</span><span class="sxs-lookup"><span data-stu-id="cb6a2-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="cb6a2-115">3. példa: Jogi holdcímkék eltávolítása egy folyamatban lévő tárfiók összes tár blobtárolóból</span><span class="sxs-lookup"><span data-stu-id="cb6a2-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="cb6a2-116">Ez a parancs eltávolítja a jogi tárterületcímkéket egy folyamatban lévő tárfiók összes tárterület-blobtárolóból.</span><span class="sxs-lookup"><span data-stu-id="cb6a2-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="cb6a2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb6a2-117">PARAMETERS</span></span>

### <span data-ttu-id="cb6a2-118">-Container</span><span class="sxs-lookup"><span data-stu-id="cb6a2-118">-Container</span></span>
<span data-ttu-id="cb6a2-119">Tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="cb6a2-119">Storage container object</span></span>

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

### <span data-ttu-id="cb6a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb6a2-120">-DefaultProfile</span></span>
<span data-ttu-id="cb6a2-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb6a2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb6a2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cb6a2-122">-Name</span></span>
<span data-ttu-id="cb6a2-123">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="cb6a2-123">Container Name</span></span>

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

### <span data-ttu-id="cb6a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb6a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="cb6a2-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cb6a2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="cb6a2-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb6a2-126">-StorageAccount</span></span>
<span data-ttu-id="cb6a2-127">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="cb6a2-127">Storage account object</span></span>

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

### <span data-ttu-id="cb6a2-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cb6a2-128">-StorageAccountName</span></span>
<span data-ttu-id="cb6a2-129">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="cb6a2-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="cb6a2-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb6a2-130">-Tag</span></span>
<span data-ttu-id="cb6a2-131">Container LegalHold Tags</span><span class="sxs-lookup"><span data-stu-id="cb6a2-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="cb6a2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb6a2-132">-Confirm</span></span>
<span data-ttu-id="cb6a2-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cb6a2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb6a2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb6a2-134">-WhatIf</span></span>
<span data-ttu-id="cb6a2-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cb6a2-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb6a2-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb6a2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb6a2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb6a2-137">CommonParameters</span></span>
<span data-ttu-id="cb6a2-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb6a2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb6a2-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb6a2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb6a2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb6a2-140">INPUTS</span></span>

### <span data-ttu-id="cb6a2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cb6a2-141">System.String</span></span>

### <span data-ttu-id="cb6a2-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb6a2-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="cb6a2-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="cb6a2-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="cb6a2-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb6a2-144">OUTPUTS</span></span>

### <span data-ttu-id="cb6a2-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="cb6a2-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="cb6a2-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb6a2-146">NOTES</span></span>

## <span data-ttu-id="cb6a2-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb6a2-147">RELATED LINKS</span></span>

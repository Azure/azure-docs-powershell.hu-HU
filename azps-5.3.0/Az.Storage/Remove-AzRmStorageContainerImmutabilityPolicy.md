---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467079"
---
# <span data-ttu-id="5e216-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5e216-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="5e216-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e216-102">SYNOPSIS</span></span>
<span data-ttu-id="5e216-103">Feloldott házirendet tartalmazó tár blobtároló ImmutabilityPolicy-ának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5e216-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="5e216-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e216-104">SYNTAX</span></span>

### <span data-ttu-id="5e216-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e216-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e216-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5e216-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e216-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="5e216-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e216-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="5e216-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e216-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e216-109">DESCRIPTION</span></span>
<span data-ttu-id="5e216-110">A **Remove-AzRmStorageContainerImmutabilityPolicy parancsmag** eltávolítja egy tárterület blobtárolójában a ImmutabilityPolicy házirendet.</span><span class="sxs-lookup"><span data-stu-id="5e216-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="5e216-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e216-111">EXAMPLES</span></span>

### <span data-ttu-id="5e216-112">1. példa: Tárfiók nevét és tárolónevét tartalmazó tár blobtároló nem zárolt ImmutabilityPolicy eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5e216-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="5e216-113">Ez a parancs eltávolítja a tárfiók nevét és tárolónevét tartalmazó tár blobtároló nem zárolt ImmutabilityPolicy-ját.</span><span class="sxs-lookup"><span data-stu-id="5e216-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="5e216-114">2. példa: Tárfiók-objektummal eltávolíthatja a tárterület blobtárolója nem zárolt ImmutabilityPolicy-ját</span><span class="sxs-lookup"><span data-stu-id="5e216-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="5e216-115">Ez a parancs eltávolítja a Tárfiók-objektummal együtt egy tárterület blobtárolója nem zárolt ImmutabilityPolicy-ját.</span><span class="sxs-lookup"><span data-stu-id="5e216-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="5e216-116">3. példa: Tár blobtároló nem zárolt ImmutabilityPolicy-ának eltávolítása tárolóobjektummal</span><span class="sxs-lookup"><span data-stu-id="5e216-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="5e216-117">Ez a parancs eltávolítja a Tártároló objektumot tartalmazó tároló blobtároló nem zárolt ImmutabilityPolicy-ját.</span><span class="sxs-lookup"><span data-stu-id="5e216-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="5e216-118">4. példa: Tárterület blobtároló nem zárolt ImmutabilityPolicy-ának eltávolítása ImmutabilityPolicy objektummal</span><span class="sxs-lookup"><span data-stu-id="5e216-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="5e216-119">Ez a parancs eltávolítja a Tárterület blobtárolója nem zárolt ImmutabilityPolicy-ját, a ImmutabilityPolicy objektummal.</span><span class="sxs-lookup"><span data-stu-id="5e216-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="5e216-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e216-120">PARAMETERS</span></span>

### <span data-ttu-id="5e216-121">-Container</span><span class="sxs-lookup"><span data-stu-id="5e216-121">-Container</span></span>
<span data-ttu-id="5e216-122">Tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="5e216-122">Storage container object</span></span>

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

### <span data-ttu-id="5e216-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="5e216-123">-ContainerName</span></span>
<span data-ttu-id="5e216-124">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="5e216-124">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e216-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e216-125">-DefaultProfile</span></span>
<span data-ttu-id="5e216-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e216-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e216-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="5e216-127">-Etag</span></span>
<span data-ttu-id="5e216-128">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="5e216-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e216-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e216-129">-InputObject</span></span>
<span data-ttu-id="5e216-130">Feloldott ImmutabilityPolicy objektum eltávolítható</span><span class="sxs-lookup"><span data-stu-id="5e216-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e216-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e216-131">-ResourceGroupName</span></span>
<span data-ttu-id="5e216-132">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5e216-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="5e216-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e216-133">-StorageAccount</span></span>
<span data-ttu-id="5e216-134">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="5e216-134">Storage account object</span></span>

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

### <span data-ttu-id="5e216-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5e216-135">-StorageAccountName</span></span>
<span data-ttu-id="5e216-136">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="5e216-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="5e216-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e216-137">-Confirm</span></span>
<span data-ttu-id="5e216-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5e216-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e216-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e216-139">-WhatIf</span></span>
<span data-ttu-id="5e216-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5e216-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e216-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e216-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e216-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e216-142">CommonParameters</span></span>
<span data-ttu-id="5e216-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e216-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e216-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e216-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e216-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e216-145">INPUTS</span></span>

### <span data-ttu-id="5e216-146">System.String</span><span class="sxs-lookup"><span data-stu-id="5e216-146">System.String</span></span>

### <span data-ttu-id="5e216-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e216-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="5e216-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="5e216-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="5e216-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5e216-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="5e216-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e216-150">OUTPUTS</span></span>

### <span data-ttu-id="5e216-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5e216-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="5e216-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e216-152">NOTES</span></span>

## <span data-ttu-id="5e216-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e216-153">RELATED LINKS</span></span>

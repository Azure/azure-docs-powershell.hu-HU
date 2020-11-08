---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014672"
---
# <span data-ttu-id="cd9ec-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cd9ec-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="cd9ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9ec-103">ImmutabilityPolicy-tároló blob-tárolójának eltávolítása a zárolt házirenddel</span><span class="sxs-lookup"><span data-stu-id="cd9ec-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="cd9ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd9ec-104">SYNTAX</span></span>

### <span data-ttu-id="cd9ec-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd9ec-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd9ec-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cd9ec-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd9ec-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="cd9ec-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd9ec-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="cd9ec-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd9ec-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd9ec-109">DESCRIPTION</span></span>
<span data-ttu-id="cd9ec-110">A **Remove-AzRmStorageContainerImmutabilityPolicy** parancsmag eltávolítja a ImmutabilityPolicy-tároló blob-tárolóját a zárolt házirendkel.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="cd9ec-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cd9ec-111">EXAMPLES</span></span>

### <span data-ttu-id="cd9ec-112">1. példa: a tárterület-tároló blob-tárolójának zárolt ImmutabilityPolicy eltávolítása a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="cd9ec-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="cd9ec-113">Ez a parancs eltávolítja a ImmutabilityPolicy-tároló blob-tárolójának zárolt zárolását a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="cd9ec-114">2. példa: a tárterület-tárolóból kioldott ImmutabilityPolicy eltávolítása a Storage Account objektummal</span><span class="sxs-lookup"><span data-stu-id="cd9ec-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="cd9ec-115">Ez a parancs eltávolítja a ImmutabilityPolicy-tároló blob-tárolójának zárolt zárolását.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="cd9ec-116">3. példa: ImmutabilityPolicy eltávolítása a tároló blob-tárolóból, a tároló objektummal</span><span class="sxs-lookup"><span data-stu-id="cd9ec-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="cd9ec-117">Ez a parancs eltávolítja a tároló blob-tároló zárolt ImmutabilityPolicy a tároló tároló objektummal.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="cd9ec-118">4. példa: a ImmutabilityPolicy-tárolók zárolásának megszüntetése a ImmutabilityPolicy objektummal</span><span class="sxs-lookup"><span data-stu-id="cd9ec-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="cd9ec-119">Ez a parancs eltávolítja a ImmutabilityPolicy-tároló blob-tárolójának zárolt zárolását a ImmutabilityPolicy objektummal.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="cd9ec-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd9ec-120">PARAMETERS</span></span>

### <span data-ttu-id="cd9ec-121">-Container</span><span class="sxs-lookup"><span data-stu-id="cd9ec-121">-Container</span></span>
<span data-ttu-id="cd9ec-122">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="cd9ec-122">Storage container object</span></span>

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

### <span data-ttu-id="cd9ec-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="cd9ec-123">-ContainerName</span></span>
<span data-ttu-id="cd9ec-124">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="cd9ec-124">Container Name</span></span>

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

### <span data-ttu-id="cd9ec-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9ec-125">-DefaultProfile</span></span>
<span data-ttu-id="cd9ec-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd9ec-127">-ETAG</span><span class="sxs-lookup"><span data-stu-id="cd9ec-127">-Etag</span></span>
<span data-ttu-id="cd9ec-128">A Immutability házirend ETAG.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="cd9ec-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd9ec-129">-InputObject</span></span>
<span data-ttu-id="cd9ec-130">Zárolt ImmutabilityPolicy objektum eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cd9ec-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="cd9ec-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd9ec-131">-ResourceGroupName</span></span>
<span data-ttu-id="cd9ec-132">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="cd9ec-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd9ec-133">-StorageAccount</span></span>
<span data-ttu-id="cd9ec-134">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="cd9ec-134">Storage account object</span></span>

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

### <span data-ttu-id="cd9ec-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cd9ec-135">-StorageAccountName</span></span>
<span data-ttu-id="cd9ec-136">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="cd9ec-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd9ec-137">-Confirm</span></span>
<span data-ttu-id="cd9ec-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd9ec-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd9ec-139">-WhatIf</span></span>
<span data-ttu-id="cd9ec-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd9ec-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd9ec-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd9ec-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9ec-142">CommonParameters</span></span>
<span data-ttu-id="cd9ec-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd9ec-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9ec-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9ec-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9ec-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd9ec-145">INPUTS</span></span>

### <span data-ttu-id="cd9ec-146">System. String</span><span class="sxs-lookup"><span data-stu-id="cd9ec-146">System.String</span></span>

### <span data-ttu-id="cd9ec-147">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd9ec-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="cd9ec-148">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="cd9ec-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="cd9ec-149">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cd9ec-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="cd9ec-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd9ec-150">OUTPUTS</span></span>

### <span data-ttu-id="cd9ec-151">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cd9ec-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="cd9ec-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd9ec-152">NOTES</span></span>

## <span data-ttu-id="cd9ec-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd9ec-153">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011225"
---
# <span data-ttu-id="3e1f2-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3e1f2-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="3e1f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1f2-103">ImmutabilityPolicy-tárolók létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="3e1f2-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="3e1f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e1f2-104">SYNTAX</span></span>

### <span data-ttu-id="3e1f2-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e1f2-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e1f2-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="3e1f2-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e1f2-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3e1f2-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e1f2-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="3e1f2-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e1f2-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="3e1f2-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e1f2-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="3e1f2-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e1f2-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="3e1f2-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e1f2-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="3e1f2-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e1f2-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e1f2-113">DESCRIPTION</span></span>
<span data-ttu-id="3e1f2-114">A **set-AzRmStorageContainerImmutabilityPolicy** parancsmag ImmutabilityPolicy-tárolókat hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="3e1f2-115">Példák</span><span class="sxs-lookup"><span data-stu-id="3e1f2-115">EXAMPLES</span></span>

### <span data-ttu-id="3e1f2-116">1. példa: ImmutabilityPolicy létrehozása vagy frissítése a tároló blob-tárolójában a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="3e1f2-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="3e1f2-117">Ezzel a paranccsal létrehozhatja vagy frissítheti a ImmutabilityPolicy-tároló blob-tárolóját a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="3e1f2-118">2. példa: ImmutabilityPolicy-tároló kiterjesztése a Storage Account objektummal</span><span class="sxs-lookup"><span data-stu-id="3e1f2-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="3e1f2-119">Ez a parancs a tárterület-tárolót tartalmazó ImmutabilityPolicy-tárolót (Storage Account Object-objektumot) bővíti.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="3e1f2-120">A ImmutabilityPolicy meghosszabbítása csak akkor futtatható, ha a ImmutabilityPolicy zárolva van.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="3e1f2-121">3. példa: ImmutabilityPolicy frissítése</span><span class="sxs-lookup"><span data-stu-id="3e1f2-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="3e1f2-122">Ez a parancs a ImmutabilityPolicy 3 alkalommal frissíti a tárterület-tároló blob-tárolóját, így a ImmutabilityPeriod 12 napig nem ETAG, majd a ImmutabilityPeriod 9 napig tart a ETAG, végül a AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="3e1f2-123">4. példa: ImmutabilityPolicy-tároló kiterjesztése a ImmutabilityPolicy objektummal</span><span class="sxs-lookup"><span data-stu-id="3e1f2-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="3e1f2-124">Ez a parancs a ImmutabilityPolicy-tároló blob-tárolójának ImmutabilityPolicy-objektummal való meghosszabbítását.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="3e1f2-125">A ImmutabilityPolicy meghosszabbítása csak akkor futtatható, ha a ImmutabilityPolicy zárolva van.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="3e1f2-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e1f2-126">PARAMETERS</span></span>

### <span data-ttu-id="3e1f2-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="3e1f2-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="3e1f2-128">Ezt a tulajdonságot csak a zárolt időalapú adatmegőrzési házirendek esetében lehet módosítani.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="3e1f2-129">Ezzel a tulajdonsággal engedélyezve van az új blokkok hozzáfűzése a immutability-védelem és a megfelelőség megőrzése mellett.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="3e1f2-130">Csak az új blokkok adhatók hozzá, és a meglévő blokkok nem módosíthatók vagy törölhetők.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1f2-131">-Container</span><span class="sxs-lookup"><span data-stu-id="3e1f2-131">-Container</span></span>
<span data-ttu-id="3e1f2-132">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="3e1f2-132">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1f2-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3e1f2-133">-ContainerName</span></span>
<span data-ttu-id="3e1f2-134">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="3e1f2-134">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1f2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1f2-135">-DefaultProfile</span></span>
<span data-ttu-id="3e1f2-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e1f2-137">-ETAG</span><span class="sxs-lookup"><span data-stu-id="3e1f2-137">-Etag</span></span>
<span data-ttu-id="3e1f2-138">A Immutability házirend ETAG.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-138">Immutability policy etag.</span></span> <span data-ttu-id="3e1f2-139">Ha-ExtendPolicy nincs megadva, a ETAG nem kötelező. Máskülönben ETAG van szükség.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1f2-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="3e1f2-140">-ExtendPolicy</span></span>
<span data-ttu-id="3e1f2-141">Adja meg a ExtendPolicy egy meglévő ImmutabilityPolicy meghosszabbításához.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="3e1f2-142">Ha a ImmutabilityPolicy zárolva van, akkor csak akkor lehet hosszabb.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1f2-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="3e1f2-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="3e1f2-144">Immutability az időszak létrehozása óta a napokban.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-144">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1f2-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e1f2-145">-InputObject</span></span>
<span data-ttu-id="3e1f2-146">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="3e1f2-146">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1f2-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1f2-147">-ResourceGroupName</span></span>
<span data-ttu-id="3e1f2-148">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1f2-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3e1f2-149">-StorageAccount</span></span>
<span data-ttu-id="3e1f2-150">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="3e1f2-150">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1f2-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e1f2-151">-StorageAccountName</span></span>
<span data-ttu-id="3e1f2-152">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-152">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1f2-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e1f2-153">-Confirm</span></span>
<span data-ttu-id="3e1f2-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e1f2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e1f2-155">-WhatIf</span></span>
<span data-ttu-id="3e1f2-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e1f2-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e1f2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e1f2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1f2-158">CommonParameters</span></span>
<span data-ttu-id="3e1f2-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e1f2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1f2-160">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e1f2-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1f2-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e1f2-161">INPUTS</span></span>

### <span data-ttu-id="3e1f2-162">System. String</span><span class="sxs-lookup"><span data-stu-id="3e1f2-162">System.String</span></span>

### <span data-ttu-id="3e1f2-163">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3e1f2-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3e1f2-164">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="3e1f2-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="3e1f2-165">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3e1f2-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="3e1f2-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e1f2-166">OUTPUTS</span></span>

### <span data-ttu-id="3e1f2-167">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3e1f2-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="3e1f2-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e1f2-168">NOTES</span></span>

## <span data-ttu-id="3e1f2-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e1f2-169">RELATED LINKS</span></span>

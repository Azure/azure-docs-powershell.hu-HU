---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c216765657cc87c958cc20dd0f2014f0e1c16970
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839852"
---
# <span data-ttu-id="11db3-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="11db3-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="11db3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11db3-102">SYNOPSIS</span></span>
<span data-ttu-id="11db3-103">ImmutabilityPolicy-tárolók létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="11db3-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="11db3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11db3-104">SYNTAX</span></span>

### <span data-ttu-id="11db3-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11db3-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11db3-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="11db3-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11db3-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="11db3-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11db3-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="11db3-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11db3-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="11db3-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11db3-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="11db3-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11db3-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="11db3-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11db3-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="11db3-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11db3-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="11db3-113">DESCRIPTION</span></span>
<span data-ttu-id="11db3-114">A **set-AzRmStorageContainerImmutabilityPolicy** parancsmag ImmutabilityPolicy-tárolókat hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="11db3-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="11db3-115">Példák</span><span class="sxs-lookup"><span data-stu-id="11db3-115">EXAMPLES</span></span>

### <span data-ttu-id="11db3-116">1. példa: ImmutabilityPolicy létrehozása vagy frissítése a tároló blob-tárolójában a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="11db3-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="11db3-117">Ezzel a paranccsal létrehozhatja vagy frissítheti a ImmutabilityPolicy-tároló blob-tárolóját a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="11db3-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="11db3-118">2. példa: ImmutabilityPolicy-tároló kiterjesztése a Storage Account objektummal</span><span class="sxs-lookup"><span data-stu-id="11db3-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="11db3-119">Ez a parancs a tárterület-tárolót tartalmazó ImmutabilityPolicy-tárolót (Storage Account Object-objektumot) bővíti.</span><span class="sxs-lookup"><span data-stu-id="11db3-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="11db3-120">A ImmutabilityPolicy meghosszabbítása csak akkor futtatható, ha a ImmutabilityPolicy zárolva van.</span><span class="sxs-lookup"><span data-stu-id="11db3-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="11db3-121">3. példa: ImmutabilityPolicyof frissítése tároló blob-tárolóban</span><span class="sxs-lookup"><span data-stu-id="11db3-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="11db3-122">Ez a parancs frissíti a ImmutabilityPolicy-tároló blob-tárolóját (2 alkalommal) a Storage Container objektummal, amely először ImmutabilityPeriod 12 napig tart a ETAG nélkül, majd a ImmutabilityPeriod 9 nap a ETAG.</span><span class="sxs-lookup"><span data-stu-id="11db3-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="11db3-123">4. példa: ImmutabilityPolicy-tároló kiterjesztése a ImmutabilityPolicy objektummal</span><span class="sxs-lookup"><span data-stu-id="11db3-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="11db3-124">Ez a parancs a ImmutabilityPolicy-tároló blob-tárolójának ImmutabilityPolicy-objektummal való meghosszabbítását.</span><span class="sxs-lookup"><span data-stu-id="11db3-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="11db3-125">A ImmutabilityPolicy meghosszabbítása csak akkor futtatható, ha a ImmutabilityPolicy zárolva van.</span><span class="sxs-lookup"><span data-stu-id="11db3-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="11db3-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11db3-126">PARAMETERS</span></span>

### <span data-ttu-id="11db3-127">-Container</span><span class="sxs-lookup"><span data-stu-id="11db3-127">-Container</span></span>
<span data-ttu-id="11db3-128">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="11db3-128">Storage container object</span></span>

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

### <span data-ttu-id="11db3-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="11db3-129">-ContainerName</span></span>
<span data-ttu-id="11db3-130">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="11db3-130">Container Name</span></span>

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

### <span data-ttu-id="11db3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11db3-131">-DefaultProfile</span></span>
<span data-ttu-id="11db3-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11db3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11db3-133">-ETAG</span><span class="sxs-lookup"><span data-stu-id="11db3-133">-Etag</span></span>
<span data-ttu-id="11db3-134">A Immutability házirend ETAG.</span><span class="sxs-lookup"><span data-stu-id="11db3-134">Immutability policy etag.</span></span> <span data-ttu-id="11db3-135">Ha-ExtendPolicy nincs megadva, a ETAG nem kötelező. Máskülönben ETAG van szükség.</span><span class="sxs-lookup"><span data-stu-id="11db3-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="11db3-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="11db3-136">-ExtendPolicy</span></span>
<span data-ttu-id="11db3-137">Adja meg a ExtendPolicy egy meglévő ImmutabilityPolicy meghosszabbításához.</span><span class="sxs-lookup"><span data-stu-id="11db3-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="11db3-138">Ha a ImmutabilityPolicy zárolva van, akkor csak akkor lehet hosszabb.</span><span class="sxs-lookup"><span data-stu-id="11db3-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="11db3-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="11db3-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="11db3-140">Immutability az időszak létrehozása óta a napokban.</span><span class="sxs-lookup"><span data-stu-id="11db3-140">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11db3-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11db3-141">-InputObject</span></span>
<span data-ttu-id="11db3-142">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="11db3-142">Container Name</span></span>

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

### <span data-ttu-id="11db3-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11db3-143">-ResourceGroupName</span></span>
<span data-ttu-id="11db3-144">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="11db3-144">Resource Group Name.</span></span>

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

### <span data-ttu-id="11db3-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="11db3-145">-StorageAccount</span></span>
<span data-ttu-id="11db3-146">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="11db3-146">Storage account object</span></span>

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

### <span data-ttu-id="11db3-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="11db3-147">-StorageAccountName</span></span>
<span data-ttu-id="11db3-148">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="11db3-148">Storage Account Name.</span></span>

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

### <span data-ttu-id="11db3-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11db3-149">-Confirm</span></span>
<span data-ttu-id="11db3-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11db3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11db3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11db3-151">-WhatIf</span></span>
<span data-ttu-id="11db3-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11db3-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11db3-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11db3-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11db3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11db3-154">CommonParameters</span></span>
<span data-ttu-id="11db3-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11db3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11db3-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11db3-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11db3-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11db3-157">INPUTS</span></span>

### <span data-ttu-id="11db3-158">System. String</span><span class="sxs-lookup"><span data-stu-id="11db3-158">System.String</span></span>

### <span data-ttu-id="11db3-159">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11db3-159">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="11db3-160">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="11db3-160">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="11db3-161">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="11db3-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="11db3-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11db3-162">OUTPUTS</span></span>

### <span data-ttu-id="11db3-163">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="11db3-163">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="11db3-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11db3-164">NOTES</span></span>

## <span data-ttu-id="11db3-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11db3-165">RELATED LINKS</span></span>

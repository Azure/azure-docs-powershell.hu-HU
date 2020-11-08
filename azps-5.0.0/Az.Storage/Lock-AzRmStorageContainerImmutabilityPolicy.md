---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186617"
---
# <span data-ttu-id="63fe3-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="63fe3-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="63fe3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="63fe3-103">Tároló blob-tárolók ImmutabilityPolicy zárolása</span><span class="sxs-lookup"><span data-stu-id="63fe3-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="63fe3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63fe3-104">SYNTAX</span></span>

### <span data-ttu-id="63fe3-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63fe3-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63fe3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="63fe3-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63fe3-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="63fe3-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63fe3-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="63fe3-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63fe3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="63fe3-109">DESCRIPTION</span></span>
<span data-ttu-id="63fe3-110">A **Lock-AzRmStorageContainerImmutabilityPolicy** parancsmag zárolja a ImmutabilityPolicy tároló blob-tárolókat.</span><span class="sxs-lookup"><span data-stu-id="63fe3-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="63fe3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="63fe3-111">EXAMPLES</span></span>

### <span data-ttu-id="63fe3-112">1. példa: ImmutabilityPolicy zárolása a tárolási blob-tárolóról a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="63fe3-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="63fe3-113">Ez a parancs a ImmutabilityPolicy-tároló blob-tárolóját rögzíti a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="63fe3-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="63fe3-114">2. példa: ImmutabilityPolicy zárolása tároló blob-tároló zárolása a Storage Account objektummal</span><span class="sxs-lookup"><span data-stu-id="63fe3-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="63fe3-115">Ez a parancs egy ImmutabilityPolicy tároló BLOB-tárolót zárol, a Storage Account objektummal.</span><span class="sxs-lookup"><span data-stu-id="63fe3-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="63fe3-116">3. példa: ImmutabilityPolicyof zárolása tároló blob-tárolóhoz a tároló objektummal</span><span class="sxs-lookup"><span data-stu-id="63fe3-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="63fe3-117">Ez a parancs a tárterület-tároló objektummal ImmutabilityPolicy zárolja a tároló BLOB-tárolót.</span><span class="sxs-lookup"><span data-stu-id="63fe3-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="63fe3-118">Példa 4: ImmutabilityPolicy zárolása ImmutabilityPolicy objektummal</span><span class="sxs-lookup"><span data-stu-id="63fe3-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="63fe3-119">Ez a parancs a ImmutabilityPolicy-tároló (ImmutabilityPolicy objektum) segítségével zárolja a BLOB-tárolót.</span><span class="sxs-lookup"><span data-stu-id="63fe3-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="63fe3-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63fe3-120">PARAMETERS</span></span>

### <span data-ttu-id="63fe3-121">-Container</span><span class="sxs-lookup"><span data-stu-id="63fe3-121">-Container</span></span>
<span data-ttu-id="63fe3-122">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="63fe3-122">Storage container object</span></span>

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

### <span data-ttu-id="63fe3-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="63fe3-123">-ContainerName</span></span>
<span data-ttu-id="63fe3-124">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="63fe3-124">Container Name</span></span>

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

### <span data-ttu-id="63fe3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fe3-125">-DefaultProfile</span></span>
<span data-ttu-id="63fe3-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63fe3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63fe3-127">-ETAG</span><span class="sxs-lookup"><span data-stu-id="63fe3-127">-Etag</span></span>
<span data-ttu-id="63fe3-128">A Immutability házirend ETAG.</span><span class="sxs-lookup"><span data-stu-id="63fe3-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="63fe3-129">-Force</span><span class="sxs-lookup"><span data-stu-id="63fe3-129">-Force</span></span>
<span data-ttu-id="63fe3-130">Kényszeríti a ImmutabilityPolicy eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="63fe3-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="63fe3-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63fe3-131">-InputObject</span></span>
<span data-ttu-id="63fe3-132">ImmutabilityPolicy objektum eltávolítása</span><span class="sxs-lookup"><span data-stu-id="63fe3-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="63fe3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63fe3-133">-ResourceGroupName</span></span>
<span data-ttu-id="63fe3-134">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="63fe3-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="63fe3-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="63fe3-135">-StorageAccount</span></span>
<span data-ttu-id="63fe3-136">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="63fe3-136">Storage account object</span></span>

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

### <span data-ttu-id="63fe3-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="63fe3-137">-StorageAccountName</span></span>
<span data-ttu-id="63fe3-138">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="63fe3-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="63fe3-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="63fe3-139">-Confirm</span></span>
<span data-ttu-id="63fe3-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="63fe3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63fe3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63fe3-141">-WhatIf</span></span>
<span data-ttu-id="63fe3-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="63fe3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63fe3-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63fe3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63fe3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fe3-144">CommonParameters</span></span>
<span data-ttu-id="63fe3-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63fe3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fe3-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63fe3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fe3-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63fe3-147">INPUTS</span></span>

### <span data-ttu-id="63fe3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="63fe3-148">System.String</span></span>

### <span data-ttu-id="63fe3-149">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="63fe3-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="63fe3-150">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="63fe3-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="63fe3-151">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="63fe3-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="63fe3-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63fe3-152">OUTPUTS</span></span>

### <span data-ttu-id="63fe3-153">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="63fe3-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="63fe3-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63fe3-154">NOTES</span></span>

## <span data-ttu-id="63fe3-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63fe3-155">RELATED LINKS</span></span>

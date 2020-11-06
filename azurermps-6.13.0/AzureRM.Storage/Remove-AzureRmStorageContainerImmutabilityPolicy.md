---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 74963ef36a33bed6145d315f5792aa776a36bc7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498159"
---
# <span data-ttu-id="1ca46-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1ca46-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="1ca46-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ca46-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca46-103">ImmutabilityPolicy eltávolítása a blob-tárolókban</span><span class="sxs-lookup"><span data-stu-id="1ca46-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ca46-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ca46-104">SYNTAX</span></span>

### <span data-ttu-id="1ca46-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ca46-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ca46-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1ca46-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ca46-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="1ca46-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ca46-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1ca46-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ca46-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ca46-109">DESCRIPTION</span></span>
<span data-ttu-id="1ca46-110">A **Remove-AzureRmStorageContainerImmutabilityPolicy** parancsmag eltávolítja a ImmutabilityPolicy-tárolók blob-tárolóit.</span><span class="sxs-lookup"><span data-stu-id="1ca46-110">The **Remove-AzureRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="1ca46-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1ca46-111">EXAMPLES</span></span>

### <span data-ttu-id="1ca46-112">1. példa: a ImmutabilityPolicy-tároló blob-tárolójának eltávolítása a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="1ca46-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="1ca46-113">Ez a parancs eltávolítja a ImmutabilityPolicy-tároló blob-tárolójának a tárolási fiók nevével és a tároló nevével való eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="1ca46-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1ca46-114">2. példa: ImmutabilityPolicy-tároló eltávolítása a tárterület-objektummal</span><span class="sxs-lookup"><span data-stu-id="1ca46-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="1ca46-115">Ez a parancs eltávolítja a ImmutabilityPolicy-tároló bináris tárolóját a Storage Account Object objektummal.</span><span class="sxs-lookup"><span data-stu-id="1ca46-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="1ca46-116">3. példa: ImmutabilityPolicyof eltávolítása a tároló blob-tárolóból, a tároló objektummal</span><span class="sxs-lookup"><span data-stu-id="1ca46-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="1ca46-117">Ez a parancs eltávolítja a ImmutabilityPolicy tároló BLOB-tárolót.</span><span class="sxs-lookup"><span data-stu-id="1ca46-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="1ca46-118">Példa 4: ImmutabilityPolicy-tároló eltávolítása a ImmutabilityPolicy objektummal</span><span class="sxs-lookup"><span data-stu-id="1ca46-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzureRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="1ca46-119">Ez a parancs eltávolítja a ImmutabilityPolicy-tároló ImmutabilityPolicy objektummal való eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="1ca46-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="1ca46-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ca46-120">PARAMETERS</span></span>

### <span data-ttu-id="1ca46-121">-Container</span><span class="sxs-lookup"><span data-stu-id="1ca46-121">-Container</span></span>
<span data-ttu-id="1ca46-122">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="1ca46-122">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca46-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1ca46-123">-ContainerName</span></span>
<span data-ttu-id="1ca46-124">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="1ca46-124">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca46-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca46-125">-DefaultProfile</span></span>
<span data-ttu-id="1ca46-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ca46-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca46-127">-ETAG</span><span class="sxs-lookup"><span data-stu-id="1ca46-127">-Etag</span></span>
<span data-ttu-id="1ca46-128">A Immutability házirend ETAG.</span><span class="sxs-lookup"><span data-stu-id="1ca46-128">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca46-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ca46-129">-InputObject</span></span>
<span data-ttu-id="1ca46-130">ImmutabilityPolicy objektum eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1ca46-130">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca46-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ca46-131">-ResourceGroupName</span></span>
<span data-ttu-id="1ca46-132">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1ca46-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca46-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ca46-133">-StorageAccount</span></span>
<span data-ttu-id="1ca46-134">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="1ca46-134">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca46-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1ca46-135">-StorageAccountName</span></span>
<span data-ttu-id="1ca46-136">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="1ca46-136">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca46-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ca46-137">-Confirm</span></span>
<span data-ttu-id="1ca46-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ca46-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca46-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ca46-139">-WhatIf</span></span>
<span data-ttu-id="1ca46-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ca46-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ca46-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ca46-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca46-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca46-142">CommonParameters</span></span>
<span data-ttu-id="1ca46-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ca46-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca46-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ca46-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca46-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ca46-145">INPUTS</span></span>

### <span data-ttu-id="1ca46-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1ca46-146">System.String</span></span>
<span data-ttu-id="1ca46-147">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1ca46-147">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1ca46-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ca46-148">OUTPUTS</span></span>

### <span data-ttu-id="1ca46-149">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1ca46-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1ca46-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ca46-150">NOTES</span></span>

## <span data-ttu-id="1ca46-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ca46-151">RELATED LINKS</span></span>


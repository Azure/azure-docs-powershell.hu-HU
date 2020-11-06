---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/lock-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 726dc9043c1082f97e32da46305cf81192e1806c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491854"
---
# <span data-ttu-id="9f599-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9f599-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="9f599-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f599-102">SYNOPSIS</span></span>
<span data-ttu-id="9f599-103">Tároló blob-tárolók ImmutabilityPolicy zárolása</span><span class="sxs-lookup"><span data-stu-id="9f599-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f599-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f599-104">SYNTAX</span></span>

### <span data-ttu-id="9f599-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f599-105">AccountName (Default)</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f599-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9f599-106">AccountObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f599-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="9f599-107">ContainerObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f599-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="9f599-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f599-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f599-109">DESCRIPTION</span></span>
<span data-ttu-id="9f599-110">A **Lock-AzureRmStorageContainerImmutabilityPolicy** parancsmag zárolja a ImmutabilityPolicy tároló blob-tárolókat.</span><span class="sxs-lookup"><span data-stu-id="9f599-110">The **Lock-AzureRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="9f599-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9f599-111">EXAMPLES</span></span>

### <span data-ttu-id="9f599-112">1. példa: ImmutabilityPolicy zárolása a tárolási blob-tárolóról a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="9f599-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="9f599-113">Ez a parancs a ImmutabilityPolicy-tároló blob-tárolóját rögzíti a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="9f599-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="9f599-114">2. példa: ImmutabilityPolicy zárolása tároló blob-tároló zárolása a Storage Account objektummal</span><span class="sxs-lookup"><span data-stu-id="9f599-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="9f599-115">Ez a parancs egy ImmutabilityPolicy tároló BLOB-tárolót zárol, a Storage Account objektummal.</span><span class="sxs-lookup"><span data-stu-id="9f599-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="9f599-116">3. példa: ImmutabilityPolicyof zárolása tároló blob-tárolóhoz a tároló objektummal</span><span class="sxs-lookup"><span data-stu-id="9f599-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="9f599-117">Ez a parancs a tárterület-tároló objektummal ImmutabilityPolicy zárolja a tároló BLOB-tárolót.</span><span class="sxs-lookup"><span data-stu-id="9f599-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="9f599-118">Példa 4: ImmutabilityPolicy zárolása ImmutabilityPolicy objektummal</span><span class="sxs-lookup"><span data-stu-id="9f599-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzureRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="9f599-119">Ez a parancs a ImmutabilityPolicy-tároló (ImmutabilityPolicy objektum) segítségével zárolja a BLOB-tárolót.</span><span class="sxs-lookup"><span data-stu-id="9f599-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="9f599-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f599-120">PARAMETERS</span></span>

### <span data-ttu-id="9f599-121">-Container</span><span class="sxs-lookup"><span data-stu-id="9f599-121">-Container</span></span>
<span data-ttu-id="9f599-122">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="9f599-122">Storage container object</span></span>

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

### <span data-ttu-id="9f599-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9f599-123">-ContainerName</span></span>
<span data-ttu-id="9f599-124">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="9f599-124">Container Name</span></span>

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

### <span data-ttu-id="9f599-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f599-125">-DefaultProfile</span></span>
<span data-ttu-id="9f599-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f599-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f599-127">-ETAG</span><span class="sxs-lookup"><span data-stu-id="9f599-127">-Etag</span></span>
<span data-ttu-id="9f599-128">A Immutability házirend ETAG.</span><span class="sxs-lookup"><span data-stu-id="9f599-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="9f599-129">-Force</span><span class="sxs-lookup"><span data-stu-id="9f599-129">-Force</span></span>
<span data-ttu-id="9f599-130">Kényszeríti a ImmutabilityPolicy eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="9f599-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f599-131">-InputObject</span></span>
<span data-ttu-id="9f599-132">ImmutabilityPolicy objektum eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9f599-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="9f599-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f599-133">-ResourceGroupName</span></span>
<span data-ttu-id="9f599-134">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9f599-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="9f599-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9f599-135">-StorageAccount</span></span>
<span data-ttu-id="9f599-136">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="9f599-136">Storage account object</span></span>

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

### <span data-ttu-id="9f599-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9f599-137">-StorageAccountName</span></span>
<span data-ttu-id="9f599-138">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="9f599-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="9f599-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f599-139">-Confirm</span></span>
<span data-ttu-id="9f599-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f599-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f599-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f599-141">-WhatIf</span></span>
<span data-ttu-id="9f599-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f599-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f599-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f599-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f599-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f599-144">CommonParameters</span></span>
<span data-ttu-id="9f599-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f599-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f599-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f599-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f599-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f599-147">INPUTS</span></span>

### <span data-ttu-id="9f599-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9f599-148">System.String</span></span>
<span data-ttu-id="9f599-149">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9f599-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="9f599-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f599-150">OUTPUTS</span></span>

### <span data-ttu-id="9f599-151">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9f599-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="9f599-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f599-152">NOTES</span></span>

## <span data-ttu-id="9f599-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f599-153">RELATED LINKS</span></span>


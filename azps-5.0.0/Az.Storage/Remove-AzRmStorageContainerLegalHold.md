---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195042"
---
# <span data-ttu-id="d7ae7-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="d7ae7-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="d7ae7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ae7-103">A jogi mentességgel rendelkező címkék eltávolítása a tárterület-tárolóból</span><span class="sxs-lookup"><span data-stu-id="d7ae7-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="d7ae7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7ae7-104">SYNTAX</span></span>

### <span data-ttu-id="d7ae7-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7ae7-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7ae7-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d7ae7-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7ae7-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d7ae7-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7ae7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7ae7-108">DESCRIPTION</span></span>
<span data-ttu-id="d7ae7-109">A **Remove-AzRmStorageContainerLegalHold** parancsmag a jogcímeket tároló blob-tárolóból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="d7ae7-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="d7ae7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d7ae7-110">EXAMPLES</span></span>

### <span data-ttu-id="d7ae7-111">1. példa: a mentességi kódok eltávolítása a tároló blob-tárolóból a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="d7ae7-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="d7ae7-112">Ez a parancs eltávolítja a jogi mentességet tároló blob-tárolóból a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="d7ae7-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d7ae7-113">2. példa: a mentességi kódok eltávolítása a tároló blob-tárolóból a tárterület-objektummal és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="d7ae7-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="d7ae7-114">Ez a parancs eltávolítja a jogi mentességet tároló blob-tárolóból a Storage Account objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="d7ae7-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="d7ae7-115">3. példa: a minden tároló blob-tárolóban lévő jogi mentességi címke eltávolítása egy csővezetéket tartalmazó tárterületről</span><span class="sxs-lookup"><span data-stu-id="d7ae7-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="d7ae7-116">Ez a parancs eltávolítja a minden tároló blob-tárolóban lévő jogi mentességi címkét egy csővezetéket tartalmazó tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="d7ae7-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="d7ae7-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7ae7-117">PARAMETERS</span></span>

### <span data-ttu-id="d7ae7-118">-Container</span><span class="sxs-lookup"><span data-stu-id="d7ae7-118">-Container</span></span>
<span data-ttu-id="d7ae7-119">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="d7ae7-119">Storage container object</span></span>

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

### <span data-ttu-id="d7ae7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ae7-120">-DefaultProfile</span></span>
<span data-ttu-id="d7ae7-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7ae7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7ae7-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7ae7-122">-Name</span></span>
<span data-ttu-id="d7ae7-123">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="d7ae7-123">Container Name</span></span>

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

### <span data-ttu-id="d7ae7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ae7-124">-ResourceGroupName</span></span>
<span data-ttu-id="d7ae7-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d7ae7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d7ae7-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7ae7-126">-StorageAccount</span></span>
<span data-ttu-id="d7ae7-127">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="d7ae7-127">Storage account object</span></span>

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

### <span data-ttu-id="d7ae7-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d7ae7-128">-StorageAccountName</span></span>
<span data-ttu-id="d7ae7-129">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d7ae7-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="d7ae7-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="d7ae7-130">-Tag</span></span>
<span data-ttu-id="d7ae7-131">Tároló LegalHold Címkék</span><span class="sxs-lookup"><span data-stu-id="d7ae7-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="d7ae7-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7ae7-132">-Confirm</span></span>
<span data-ttu-id="d7ae7-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7ae7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7ae7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7ae7-134">-WhatIf</span></span>
<span data-ttu-id="d7ae7-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7ae7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7ae7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7ae7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7ae7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ae7-137">CommonParameters</span></span>
<span data-ttu-id="d7ae7-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7ae7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ae7-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ae7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ae7-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7ae7-140">INPUTS</span></span>

### <span data-ttu-id="d7ae7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d7ae7-141">System.String</span></span>

### <span data-ttu-id="d7ae7-142">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7ae7-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d7ae7-143">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="d7ae7-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d7ae7-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7ae7-144">OUTPUTS</span></span>

### <span data-ttu-id="d7ae7-145">Microsoft. Azure. Command. Management. Storage. models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="d7ae7-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="d7ae7-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7ae7-146">NOTES</span></span>

## <span data-ttu-id="d7ae7-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7ae7-147">RELATED LINKS</span></span>

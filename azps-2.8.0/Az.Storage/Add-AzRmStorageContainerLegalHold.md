---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 13fc089db38bb9aa525285c61b1a2d4fecd934b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839589"
---
# <span data-ttu-id="ba110-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ba110-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="ba110-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba110-102">SYNOPSIS</span></span>
<span data-ttu-id="ba110-103">Jogi visszatartási címke hozzáadása a tároló blob-tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="ba110-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="ba110-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba110-104">SYNTAX</span></span>

### <span data-ttu-id="ba110-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba110-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba110-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ba110-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba110-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="ba110-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba110-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba110-108">DESCRIPTION</span></span>
<span data-ttu-id="ba110-109">A **Add-AzRmStorageContainerLegalHold** parancsmag jogi visszatartási címkéket ad a tároló blob-tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="ba110-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="ba110-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ba110-110">EXAMPLES</span></span>

### <span data-ttu-id="ba110-111">1. példa: jogi célú mentességi Címkék hozzáadása a tároló blob-tárolóhoz a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="ba110-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="ba110-112">Ez a parancs a jogi mentességet tartalmazó címkét felveszi egy tároló blob-tárolóba a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="ba110-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="ba110-113">2. példa: az adatmegőrzési Címkék felvétele a tároló blob-tárolóba a tárolási fiók objektummal és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="ba110-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="ba110-114">Ez a parancs a jogi mentességet tartalmazó címkét felveszi egy tároló blob-tárolóba a Storage Account objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="ba110-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="ba110-115">3. példa: adatmegőrzési címkék elhelyezése a tárterületen lévő tárterület-tárolóban a csővezetéken</span><span class="sxs-lookup"><span data-stu-id="ba110-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="ba110-116">Ez a parancs a minden tároló blob-tárolóhoz hozzáadja a jogi mentességi címkéket a csővezetéket tároló tárterületen.</span><span class="sxs-lookup"><span data-stu-id="ba110-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="ba110-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba110-117">PARAMETERS</span></span>

### <span data-ttu-id="ba110-118">-Container</span><span class="sxs-lookup"><span data-stu-id="ba110-118">-Container</span></span>
<span data-ttu-id="ba110-119">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="ba110-119">Storage container object</span></span>

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

### <span data-ttu-id="ba110-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba110-120">-DefaultProfile</span></span>
<span data-ttu-id="ba110-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba110-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba110-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba110-122">-Name</span></span>
<span data-ttu-id="ba110-123">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="ba110-123">Container Name</span></span>

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

### <span data-ttu-id="ba110-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba110-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba110-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ba110-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ba110-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba110-126">-StorageAccount</span></span>
<span data-ttu-id="ba110-127">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="ba110-127">Storage account object</span></span>

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

### <span data-ttu-id="ba110-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ba110-128">-StorageAccountName</span></span>
<span data-ttu-id="ba110-129">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ba110-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="ba110-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="ba110-130">-Tag</span></span>
<span data-ttu-id="ba110-131">Tároló LegalHold Címkék</span><span class="sxs-lookup"><span data-stu-id="ba110-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="ba110-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba110-132">-Confirm</span></span>
<span data-ttu-id="ba110-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba110-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba110-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba110-134">-WhatIf</span></span>
<span data-ttu-id="ba110-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba110-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba110-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba110-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba110-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba110-137">CommonParameters</span></span>
<span data-ttu-id="ba110-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba110-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba110-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba110-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba110-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba110-140">INPUTS</span></span>

### <span data-ttu-id="ba110-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ba110-141">System.String</span></span>

### <span data-ttu-id="ba110-142">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba110-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ba110-143">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="ba110-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="ba110-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba110-144">OUTPUTS</span></span>

### <span data-ttu-id="ba110-145">Microsoft. Azure. Command. Management. Storage. models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="ba110-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="ba110-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba110-146">NOTES</span></span>

## <span data-ttu-id="ba110-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba110-147">RELATED LINKS</span></span>

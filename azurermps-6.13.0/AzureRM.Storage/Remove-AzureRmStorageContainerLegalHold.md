---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: da0793e7eb10f7b83d785aea34866842abe9b887
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498156"
---
# <span data-ttu-id="486d0-101">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="486d0-101">Remove-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="486d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="486d0-102">SYNOPSIS</span></span>
<span data-ttu-id="486d0-103">A jogi mentességgel rendelkező címkék eltávolítása a tárterület-tárolóból</span><span class="sxs-lookup"><span data-stu-id="486d0-103">Removes legal hold tags from a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="486d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="486d0-104">SYNTAX</span></span>

### <span data-ttu-id="486d0-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="486d0-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="486d0-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="486d0-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="486d0-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="486d0-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="486d0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="486d0-108">DESCRIPTION</span></span>
<span data-ttu-id="486d0-109">A **Remove-AzureRmStorageContainerLegalHold** parancsmag a jogcímeket tároló blob-tárolóból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="486d0-109">The **Remove-AzureRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="486d0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="486d0-110">EXAMPLES</span></span>

### <span data-ttu-id="486d0-111">1. példa: a mentességi kódok eltávolítása a tároló blob-tárolóból a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="486d0-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="486d0-112">Ez a parancs eltávolítja a jogi mentességet tároló blob-tárolóból a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="486d0-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="486d0-113">2. példa: a mentességi kódok eltávolítása a tároló blob-tárolóból a tárterület-objektummal és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="486d0-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2 
```

<span data-ttu-id="486d0-114">Ez a parancs eltávolítja a jogi mentességet tároló blob-tárolóból a Storage Account objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="486d0-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="486d0-115">3. példa: a minden tároló blob-tárolóban lévő jogi mentességi címke eltávolítása egy csővezetéket tartalmazó tárterületről</span><span class="sxs-lookup"><span data-stu-id="486d0-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="486d0-116">Ez a parancs eltávolítja a minden tároló blob-tárolóban lévő jogi mentességi címkét egy csővezetéket tartalmazó tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="486d0-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>


## <span data-ttu-id="486d0-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="486d0-117">PARAMETERS</span></span>

### <span data-ttu-id="486d0-118">-Container</span><span class="sxs-lookup"><span data-stu-id="486d0-118">-Container</span></span>
<span data-ttu-id="486d0-119">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="486d0-119">Storage container object</span></span>

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

### <span data-ttu-id="486d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486d0-120">-DefaultProfile</span></span>
<span data-ttu-id="486d0-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="486d0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="486d0-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="486d0-122">-Name</span></span>
<span data-ttu-id="486d0-123">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="486d0-123">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="486d0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="486d0-124">-ResourceGroupName</span></span>
<span data-ttu-id="486d0-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="486d0-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="486d0-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="486d0-126">-StorageAccount</span></span>
<span data-ttu-id="486d0-127">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="486d0-127">Storage account object</span></span>

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

### <span data-ttu-id="486d0-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="486d0-128">-StorageAccountName</span></span>
<span data-ttu-id="486d0-129">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="486d0-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="486d0-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="486d0-130">-Tag</span></span>
<span data-ttu-id="486d0-131">Tároló LegalHold Címkék</span><span class="sxs-lookup"><span data-stu-id="486d0-131">Container LegalHold Tags</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486d0-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="486d0-132">-Confirm</span></span>
<span data-ttu-id="486d0-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="486d0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="486d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="486d0-134">-WhatIf</span></span>
<span data-ttu-id="486d0-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="486d0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="486d0-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="486d0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="486d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486d0-137">CommonParameters</span></span>
<span data-ttu-id="486d0-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="486d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486d0-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="486d0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486d0-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="486d0-140">INPUTS</span></span>

### <span data-ttu-id="486d0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="486d0-141">System.String</span></span>

## <span data-ttu-id="486d0-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="486d0-142">OUTPUTS</span></span>

### <span data-ttu-id="486d0-143">Microsoft. Azure. Command. Management. Storage. models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="486d0-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="486d0-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="486d0-144">NOTES</span></span>

## <span data-ttu-id="486d0-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="486d0-145">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: 465a40e384e5ea7240e0ced2a010c88529feb2f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492700"
---
# <span data-ttu-id="f0697-101">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="f0697-101">Add-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="f0697-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0697-102">SYNOPSIS</span></span>
<span data-ttu-id="f0697-103">Jogi visszatartási címke hozzáadása a tároló blob-tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="f0697-103">Adds legal hold tags to a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0697-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0697-104">SYNTAX</span></span>

### <span data-ttu-id="f0697-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0697-105">AccountName (Default)</span></span>
```
Add-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0697-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f0697-106">AccountObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0697-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="f0697-107">ContainerObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0697-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0697-108">DESCRIPTION</span></span>
<span data-ttu-id="f0697-109">A **Add-AzureRmStorageContainerLegalHold** parancsmag jogi visszatartási címkéket ad a tároló blob-tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="f0697-109">The **Add-AzureRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="f0697-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f0697-110">EXAMPLES</span></span>

### <span data-ttu-id="f0697-111">1. példa: jogi célú mentességi Címkék hozzáadása a tároló blob-tárolóhoz a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="f0697-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2 
```

<span data-ttu-id="f0697-112">Ez a parancs a jogi mentességet tartalmazó címkét felveszi egy tároló blob-tárolóba a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="f0697-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="f0697-113">2. példa: az adatmegőrzési Címkék felvétele a tároló blob-tárolóba a tárolási fiók objektummal és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="f0697-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="f0697-114">Ez a parancs a jogi mentességet tartalmazó címkét felveszi egy tároló blob-tárolóba a Storage Account objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="f0697-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="f0697-115">3. példa: adatmegőrzési címkék elhelyezése a tárterületen lévő tárterület-tárolóban a csővezetéken</span><span class="sxs-lookup"><span data-stu-id="f0697-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzureRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="f0697-116">Ez a parancs a minden tároló blob-tárolóhoz hozzáadja a jogi mentességi címkéket a csővezetéket tároló tárterületen.</span><span class="sxs-lookup"><span data-stu-id="f0697-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="f0697-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0697-117">PARAMETERS</span></span>

### <span data-ttu-id="f0697-118">-Container</span><span class="sxs-lookup"><span data-stu-id="f0697-118">-Container</span></span>
<span data-ttu-id="f0697-119">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="f0697-119">Storage container object</span></span>

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

### <span data-ttu-id="f0697-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0697-120">-DefaultProfile</span></span>
<span data-ttu-id="f0697-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0697-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0697-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f0697-122">-Name</span></span>
<span data-ttu-id="f0697-123">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="f0697-123">Container Name</span></span>

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

### <span data-ttu-id="f0697-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0697-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0697-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f0697-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f0697-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f0697-126">-StorageAccount</span></span>
<span data-ttu-id="f0697-127">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="f0697-127">Storage account object</span></span>

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

### <span data-ttu-id="f0697-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f0697-128">-StorageAccountName</span></span>
<span data-ttu-id="f0697-129">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f0697-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="f0697-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="f0697-130">-Tag</span></span>
<span data-ttu-id="f0697-131">Tároló LegalHold Címkék</span><span class="sxs-lookup"><span data-stu-id="f0697-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="f0697-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f0697-132">-Confirm</span></span>
<span data-ttu-id="f0697-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f0697-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0697-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0697-134">-WhatIf</span></span>
<span data-ttu-id="f0697-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f0697-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0697-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0697-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0697-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0697-137">CommonParameters</span></span>
<span data-ttu-id="f0697-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0697-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0697-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0697-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0697-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0697-140">INPUTS</span></span>

### <span data-ttu-id="f0697-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f0697-141">System.String</span></span>

## <span data-ttu-id="f0697-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0697-142">OUTPUTS</span></span>

### <span data-ttu-id="f0697-143">Microsoft. Azure. Command. Management. Storage. models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="f0697-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="f0697-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0697-144">NOTES</span></span>

## <span data-ttu-id="f0697-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0697-145">RELATED LINKS</span></span>


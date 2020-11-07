---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
ms.openlocfilehash: 089451a0a0aae399a18296fbf4982724b35d432e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680297"
---
# <span data-ttu-id="2f53b-101">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2f53b-101">Remove-AzureRmStorageContainer</span></span>

## <span data-ttu-id="2f53b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f53b-102">SYNOPSIS</span></span>
<span data-ttu-id="2f53b-103">Tároló blob-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2f53b-103">Removes a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f53b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f53b-104">SYNTAX</span></span>

### <span data-ttu-id="2f53b-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f53b-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f53b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2f53b-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f53b-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="2f53b-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f53b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f53b-108">DESCRIPTION</span></span>
<span data-ttu-id="2f53b-109">A **Remove-AzureRmStorageContainer** parancsmag eltávolítja a BLOB-tárolót</span><span class="sxs-lookup"><span data-stu-id="2f53b-109">The **Remove-AzureRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="2f53b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2f53b-110">EXAMPLES</span></span>

### <span data-ttu-id="2f53b-111">1. példa: a tárolási blob-tároló eltávolítása a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="2f53b-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="2f53b-112">Ez a parancs a tároló BLOB-tárolót eltávolítja a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="2f53b-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="2f53b-113">2. példa: a tárolási blob-tároló eltávolítása a Storage Account objektummal és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="2f53b-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="2f53b-114">Ez a parancs eltávolítja a tároló BLOB-tárolót a Storage Account objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="2f53b-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="2f53b-115">3. példa: az összes tárterületet tároló blob-tároló eltávolítása egy csővezetéktel</span><span class="sxs-lookup"><span data-stu-id="2f53b-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainer -Force
```

<span data-ttu-id="2f53b-116">Ez a parancs eltávolítja az összes tárterület-tárolót a tároló fiókból a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="2f53b-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="2f53b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f53b-117">PARAMETERS</span></span>

### <span data-ttu-id="2f53b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f53b-118">-DefaultProfile</span></span>
<span data-ttu-id="2f53b-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f53b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f53b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2f53b-120">-Force</span></span>
<span data-ttu-id="2f53b-121">A tároló és az összes tartalom eltávolításának kényszerítése</span><span class="sxs-lookup"><span data-stu-id="2f53b-121">Force to remove the container and all content in it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f53b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f53b-122">-InputObject</span></span>
<span data-ttu-id="2f53b-123">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="2f53b-123">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f53b-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f53b-124">-Name</span></span>
<span data-ttu-id="2f53b-125">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="2f53b-125">Container Name</span></span>

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

### <span data-ttu-id="2f53b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f53b-126">-PassThru</span></span>
<span data-ttu-id="2f53b-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2f53b-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2f53b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f53b-128">-ResourceGroupName</span></span>
<span data-ttu-id="2f53b-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="2f53b-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="2f53b-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2f53b-130">-StorageAccount</span></span>
<span data-ttu-id="2f53b-131">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="2f53b-131">Storage account object</span></span>

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

### <span data-ttu-id="2f53b-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2f53b-132">-StorageAccountName</span></span>
<span data-ttu-id="2f53b-133">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="2f53b-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="2f53b-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f53b-134">-Confirm</span></span>
<span data-ttu-id="2f53b-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f53b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f53b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f53b-136">-WhatIf</span></span>
<span data-ttu-id="2f53b-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f53b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f53b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f53b-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f53b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f53b-139">CommonParameters</span></span>
<span data-ttu-id="2f53b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f53b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f53b-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f53b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f53b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f53b-142">INPUTS</span></span>

### <span data-ttu-id="2f53b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2f53b-143">System.String</span></span>

## <span data-ttu-id="2f53b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f53b-144">OUTPUTS</span></span>

### <span data-ttu-id="2f53b-145">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="2f53b-145">System.Object</span></span>

## <span data-ttu-id="2f53b-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f53b-146">NOTES</span></span>

## <span data-ttu-id="2f53b-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f53b-147">RELATED LINKS</span></span>

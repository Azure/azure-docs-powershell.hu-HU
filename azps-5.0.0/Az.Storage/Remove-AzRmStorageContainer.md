---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195045"
---
# <span data-ttu-id="ad515-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad515-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="ad515-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad515-102">SYNOPSIS</span></span>
<span data-ttu-id="ad515-103">Tároló blob-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ad515-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="ad515-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad515-104">SYNTAX</span></span>

### <span data-ttu-id="ad515-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad515-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad515-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ad515-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad515-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="ad515-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad515-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad515-108">DESCRIPTION</span></span>
<span data-ttu-id="ad515-109">A **Remove-AzRmStorageContainer** parancsmag eltávolítja a BLOB-tárolót</span><span class="sxs-lookup"><span data-stu-id="ad515-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="ad515-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ad515-110">EXAMPLES</span></span>

### <span data-ttu-id="ad515-111">1. példa: a tárolási blob-tároló eltávolítása a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="ad515-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="ad515-112">Ez a parancs a tároló BLOB-tárolót eltávolítja a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="ad515-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="ad515-113">2. példa: a tárolási blob-tároló eltávolítása a Storage Account objektummal és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="ad515-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="ad515-114">Ez a parancs eltávolítja a tároló BLOB-tárolót a Storage Account objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="ad515-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="ad515-115">3. példa: az összes tárterületet tároló blob-tároló eltávolítása egy csővezetéktel</span><span class="sxs-lookup"><span data-stu-id="ad515-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="ad515-116">Ez a parancs eltávolítja az összes tárterület-tárolót a tároló fiókból a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="ad515-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="ad515-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad515-117">PARAMETERS</span></span>

### <span data-ttu-id="ad515-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad515-118">-DefaultProfile</span></span>
<span data-ttu-id="ad515-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad515-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad515-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ad515-120">-Force</span></span>
<span data-ttu-id="ad515-121">A tároló és az összes tartalom eltávolításának kényszerítése</span><span class="sxs-lookup"><span data-stu-id="ad515-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad515-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad515-122">-InputObject</span></span>
<span data-ttu-id="ad515-123">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="ad515-123">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad515-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad515-124">-Name</span></span>
<span data-ttu-id="ad515-125">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="ad515-125">Container Name</span></span>

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

### <span data-ttu-id="ad515-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad515-126">-PassThru</span></span>
<span data-ttu-id="ad515-127">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="ad515-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ad515-128">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="ad515-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ad515-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad515-129">-ResourceGroupName</span></span>
<span data-ttu-id="ad515-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ad515-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ad515-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad515-131">-StorageAccount</span></span>
<span data-ttu-id="ad515-132">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="ad515-132">Storage account object</span></span>

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

### <span data-ttu-id="ad515-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ad515-133">-StorageAccountName</span></span>
<span data-ttu-id="ad515-134">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ad515-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="ad515-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad515-135">-Confirm</span></span>
<span data-ttu-id="ad515-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad515-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad515-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad515-137">-WhatIf</span></span>
<span data-ttu-id="ad515-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad515-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad515-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad515-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad515-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad515-140">CommonParameters</span></span>
<span data-ttu-id="ad515-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad515-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad515-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad515-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad515-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad515-143">INPUTS</span></span>

### <span data-ttu-id="ad515-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ad515-144">System.String</span></span>

### <span data-ttu-id="ad515-145">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad515-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ad515-146">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="ad515-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="ad515-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad515-147">OUTPUTS</span></span>

### <span data-ttu-id="ad515-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad515-148">System.Boolean</span></span>

## <span data-ttu-id="ad515-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad515-149">NOTES</span></span>

## <span data-ttu-id="ad515-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad515-150">RELATED LINKS</span></span>
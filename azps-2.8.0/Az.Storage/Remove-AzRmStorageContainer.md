---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: d7a4563a32da28215dbb9b6dab2b911a500183a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839789"
---
# <span data-ttu-id="83a02-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="83a02-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="83a02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83a02-102">SYNOPSIS</span></span>
<span data-ttu-id="83a02-103">Tároló blob-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="83a02-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="83a02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83a02-104">SYNTAX</span></span>

### <span data-ttu-id="83a02-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83a02-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83a02-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="83a02-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83a02-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="83a02-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83a02-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="83a02-108">DESCRIPTION</span></span>
<span data-ttu-id="83a02-109">A **Remove-AzRmStorageContainer** parancsmag eltávolítja a BLOB-tárolót</span><span class="sxs-lookup"><span data-stu-id="83a02-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="83a02-110">Példák</span><span class="sxs-lookup"><span data-stu-id="83a02-110">EXAMPLES</span></span>

### <span data-ttu-id="83a02-111">1. példa: a tárolási blob-tároló eltávolítása a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="83a02-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="83a02-112">Ez a parancs a tároló BLOB-tárolót eltávolítja a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="83a02-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="83a02-113">2. példa: a tárolási blob-tároló eltávolítása a Storage Account objektummal és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="83a02-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="83a02-114">Ez a parancs eltávolítja a tároló BLOB-tárolót a Storage Account objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="83a02-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="83a02-115">3. példa: az összes tárterületet tároló blob-tároló eltávolítása egy csővezetéktel</span><span class="sxs-lookup"><span data-stu-id="83a02-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="83a02-116">Ez a parancs eltávolítja az összes tárterület-tárolót a tároló fiókból a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="83a02-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="83a02-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83a02-117">PARAMETERS</span></span>

### <span data-ttu-id="83a02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a02-118">-DefaultProfile</span></span>
<span data-ttu-id="83a02-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83a02-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83a02-120">-Force</span><span class="sxs-lookup"><span data-stu-id="83a02-120">-Force</span></span>
<span data-ttu-id="83a02-121">A tároló és az összes tartalom eltávolításának kényszerítése</span><span class="sxs-lookup"><span data-stu-id="83a02-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="83a02-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83a02-122">-InputObject</span></span>
<span data-ttu-id="83a02-123">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="83a02-123">Storage container object</span></span>

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

### <span data-ttu-id="83a02-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83a02-124">-Name</span></span>
<span data-ttu-id="83a02-125">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="83a02-125">Container Name</span></span>

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

### <span data-ttu-id="83a02-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83a02-126">-PassThru</span></span>
<span data-ttu-id="83a02-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="83a02-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="83a02-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83a02-128">-ResourceGroupName</span></span>
<span data-ttu-id="83a02-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="83a02-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="83a02-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="83a02-130">-StorageAccount</span></span>
<span data-ttu-id="83a02-131">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="83a02-131">Storage account object</span></span>

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

### <span data-ttu-id="83a02-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="83a02-132">-StorageAccountName</span></span>
<span data-ttu-id="83a02-133">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="83a02-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="83a02-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83a02-134">-Confirm</span></span>
<span data-ttu-id="83a02-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83a02-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83a02-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83a02-136">-WhatIf</span></span>
<span data-ttu-id="83a02-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83a02-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83a02-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83a02-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83a02-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a02-139">CommonParameters</span></span>
<span data-ttu-id="83a02-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83a02-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a02-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83a02-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a02-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83a02-142">INPUTS</span></span>

### <span data-ttu-id="83a02-143">System. String</span><span class="sxs-lookup"><span data-stu-id="83a02-143">System.String</span></span>

### <span data-ttu-id="83a02-144">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83a02-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="83a02-145">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="83a02-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="83a02-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83a02-146">OUTPUTS</span></span>

### <span data-ttu-id="83a02-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83a02-147">System.Boolean</span></span>

## <span data-ttu-id="83a02-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83a02-148">NOTES</span></span>

## <span data-ttu-id="83a02-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83a02-149">RELATED LINKS</span></span>

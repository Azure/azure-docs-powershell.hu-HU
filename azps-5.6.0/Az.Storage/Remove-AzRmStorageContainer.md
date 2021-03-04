---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 467fab7d2d7c344c3ffa2ca631addb538e790101
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937282"
---
# <span data-ttu-id="a6749-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a6749-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="a6749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6749-102">SYNOPSIS</span></span>
<span data-ttu-id="a6749-103">Tároló blobtároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a6749-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="a6749-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a6749-104">SYNTAX</span></span>

### <span data-ttu-id="a6749-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6749-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6749-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a6749-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6749-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a6749-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6749-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a6749-108">DESCRIPTION</span></span>
<span data-ttu-id="a6749-109">A **Remove-AzRmStorageContainer** parancsmag eltávolít egy tároló blobtárolót</span><span class="sxs-lookup"><span data-stu-id="a6749-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="a6749-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a6749-110">EXAMPLES</span></span>

### <span data-ttu-id="a6749-111">1. példa: Tárterület blobtároló eltávolítása tárfióknévvel és tárolónévvel</span><span class="sxs-lookup"><span data-stu-id="a6749-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="a6749-112">Ez a parancs eltávolítja a Tárfiók nevét és tárolónevét tartalmazó tár blobtárolót.</span><span class="sxs-lookup"><span data-stu-id="a6749-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a6749-113">2. példa: Tárterület blobtároló eltávolítása Tárfiók-objektummal és tárolónévvel</span><span class="sxs-lookup"><span data-stu-id="a6749-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="a6749-114">Ez a parancs eltávolít egy Tárfiók-objektumot és -tároló nevét tartalmazó tár blobtárolót.</span><span class="sxs-lookup"><span data-stu-id="a6749-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="a6749-115">3. példa: Az összes tár blobtároló eltávolítása egy tárfiókból folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="a6749-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="a6749-116">Ez a parancs eltávolítja az összes tárterület blobtárolóját egy folyamatban lévő tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="a6749-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="a6749-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6749-117">PARAMETERS</span></span>

### <span data-ttu-id="a6749-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6749-118">-DefaultProfile</span></span>
<span data-ttu-id="a6749-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6749-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6749-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a6749-120">-Force</span></span>
<span data-ttu-id="a6749-121">A tároló és az abban található összes tartalom eltávolításának kényszerítve</span><span class="sxs-lookup"><span data-stu-id="a6749-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="a6749-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6749-122">-InputObject</span></span>
<span data-ttu-id="a6749-123">Tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="a6749-123">Storage container object</span></span>

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

### <span data-ttu-id="a6749-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a6749-124">-Name</span></span>
<span data-ttu-id="a6749-125">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="a6749-125">Container Name</span></span>

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

### <span data-ttu-id="a6749-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6749-126">-PassThru</span></span>
<span data-ttu-id="a6749-127">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="a6749-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a6749-128">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="a6749-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a6749-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6749-129">-ResourceGroupName</span></span>
<span data-ttu-id="a6749-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a6749-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="a6749-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6749-131">-StorageAccount</span></span>
<span data-ttu-id="a6749-132">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="a6749-132">Storage account object</span></span>

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

### <span data-ttu-id="a6749-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a6749-133">-StorageAccountName</span></span>
<span data-ttu-id="a6749-134">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="a6749-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="a6749-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6749-135">-Confirm</span></span>
<span data-ttu-id="a6749-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a6749-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6749-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6749-137">-WhatIf</span></span>
<span data-ttu-id="a6749-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a6749-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6749-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6749-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6749-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6749-140">CommonParameters</span></span>
<span data-ttu-id="a6749-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6749-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6749-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6749-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6749-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6749-143">INPUTS</span></span>

### <span data-ttu-id="a6749-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a6749-144">System.String</span></span>

### <span data-ttu-id="a6749-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6749-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a6749-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="a6749-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="a6749-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6749-147">OUTPUTS</span></span>

### <span data-ttu-id="a6749-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6749-148">System.Boolean</span></span>

## <span data-ttu-id="a6749-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a6749-149">NOTES</span></span>

## <span data-ttu-id="a6749-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6749-150">RELATED LINKS</span></span>

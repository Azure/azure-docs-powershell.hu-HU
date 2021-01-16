---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479398"
---
# <span data-ttu-id="75986-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="75986-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="75986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75986-102">SYNOPSIS</span></span>
<span data-ttu-id="75986-103">Tároló blobtároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="75986-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="75986-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75986-104">SYNTAX</span></span>

### <span data-ttu-id="75986-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75986-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75986-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="75986-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75986-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="75986-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75986-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75986-108">DESCRIPTION</span></span>
<span data-ttu-id="75986-109">A **Remove-AzRmStorageContainer** parancsmag eltávolít egy tároló blobtárolót</span><span class="sxs-lookup"><span data-stu-id="75986-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="75986-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75986-110">EXAMPLES</span></span>

### <span data-ttu-id="75986-111">1. példa: Tárterület blobtároló eltávolítása tárfióknévvel és tárolónévvel</span><span class="sxs-lookup"><span data-stu-id="75986-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="75986-112">Ez a parancs eltávolítja a Tárfiók nevét és tárolónevét tartalmazó tár blobtárolót.</span><span class="sxs-lookup"><span data-stu-id="75986-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="75986-113">2. példa: Tárterület blobtároló eltávolítása Tárfiók-objektummal és tárolónévvel</span><span class="sxs-lookup"><span data-stu-id="75986-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="75986-114">Ez a parancs eltávolít egy Tárfiók-objektumot és -tároló nevét tartalmazó tár blobtárolót.</span><span class="sxs-lookup"><span data-stu-id="75986-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="75986-115">3. példa: Az összes tár blobtároló eltávolítása egy tárfiókból folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="75986-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="75986-116">Ez a parancs eltávolítja az összes tárterület blobtárolóját egy folyamatban lévő tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="75986-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="75986-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75986-117">PARAMETERS</span></span>

### <span data-ttu-id="75986-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75986-118">-DefaultProfile</span></span>
<span data-ttu-id="75986-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75986-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75986-120">-Force</span><span class="sxs-lookup"><span data-stu-id="75986-120">-Force</span></span>
<span data-ttu-id="75986-121">A tároló és a benne található összes tartalom eltávolítása kényszerítve</span><span class="sxs-lookup"><span data-stu-id="75986-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="75986-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75986-122">-InputObject</span></span>
<span data-ttu-id="75986-123">Tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="75986-123">Storage container object</span></span>

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

### <span data-ttu-id="75986-124">-Name</span><span class="sxs-lookup"><span data-stu-id="75986-124">-Name</span></span>
<span data-ttu-id="75986-125">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="75986-125">Container Name</span></span>

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

### <span data-ttu-id="75986-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75986-126">-PassThru</span></span>
<span data-ttu-id="75986-127">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="75986-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="75986-128">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="75986-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="75986-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75986-129">-ResourceGroupName</span></span>
<span data-ttu-id="75986-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="75986-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="75986-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="75986-131">-StorageAccount</span></span>
<span data-ttu-id="75986-132">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="75986-132">Storage account object</span></span>

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

### <span data-ttu-id="75986-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="75986-133">-StorageAccountName</span></span>
<span data-ttu-id="75986-134">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="75986-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="75986-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75986-135">-Confirm</span></span>
<span data-ttu-id="75986-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="75986-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75986-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75986-137">-WhatIf</span></span>
<span data-ttu-id="75986-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="75986-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75986-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75986-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75986-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75986-140">CommonParameters</span></span>
<span data-ttu-id="75986-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75986-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75986-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75986-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75986-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75986-143">INPUTS</span></span>

### <span data-ttu-id="75986-144">System.String</span><span class="sxs-lookup"><span data-stu-id="75986-144">System.String</span></span>

### <span data-ttu-id="75986-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75986-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="75986-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="75986-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="75986-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75986-147">OUTPUTS</span></span>

### <span data-ttu-id="75986-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="75986-148">System.Boolean</span></span>

## <span data-ttu-id="75986-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75986-149">NOTES</span></span>

## <span data-ttu-id="75986-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75986-150">RELATED LINKS</span></span>

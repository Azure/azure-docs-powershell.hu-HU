---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163011"
---
# <span data-ttu-id="a145a-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a145a-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="a145a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a145a-102">SYNOPSIS</span></span>
<span data-ttu-id="a145a-103">A Tárterület blobtárolói immutabilityPolicy zárolása</span><span class="sxs-lookup"><span data-stu-id="a145a-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="a145a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a145a-104">SYNTAX</span></span>

### <span data-ttu-id="a145a-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a145a-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a145a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a145a-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a145a-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a145a-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a145a-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="a145a-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a145a-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a145a-109">DESCRIPTION</span></span>
<span data-ttu-id="a145a-110">A **Lock-AzRmStorageContainerImmutabilityPolicy parancsmag** zárolja a Tároló blobtárolók ImmutabilityPolicy parancsmagját.</span><span class="sxs-lookup"><span data-stu-id="a145a-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="a145a-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a145a-111">EXAMPLES</span></span>

### <span data-ttu-id="a145a-112">1. példa: Tárfiók nevét és tárolónevét tartalmazó Tár blobtároló ImmutabilityPolicy zárolása</span><span class="sxs-lookup"><span data-stu-id="a145a-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="a145a-113">Ez a parancs a Tárfiók nevét és tárolónevét tartalmazó Tár blobtároló ImmutabilityPolicy parancsát zárolja.</span><span class="sxs-lookup"><span data-stu-id="a145a-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a145a-114">2. példa: Tárterület-blobtároló ImmutabilityPolicy zárolása Tárfiók-objektummal</span><span class="sxs-lookup"><span data-stu-id="a145a-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="a145a-115">Ez a parancs zárolja a Tárfiók-objektummal együtt egy Tároló blobtároló ImmutabilityPolicy parancsát.</span><span class="sxs-lookup"><span data-stu-id="a145a-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="a145a-116">3. példa: A Tároló blobtároló ImmutabilityPolicyof zárolása tárolóobjektummal</span><span class="sxs-lookup"><span data-stu-id="a145a-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="a145a-117">Ez a parancs zárolja egy Tárolótároló objektummal egy Tároló blobtároló immutabilityPolicy parancsát.</span><span class="sxs-lookup"><span data-stu-id="a145a-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="a145a-118">4. példa: Tárterület blobtároló ImmutabilityPolicy zárolása ImmutabilityPolicy objektummal</span><span class="sxs-lookup"><span data-stu-id="a145a-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="a145a-119">Ez a parancs zárolja a Tár blobtároló ImmutabilityPolicy parancsát A ImmutabilityPolicy objektummal.</span><span class="sxs-lookup"><span data-stu-id="a145a-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="a145a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a145a-120">PARAMETERS</span></span>

### <span data-ttu-id="a145a-121">-Container</span><span class="sxs-lookup"><span data-stu-id="a145a-121">-Container</span></span>
<span data-ttu-id="a145a-122">Tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="a145a-122">Storage container object</span></span>

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

### <span data-ttu-id="a145a-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a145a-123">-ContainerName</span></span>
<span data-ttu-id="a145a-124">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="a145a-124">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a145a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a145a-125">-DefaultProfile</span></span>
<span data-ttu-id="a145a-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a145a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a145a-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="a145a-127">-Etag</span></span>
<span data-ttu-id="a145a-128">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="a145a-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a145a-129">-Force</span><span class="sxs-lookup"><span data-stu-id="a145a-129">-Force</span></span>
<span data-ttu-id="a145a-130">Kényszerítés a ImmutabilityPolicy eltávolítására.</span><span class="sxs-lookup"><span data-stu-id="a145a-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="a145a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a145a-131">-InputObject</span></span>
<span data-ttu-id="a145a-132">ImmutabilityPolicy Object to Remove</span><span class="sxs-lookup"><span data-stu-id="a145a-132">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a145a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a145a-133">-ResourceGroupName</span></span>
<span data-ttu-id="a145a-134">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a145a-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="a145a-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a145a-135">-StorageAccount</span></span>
<span data-ttu-id="a145a-136">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="a145a-136">Storage account object</span></span>

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

### <span data-ttu-id="a145a-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a145a-137">-StorageAccountName</span></span>
<span data-ttu-id="a145a-138">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="a145a-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="a145a-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a145a-139">-Confirm</span></span>
<span data-ttu-id="a145a-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a145a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a145a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a145a-141">-WhatIf</span></span>
<span data-ttu-id="a145a-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a145a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a145a-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a145a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a145a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a145a-144">CommonParameters</span></span>
<span data-ttu-id="a145a-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a145a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a145a-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a145a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a145a-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a145a-147">INPUTS</span></span>

### <span data-ttu-id="a145a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a145a-148">System.String</span></span>

### <span data-ttu-id="a145a-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a145a-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a145a-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="a145a-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="a145a-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a145a-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a145a-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a145a-152">OUTPUTS</span></span>

### <span data-ttu-id="a145a-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a145a-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a145a-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a145a-154">NOTES</span></span>

## <span data-ttu-id="a145a-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a145a-155">RELATED LINKS</span></span>

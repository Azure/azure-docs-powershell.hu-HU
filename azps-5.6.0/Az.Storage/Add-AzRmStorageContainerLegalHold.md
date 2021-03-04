---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 8b0608a350f73de4280380abf7fd213d48742022
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930713"
---
# <span data-ttu-id="bfb2b-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="bfb2b-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="bfb2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfb2b-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb2b-103">Jogi holdcímkéket ad egy tároló blobtárolóhoz</span><span class="sxs-lookup"><span data-stu-id="bfb2b-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="bfb2b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bfb2b-104">SYNTAX</span></span>

### <span data-ttu-id="bfb2b-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bfb2b-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb2b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bfb2b-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb2b-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="bfb2b-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfb2b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bfb2b-108">DESCRIPTION</span></span>
<span data-ttu-id="bfb2b-109">Az **Add-AzRmStorageContainerLegalHold** parancsmag jogi visszatartáscímkéket ad egy tároló blobtárolóhoz</span><span class="sxs-lookup"><span data-stu-id="bfb2b-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="bfb2b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bfb2b-110">EXAMPLES</span></span>

### <span data-ttu-id="bfb2b-111">1. példa: Jogi holdcímkék hozzáadása tároló blobtárolóhoz tárfióknévvel és tárolónévvel</span><span class="sxs-lookup"><span data-stu-id="bfb2b-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="bfb2b-112">Ez a parancs jogi tárterületcímkéket ad a tárfiók nevét és tárolónevét tartalmazó tár blobtárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="bfb2b-113">2. példa: Jogi holdcímkék hozzáadása tárterület blobtárolóhoz Tárfiók-objektummal és tárolónévvel</span><span class="sxs-lookup"><span data-stu-id="bfb2b-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="bfb2b-114">Ez a parancs jogi holdcímkéket ad egy Tárfiók-objektummal és tárolónévvel egy Tárfiók-tároló tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="bfb2b-115">3. példa: Jogi holdcímkék hozzáadása az összes tár blobtárolóhoz egy tárfiókban folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="bfb2b-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="bfb2b-116">Ez a parancs jogi holdcímkéket ad a tárfiók összes tárterület-blobtárolója számára.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="bfb2b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfb2b-117">PARAMETERS</span></span>

### <span data-ttu-id="bfb2b-118">-Container</span><span class="sxs-lookup"><span data-stu-id="bfb2b-118">-Container</span></span>
<span data-ttu-id="bfb2b-119">Tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="bfb2b-119">Storage container object</span></span>

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

### <span data-ttu-id="bfb2b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb2b-120">-DefaultProfile</span></span>
<span data-ttu-id="bfb2b-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfb2b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bfb2b-122">-Name</span></span>
<span data-ttu-id="bfb2b-123">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="bfb2b-123">Container Name</span></span>

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

### <span data-ttu-id="bfb2b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb2b-124">-ResourceGroupName</span></span>
<span data-ttu-id="bfb2b-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="bfb2b-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bfb2b-126">-StorageAccount</span></span>
<span data-ttu-id="bfb2b-127">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="bfb2b-127">Storage account object</span></span>

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

### <span data-ttu-id="bfb2b-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bfb2b-128">-StorageAccountName</span></span>
<span data-ttu-id="bfb2b-129">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="bfb2b-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="bfb2b-130">-Tag</span></span>
<span data-ttu-id="bfb2b-131">Container LegalHold Tags</span><span class="sxs-lookup"><span data-stu-id="bfb2b-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="bfb2b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfb2b-132">-Confirm</span></span>
<span data-ttu-id="bfb2b-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfb2b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb2b-134">-WhatIf</span></span>
<span data-ttu-id="bfb2b-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfb2b-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfb2b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb2b-137">CommonParameters</span></span>
<span data-ttu-id="bfb2b-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb2b-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb2b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb2b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfb2b-140">INPUTS</span></span>

### <span data-ttu-id="bfb2b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bfb2b-141">System.String</span></span>

### <span data-ttu-id="bfb2b-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bfb2b-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="bfb2b-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="bfb2b-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="bfb2b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfb2b-144">OUTPUTS</span></span>

### <span data-ttu-id="bfb2b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="bfb2b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="bfb2b-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bfb2b-146">NOTES</span></span>

## <span data-ttu-id="bfb2b-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfb2b-147">RELATED LINKS</span></span>

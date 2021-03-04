---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: def99b11efa5070881cc3226b9ec85449b4cc0b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924194"
---
# <span data-ttu-id="586f0-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="586f0-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="586f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="586f0-102">SYNOPSIS</span></span>
<span data-ttu-id="586f0-103">ACR-jegyzékfájl törlése.</span><span class="sxs-lookup"><span data-stu-id="586f0-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="586f0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="586f0-104">SYNTAX</span></span>

### <span data-ttu-id="586f0-105">ByManifestParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="586f0-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="586f0-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="586f0-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="586f0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="586f0-107">DESCRIPTION</span></span>
<span data-ttu-id="586f0-108">ACR-jegyzékfájl törlése.</span><span class="sxs-lookup"><span data-stu-id="586f0-108">Delete ACR manifest.</span></span>
<span data-ttu-id="586f0-109">A parancsmag futtatásához futtassa a `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="586f0-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="586f0-110">először.</span><span class="sxs-lookup"><span data-stu-id="586f0-110">first.</span></span>

## <span data-ttu-id="586f0-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="586f0-111">EXAMPLES</span></span>

### <span data-ttu-id="586f0-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="586f0-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="586f0-113">Jegyzékfájl törlése sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span><span class="sxs-lookup"><span data-stu-id="586f0-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="586f0-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="586f0-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="586f0-115">Delete manifest with tag latest for repository test/busybox27 under registry</span><span class="sxs-lookup"><span data-stu-id="586f0-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="586f0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="586f0-116">PARAMETERS</span></span>

### <span data-ttu-id="586f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="586f0-117">-DefaultProfile</span></span>
<span data-ttu-id="586f0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="586f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="586f0-119">-Manifest</span><span class="sxs-lookup"><span data-stu-id="586f0-119">-Manifest</span></span>
<span data-ttu-id="586f0-120">Jegyzékfájlra vonatkozó hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="586f0-120">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManifestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586f0-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="586f0-121">-RegistryName</span></span>
<span data-ttu-id="586f0-122">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="586f0-122">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586f0-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="586f0-123">-RepositoryName</span></span>
<span data-ttu-id="586f0-124">Tárnév.</span><span class="sxs-lookup"><span data-stu-id="586f0-124">Repository Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586f0-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="586f0-125">-Tag</span></span>
<span data-ttu-id="586f0-126">Címke jelölőt.</span><span class="sxs-lookup"><span data-stu-id="586f0-126">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586f0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="586f0-127">-Confirm</span></span>
<span data-ttu-id="586f0-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="586f0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="586f0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="586f0-129">-WhatIf</span></span>
<span data-ttu-id="586f0-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="586f0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="586f0-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="586f0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="586f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="586f0-132">CommonParameters</span></span>
<span data-ttu-id="586f0-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="586f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="586f0-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="586f0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="586f0-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="586f0-135">INPUTS</span></span>

### <span data-ttu-id="586f0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="586f0-136">System.String</span></span>

## <span data-ttu-id="586f0-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="586f0-137">OUTPUTS</span></span>

### <span data-ttu-id="586f0-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="586f0-138">System.Boolean</span></span>

## <span data-ttu-id="586f0-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="586f0-139">NOTES</span></span>

## <span data-ttu-id="586f0-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="586f0-140">RELATED LINKS</span></span>

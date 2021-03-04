---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: 1c0ad2ae46987a526be4e8fda110dada914bd27e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930338"
---
# <span data-ttu-id="62a00-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="62a00-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="62a00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62a00-102">SYNOPSIS</span></span>
<span data-ttu-id="62a00-103">Tárház törlése az ACR-fájlból</span><span class="sxs-lookup"><span data-stu-id="62a00-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="62a00-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="62a00-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62a00-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="62a00-105">DESCRIPTION</span></span>
<span data-ttu-id="62a00-106">Tárház törlése az ACR-fájlból</span><span class="sxs-lookup"><span data-stu-id="62a00-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="62a00-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="62a00-107">EXAMPLES</span></span>

### <span data-ttu-id="62a00-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="62a00-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="62a00-109">Törölje a tárházi tesztet/busybox15-öt a beállításjegyzékből.</span><span class="sxs-lookup"><span data-stu-id="62a00-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="62a00-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62a00-110">PARAMETERS</span></span>

### <span data-ttu-id="62a00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a00-111">-DefaultProfile</span></span>
<span data-ttu-id="62a00-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62a00-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62a00-113">-Name</span><span class="sxs-lookup"><span data-stu-id="62a00-113">-Name</span></span>
<span data-ttu-id="62a00-114">Tárnév.</span><span class="sxs-lookup"><span data-stu-id="62a00-114">Repository Name.</span></span>

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

### <span data-ttu-id="62a00-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="62a00-115">-RegistryName</span></span>
<span data-ttu-id="62a00-116">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="62a00-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="62a00-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62a00-117">-Confirm</span></span>
<span data-ttu-id="62a00-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="62a00-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62a00-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a00-119">-WhatIf</span></span>
<span data-ttu-id="62a00-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="62a00-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62a00-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62a00-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62a00-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a00-122">CommonParameters</span></span>
<span data-ttu-id="62a00-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62a00-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a00-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62a00-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a00-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62a00-125">INPUTS</span></span>

### <span data-ttu-id="62a00-126">System.String</span><span class="sxs-lookup"><span data-stu-id="62a00-126">System.String</span></span>

## <span data-ttu-id="62a00-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62a00-127">OUTPUTS</span></span>

### <span data-ttu-id="62a00-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeetedRepository</span><span class="sxs-lookup"><span data-stu-id="62a00-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="62a00-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="62a00-129">NOTES</span></span>

## <span data-ttu-id="62a00-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62a00-130">RELATED LINKS</span></span>

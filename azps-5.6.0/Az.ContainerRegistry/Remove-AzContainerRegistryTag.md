---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 6fbc5b33bb8e9c865b5ea869deed5044ee08198f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920825"
---
# <span data-ttu-id="767ed-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="767ed-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="767ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="767ed-102">SYNOPSIS</span></span>
<span data-ttu-id="767ed-103">ACR címke címkézésének visszacímkézetlene.</span><span class="sxs-lookup"><span data-stu-id="767ed-103">Untag ACR tag.</span></span>

## <span data-ttu-id="767ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="767ed-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="767ed-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="767ed-105">DESCRIPTION</span></span>
<span data-ttu-id="767ed-106">ACR címke címkézésének visszacímkézetlene.</span><span class="sxs-lookup"><span data-stu-id="767ed-106">Untag ACR tag.</span></span>
<span data-ttu-id="767ed-107">A parancsmag futtatásához futtassa a `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="767ed-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="767ed-108">először.</span><span class="sxs-lookup"><span data-stu-id="767ed-108">first.</span></span>

## <span data-ttu-id="767ed-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="767ed-109">EXAMPLES</span></span>

### <span data-ttu-id="767ed-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="767ed-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="767ed-111">Untag alpine:tag under registry.</span><span class="sxs-lookup"><span data-stu-id="767ed-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="767ed-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="767ed-112">PARAMETERS</span></span>

### <span data-ttu-id="767ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="767ed-113">-DefaultProfile</span></span>
<span data-ttu-id="767ed-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="767ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="767ed-115">-Name</span><span class="sxs-lookup"><span data-stu-id="767ed-115">-Name</span></span>
<span data-ttu-id="767ed-116">Címke jelölőt.</span><span class="sxs-lookup"><span data-stu-id="767ed-116">Tag.</span></span>

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

### <span data-ttu-id="767ed-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="767ed-117">-RegistryName</span></span>
<span data-ttu-id="767ed-118">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="767ed-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="767ed-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="767ed-119">-RepositoryName</span></span>
<span data-ttu-id="767ed-120">Tárnév.</span><span class="sxs-lookup"><span data-stu-id="767ed-120">Repository Name.</span></span>

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

### <span data-ttu-id="767ed-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="767ed-121">-Confirm</span></span>
<span data-ttu-id="767ed-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="767ed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="767ed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="767ed-123">-WhatIf</span></span>
<span data-ttu-id="767ed-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="767ed-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="767ed-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="767ed-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="767ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="767ed-126">CommonParameters</span></span>
<span data-ttu-id="767ed-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="767ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="767ed-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="767ed-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="767ed-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="767ed-129">INPUTS</span></span>

### <span data-ttu-id="767ed-130">System.String</span><span class="sxs-lookup"><span data-stu-id="767ed-130">System.String</span></span>

## <span data-ttu-id="767ed-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="767ed-131">OUTPUTS</span></span>

### <span data-ttu-id="767ed-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="767ed-132">System.Boolean</span></span>

## <span data-ttu-id="767ed-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="767ed-133">NOTES</span></span>

## <span data-ttu-id="767ed-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="767ed-134">RELATED LINKS</span></span>

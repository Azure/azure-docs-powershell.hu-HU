---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 7e6528630c731b15f906d79de45bc50f94b2a715
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166330"
---
# <span data-ttu-id="05efa-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="05efa-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="05efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05efa-102">SYNOPSIS</span></span>
<span data-ttu-id="05efa-103">ACR címke címkézésének visszacímkézetlene.</span><span class="sxs-lookup"><span data-stu-id="05efa-103">Untag ACR tag.</span></span>

## <span data-ttu-id="05efa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="05efa-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05efa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="05efa-105">DESCRIPTION</span></span>
<span data-ttu-id="05efa-106">ACR címke címkézésének visszacímkézetlene.</span><span class="sxs-lookup"><span data-stu-id="05efa-106">Untag ACR tag.</span></span>
<span data-ttu-id="05efa-107">A parancsmag futtatásához futtassa a `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="05efa-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="05efa-108">először.</span><span class="sxs-lookup"><span data-stu-id="05efa-108">first.</span></span>

## <span data-ttu-id="05efa-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="05efa-109">EXAMPLES</span></span>

### <span data-ttu-id="05efa-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="05efa-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="05efa-111">Untag alpine:tag under registry.</span><span class="sxs-lookup"><span data-stu-id="05efa-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="05efa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05efa-112">PARAMETERS</span></span>

### <span data-ttu-id="05efa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05efa-113">-DefaultProfile</span></span>
<span data-ttu-id="05efa-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05efa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05efa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="05efa-115">-Name</span></span>
<span data-ttu-id="05efa-116">Címke jelölőt.</span><span class="sxs-lookup"><span data-stu-id="05efa-116">Tag.</span></span>

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

### <span data-ttu-id="05efa-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="05efa-117">-RegistryName</span></span>
<span data-ttu-id="05efa-118">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="05efa-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="05efa-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="05efa-119">-RepositoryName</span></span>
<span data-ttu-id="05efa-120">Tárnév.</span><span class="sxs-lookup"><span data-stu-id="05efa-120">Repository Name.</span></span>

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

### <span data-ttu-id="05efa-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05efa-121">-Confirm</span></span>
<span data-ttu-id="05efa-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="05efa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05efa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05efa-123">-WhatIf</span></span>
<span data-ttu-id="05efa-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="05efa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05efa-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05efa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05efa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05efa-126">CommonParameters</span></span>
<span data-ttu-id="05efa-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05efa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05efa-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05efa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05efa-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05efa-129">INPUTS</span></span>

### <span data-ttu-id="05efa-130">System.String</span><span class="sxs-lookup"><span data-stu-id="05efa-130">System.String</span></span>

## <span data-ttu-id="05efa-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05efa-131">OUTPUTS</span></span>

### <span data-ttu-id="05efa-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="05efa-132">System.Boolean</span></span>

## <span data-ttu-id="05efa-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="05efa-133">NOTES</span></span>

## <span data-ttu-id="05efa-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05efa-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
ms.openlocfilehash: 45572cbd2255a604e492c7740d1749a0ad968845
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920754"
---
# <span data-ttu-id="1d2d5-101">Update-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="1d2d5-101">Update-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="1d2d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="1d2d5-103">Frissítse az ACR-tárházat.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-103">Update ACR repository.</span></span>

## <span data-ttu-id="1d2d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d2d5-104">SYNTAX</span></span>

```
Update-AzContainerRegistryRepository -Name <String> [-DeleteEnabled <Boolean>] [-WriteEnabled <Boolean>]
 [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d2d5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d2d5-105">DESCRIPTION</span></span>
<span data-ttu-id="1d2d5-106">Frissítse az ACR-tárházat.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-106">Update ACR repository.</span></span>

## <span data-ttu-id="1d2d5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d2d5-107">EXAMPLES</span></span>

### <span data-ttu-id="1d2d5-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1d2d5-108">Example 1</span></span>
```powershell
Update-AzContainerRegistryRepository -RegistryName registry -Name test/busybox8 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry             : registry.azurecr.io
ImageName            : test/busybox8
CreatedTime          : 2020-12-11T08:57:56.2070002Z
LastUpdateTime       : 2020-12-11T08:57:56.5188237Z
ManifestCount        : 1
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="1d2d5-109">Frissítse a tárház alpesi fájlok attribútumát a beállításjegyzékben.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-109">Update attributes for repository alpine under registry.</span></span>

## <span data-ttu-id="1d2d5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d2d5-110">PARAMETERS</span></span>

### <span data-ttu-id="1d2d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d2d5-111">-DefaultProfile</span></span>
<span data-ttu-id="1d2d5-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d2d5-113">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="1d2d5-113">-DeleteEnabled</span></span>
<span data-ttu-id="1d2d5-114">Engedélyezés törlése gombra.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-114">Delete enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d2d5-115">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="1d2d5-115">-ListEnabled</span></span>
<span data-ttu-id="1d2d5-116">Lista engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-116">List enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d2d5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1d2d5-117">-Name</span></span>
<span data-ttu-id="1d2d5-118">Tárnév.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-118">Repository Name.</span></span>

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

### <span data-ttu-id="1d2d5-119">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="1d2d5-119">-ReadEnabled</span></span>
<span data-ttu-id="1d2d5-120">Engedélyezés elolvasva.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-120">Read enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d2d5-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="1d2d5-121">-RegistryName</span></span>
<span data-ttu-id="1d2d5-122">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="1d2d5-123">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="1d2d5-123">-WriteEnabled</span></span>
<span data-ttu-id="1d2d5-124">Írási engedélyezés.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-124">Write enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d2d5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d2d5-125">-Confirm</span></span>
<span data-ttu-id="1d2d5-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d2d5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d2d5-127">-WhatIf</span></span>
<span data-ttu-id="1d2d5-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d2d5-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d2d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d2d5-130">CommonParameters</span></span>
<span data-ttu-id="1d2d5-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d2d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d2d5-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d2d5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d2d5-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d2d5-133">INPUTS</span></span>

### <span data-ttu-id="1d2d5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1d2d5-134">System.String</span></span>

## <span data-ttu-id="1d2d5-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d2d5-135">OUTPUTS</span></span>

### <span data-ttu-id="1d2d5-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="1d2d5-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="1d2d5-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d2d5-137">NOTES</span></span>

## <span data-ttu-id="1d2d5-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d2d5-138">RELATED LINKS</span></span>

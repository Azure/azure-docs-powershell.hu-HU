---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 48fb77eb9c718a09a7e13e6d6ab5af5bfc60c912
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204663"
---
# <span data-ttu-id="5d3d4-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="5d3d4-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="5d3d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3d4-103">Frissítse az ACR címkét.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-103">Update ACR tag.</span></span>

## <span data-ttu-id="5d3d4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d3d4-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d3d4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d3d4-105">DESCRIPTION</span></span>
<span data-ttu-id="5d3d4-106">Frissítse az ACR címkét.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-106">Update ACR tag.</span></span>
<span data-ttu-id="5d3d4-107">A parancsmag futtatásához futtassa a `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="5d3d4-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="5d3d4-108">először.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-108">first.</span></span>

## <span data-ttu-id="5d3d4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d3d4-109">EXAMPLES</span></span>

### <span data-ttu-id="5d3d4-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="5d3d4-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="5d3d4-111">Frissítse a legújabb címke attribútumát a beállításjegyzékben.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="5d3d4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d3d4-112">PARAMETERS</span></span>

### <span data-ttu-id="5d3d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3d4-113">-DefaultProfile</span></span>
<span data-ttu-id="5d3d4-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d3d4-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="5d3d4-115">-DeleteEnabled</span></span>
<span data-ttu-id="5d3d4-116">Engedélyezés törlése gombra.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-116">Delete enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d4-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="5d3d4-117">-ListEnabled</span></span>
<span data-ttu-id="5d3d4-118">Lista engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-118">List enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5d3d4-119">-Name</span></span>
<span data-ttu-id="5d3d4-120">Címke jelölőt.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-120">Tag.</span></span>

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

### <span data-ttu-id="5d3d4-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="5d3d4-121">-ReadEnabled</span></span>
<span data-ttu-id="5d3d4-122">Engedélyezés elolvasva.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-122">Read enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d4-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5d3d4-123">-RegistryName</span></span>
<span data-ttu-id="5d3d4-124">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="5d3d4-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="5d3d4-125">-RepositoryName</span></span>
<span data-ttu-id="5d3d4-126">Tárnév.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-126">Repository Name.</span></span>

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

### <span data-ttu-id="5d3d4-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="5d3d4-127">-WriteEnabled</span></span>
<span data-ttu-id="5d3d4-128">Írási engedélyezés.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-128">Write enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d3d4-129">-Confirm</span></span>
<span data-ttu-id="5d3d4-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d3d4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d3d4-131">-WhatIf</span></span>
<span data-ttu-id="5d3d4-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d3d4-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d3d4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3d4-134">CommonParameters</span></span>
<span data-ttu-id="5d3d4-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d3d4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3d4-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d3d4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3d4-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d3d4-137">INPUTS</span></span>

### <span data-ttu-id="5d3d4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5d3d4-138">System.String</span></span>

## <span data-ttu-id="5d3d4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d3d4-139">OUTPUTS</span></span>

### <span data-ttu-id="5d3d4-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="5d3d4-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="5d3d4-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d3d4-141">NOTES</span></span>

## <span data-ttu-id="5d3d4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d3d4-142">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 68d4eab2088bc1091d812399aade67659d7db31b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920753"
---
# <span data-ttu-id="95352-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="95352-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="95352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95352-102">SYNOPSIS</span></span>
<span data-ttu-id="95352-103">Frissítse az ACR címkét.</span><span class="sxs-lookup"><span data-stu-id="95352-103">Update ACR tag.</span></span>

## <span data-ttu-id="95352-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="95352-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95352-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="95352-105">DESCRIPTION</span></span>
<span data-ttu-id="95352-106">Frissítse az ACR címkét.</span><span class="sxs-lookup"><span data-stu-id="95352-106">Update ACR tag.</span></span>
<span data-ttu-id="95352-107">A parancsmag futtatásához futtassa a `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="95352-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="95352-108">először.</span><span class="sxs-lookup"><span data-stu-id="95352-108">first.</span></span>

## <span data-ttu-id="95352-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="95352-109">EXAMPLES</span></span>

### <span data-ttu-id="95352-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="95352-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="95352-111">Frissítse a legújabb címke attribútumát a beállításjegyzékben.</span><span class="sxs-lookup"><span data-stu-id="95352-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="95352-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95352-112">PARAMETERS</span></span>

### <span data-ttu-id="95352-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95352-113">-DefaultProfile</span></span>
<span data-ttu-id="95352-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95352-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95352-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="95352-115">-DeleteEnabled</span></span>
<span data-ttu-id="95352-116">Engedélyezés törlése gombra.</span><span class="sxs-lookup"><span data-stu-id="95352-116">Delete enable.</span></span>

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

### <span data-ttu-id="95352-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="95352-117">-ListEnabled</span></span>
<span data-ttu-id="95352-118">Lista engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="95352-118">List enable.</span></span>

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

### <span data-ttu-id="95352-119">-Name</span><span class="sxs-lookup"><span data-stu-id="95352-119">-Name</span></span>
<span data-ttu-id="95352-120">Címke jelölőt.</span><span class="sxs-lookup"><span data-stu-id="95352-120">Tag.</span></span>

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

### <span data-ttu-id="95352-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="95352-121">-ReadEnabled</span></span>
<span data-ttu-id="95352-122">Engedélyezés elolvasva.</span><span class="sxs-lookup"><span data-stu-id="95352-122">Read enable.</span></span>

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

### <span data-ttu-id="95352-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="95352-123">-RegistryName</span></span>
<span data-ttu-id="95352-124">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="95352-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="95352-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="95352-125">-RepositoryName</span></span>
<span data-ttu-id="95352-126">Tárnév.</span><span class="sxs-lookup"><span data-stu-id="95352-126">Repository Name.</span></span>

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

### <span data-ttu-id="95352-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="95352-127">-WriteEnabled</span></span>
<span data-ttu-id="95352-128">Írási engedélyezés.</span><span class="sxs-lookup"><span data-stu-id="95352-128">Write enable.</span></span>

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

### <span data-ttu-id="95352-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95352-129">-Confirm</span></span>
<span data-ttu-id="95352-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="95352-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95352-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95352-131">-WhatIf</span></span>
<span data-ttu-id="95352-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="95352-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95352-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95352-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95352-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95352-134">CommonParameters</span></span>
<span data-ttu-id="95352-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95352-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95352-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95352-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95352-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95352-137">INPUTS</span></span>

### <span data-ttu-id="95352-138">System.String</span><span class="sxs-lookup"><span data-stu-id="95352-138">System.String</span></span>

## <span data-ttu-id="95352-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95352-139">OUTPUTS</span></span>

### <span data-ttu-id="95352-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="95352-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="95352-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="95352-141">NOTES</span></span>

## <span data-ttu-id="95352-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95352-142">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
ms.openlocfilehash: 030f0b00ba77bc967a53ce43c4f08d66c214f67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920761"
---
# <span data-ttu-id="11b32-101">Update-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="11b32-101">Update-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="11b32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11b32-102">SYNOPSIS</span></span>
<span data-ttu-id="11b32-103">ACR jegyzékfájl frissítése.</span><span class="sxs-lookup"><span data-stu-id="11b32-103">Update ACR manifest.</span></span> 

## <span data-ttu-id="11b32-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11b32-104">SYNTAX</span></span>

### <span data-ttu-id="11b32-105">ByManifestParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11b32-105">ByManifestParameterSet (Default)</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11b32-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="11b32-106">ByTagParameterSet</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11b32-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11b32-107">DESCRIPTION</span></span>
<span data-ttu-id="11b32-108">ACR jegyzékfájl frissítése.</span><span class="sxs-lookup"><span data-stu-id="11b32-108">Update ACR manifest.</span></span>
<span data-ttu-id="11b32-109">A parancsmag futtatásához futtassa a `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="11b32-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="11b32-110">először.</span><span class="sxs-lookup"><span data-stu-id="11b32-110">first.</span></span>

## <span data-ttu-id="11b32-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11b32-111">EXAMPLES</span></span>

### <span data-ttu-id="11b32-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="11b32-112">Example 1</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="11b32-113">A jegyzékfájl sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 beállításjegyzékben.</span><span class="sxs-lookup"><span data-stu-id="11b32-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span></span>

### <span data-ttu-id="11b32-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="11b32-114">Example 2</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Tag latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="11b32-115">A jegyzékfájl attribútumainak frissítése a beállításjegyzékben a legújabb címkével.</span><span class="sxs-lookup"><span data-stu-id="11b32-115">Update attributes for manifest with tag latest under registry.</span></span>

## <span data-ttu-id="11b32-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11b32-116">PARAMETERS</span></span>

### <span data-ttu-id="11b32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b32-117">-DefaultProfile</span></span>
<span data-ttu-id="11b32-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11b32-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11b32-119">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="11b32-119">-DeleteEnabled</span></span>
<span data-ttu-id="11b32-120">Engedélyezés törlése gombra.</span><span class="sxs-lookup"><span data-stu-id="11b32-120">Delete enable.</span></span>

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

### <span data-ttu-id="11b32-121">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="11b32-121">-ListEnabled</span></span>
<span data-ttu-id="11b32-122">Lista engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="11b32-122">List enable.</span></span>

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

### <span data-ttu-id="11b32-123">-Manifest</span><span class="sxs-lookup"><span data-stu-id="11b32-123">-Manifest</span></span>
<span data-ttu-id="11b32-124">Jegyzékfájlra vonatkozó hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="11b32-124">Manifest reference.</span></span>

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

### <span data-ttu-id="11b32-125">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="11b32-125">-ReadEnabled</span></span>
<span data-ttu-id="11b32-126">Engedélyezés elolvasva.</span><span class="sxs-lookup"><span data-stu-id="11b32-126">Read enable.</span></span>

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

### <span data-ttu-id="11b32-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="11b32-127">-RegistryName</span></span>
<span data-ttu-id="11b32-128">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="11b32-128">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="11b32-129">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="11b32-129">-RepositoryName</span></span>
<span data-ttu-id="11b32-130">Tárnév.</span><span class="sxs-lookup"><span data-stu-id="11b32-130">Repository Name.</span></span>

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

### <span data-ttu-id="11b32-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="11b32-131">-Tag</span></span>
<span data-ttu-id="11b32-132">Címke jelölőt.</span><span class="sxs-lookup"><span data-stu-id="11b32-132">Tag.</span></span>

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

### <span data-ttu-id="11b32-133">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="11b32-133">-WriteEnabled</span></span>
<span data-ttu-id="11b32-134">Írási engedélyezés.</span><span class="sxs-lookup"><span data-stu-id="11b32-134">Write enable.</span></span>

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

### <span data-ttu-id="11b32-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11b32-135">-Confirm</span></span>
<span data-ttu-id="11b32-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="11b32-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b32-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b32-137">-WhatIf</span></span>
<span data-ttu-id="11b32-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="11b32-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11b32-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11b32-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b32-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b32-140">CommonParameters</span></span>
<span data-ttu-id="11b32-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b32-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b32-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11b32-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b32-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11b32-143">INPUTS</span></span>

### <span data-ttu-id="11b32-144">System.String</span><span class="sxs-lookup"><span data-stu-id="11b32-144">System.String</span></span>

## <span data-ttu-id="11b32-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11b32-145">OUTPUTS</span></span>

### <span data-ttu-id="11b32-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="11b32-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

## <span data-ttu-id="11b32-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11b32-147">NOTES</span></span>

## <span data-ttu-id="11b32-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11b32-148">RELATED LINKS</span></span>

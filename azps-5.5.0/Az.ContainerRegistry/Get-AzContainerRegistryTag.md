---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 88bf3648f416efa69576c6b09a0d59f0d0d0fa76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148707"
---
# <span data-ttu-id="6e1f5-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="6e1f5-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="6e1f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1f5-103">ACR-címke be- vagy listába való be- és listába hozása</span><span class="sxs-lookup"><span data-stu-id="6e1f5-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="6e1f5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e1f5-104">SYNTAX</span></span>

### <span data-ttu-id="6e1f5-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e1f5-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e1f5-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e1f5-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e1f5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e1f5-107">DESCRIPTION</span></span>
<span data-ttu-id="6e1f5-108">ACR-címke be- vagy listába való be- és listába hozása</span><span class="sxs-lookup"><span data-stu-id="6e1f5-108">Get or list ACR tag.</span></span>
<span data-ttu-id="6e1f5-109">A parancsmag futtatásához futtassa a `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="6e1f5-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="6e1f5-110">először.</span><span class="sxs-lookup"><span data-stu-id="6e1f5-110">first.</span></span>

## <span data-ttu-id="6e1f5-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e1f5-111">EXAMPLES</span></span>

### <span data-ttu-id="6e1f5-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="6e1f5-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="6e1f5-113">List tags for repository alpine under registry.</span><span class="sxs-lookup"><span data-stu-id="6e1f5-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="6e1f5-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="6e1f5-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="6e1f5-115">A beállításjegyzékben a legújabb címkét kap az alpine-adattárhoz.</span><span class="sxs-lookup"><span data-stu-id="6e1f5-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="6e1f5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e1f5-116">PARAMETERS</span></span>

### <span data-ttu-id="6e1f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1f5-117">-DefaultProfile</span></span>
<span data-ttu-id="6e1f5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e1f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e1f5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6e1f5-119">-Name</span></span>
<span data-ttu-id="6e1f5-120">Címke jelölőt.</span><span class="sxs-lookup"><span data-stu-id="6e1f5-120">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: GetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e1f5-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="6e1f5-121">-RegistryName</span></span>
<span data-ttu-id="6e1f5-122">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="6e1f5-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="6e1f5-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="6e1f5-123">-RepositoryName</span></span>
<span data-ttu-id="6e1f5-124">Tárnév.</span><span class="sxs-lookup"><span data-stu-id="6e1f5-124">Repository Name.</span></span>

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

### <span data-ttu-id="6e1f5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1f5-125">CommonParameters</span></span>
<span data-ttu-id="6e1f5-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e1f5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1f5-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e1f5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1f5-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e1f5-128">INPUTS</span></span>

### <span data-ttu-id="6e1f5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6e1f5-129">System.String</span></span>

## <span data-ttu-id="6e1f5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e1f5-130">OUTPUTS</span></span>

### <span data-ttu-id="6e1f5-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="6e1f5-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="6e1f5-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span><span class="sxs-lookup"><span data-stu-id="6e1f5-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="6e1f5-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e1f5-133">NOTES</span></span>

## <span data-ttu-id="6e1f5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e1f5-134">RELATED LINKS</span></span>

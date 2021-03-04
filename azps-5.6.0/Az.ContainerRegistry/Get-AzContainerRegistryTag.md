---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 37308ab02db132e03cf4f44536bc44d0d6845a86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938225"
---
# <span data-ttu-id="c62c9-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="c62c9-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="c62c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c62c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c62c9-103">ACR-címke be- vagy listába való be- és listába hozása</span><span class="sxs-lookup"><span data-stu-id="c62c9-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="c62c9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c62c9-104">SYNTAX</span></span>

### <span data-ttu-id="c62c9-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c62c9-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c62c9-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="c62c9-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c62c9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c62c9-107">DESCRIPTION</span></span>
<span data-ttu-id="c62c9-108">ACR-címke be- vagy listába való be- és listába hozása</span><span class="sxs-lookup"><span data-stu-id="c62c9-108">Get or list ACR tag.</span></span>
<span data-ttu-id="c62c9-109">A parancsmag futtatásához futtassa a `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="c62c9-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="c62c9-110">először.</span><span class="sxs-lookup"><span data-stu-id="c62c9-110">first.</span></span>

## <span data-ttu-id="c62c9-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c62c9-111">EXAMPLES</span></span>

### <span data-ttu-id="c62c9-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c62c9-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="c62c9-113">List tags for repository alpine under registry.</span><span class="sxs-lookup"><span data-stu-id="c62c9-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="c62c9-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c62c9-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="c62c9-115">A beállításjegyzékben a legújabb címkét kap az alpine-adattárhoz.</span><span class="sxs-lookup"><span data-stu-id="c62c9-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="c62c9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c62c9-116">PARAMETERS</span></span>

### <span data-ttu-id="c62c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c62c9-117">-DefaultProfile</span></span>
<span data-ttu-id="c62c9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c62c9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c62c9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c62c9-119">-Name</span></span>
<span data-ttu-id="c62c9-120">Címke jelölőt.</span><span class="sxs-lookup"><span data-stu-id="c62c9-120">Tag.</span></span>

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

### <span data-ttu-id="c62c9-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c62c9-121">-RegistryName</span></span>
<span data-ttu-id="c62c9-122">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="c62c9-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="c62c9-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="c62c9-123">-RepositoryName</span></span>
<span data-ttu-id="c62c9-124">Tárnév.</span><span class="sxs-lookup"><span data-stu-id="c62c9-124">Repository Name.</span></span>

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

### <span data-ttu-id="c62c9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c62c9-125">CommonParameters</span></span>
<span data-ttu-id="c62c9-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c62c9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c62c9-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c62c9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c62c9-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c62c9-128">INPUTS</span></span>

### <span data-ttu-id="c62c9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c62c9-129">System.String</span></span>

## <span data-ttu-id="c62c9-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c62c9-130">OUTPUTS</span></span>

### <span data-ttu-id="c62c9-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="c62c9-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="c62c9-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span><span class="sxs-lookup"><span data-stu-id="c62c9-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="c62c9-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c62c9-133">NOTES</span></span>

## <span data-ttu-id="c62c9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c62c9-134">RELATED LINKS</span></span>

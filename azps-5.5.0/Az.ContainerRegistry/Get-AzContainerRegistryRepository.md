---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: 7da65515138ff6afa97e6c05f9baa764d6ab920c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164146"
---
# <span data-ttu-id="98c17-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="98c17-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="98c17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98c17-102">SYNOPSIS</span></span>
<span data-ttu-id="98c17-103">ACR-adattárak le- vagy listába való be- és listából.</span><span class="sxs-lookup"><span data-stu-id="98c17-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="98c17-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="98c17-104">SYNTAX</span></span>

### <span data-ttu-id="98c17-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98c17-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98c17-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="98c17-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c17-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="98c17-107">DESCRIPTION</span></span>
<span data-ttu-id="98c17-108">ACR-adattárak le- vagy listába való be- és listából.</span><span class="sxs-lookup"><span data-stu-id="98c17-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="98c17-109">A lista csak az adattárneveket adja vissza.</span><span class="sxs-lookup"><span data-stu-id="98c17-109">List returns repository names only.</span></span>

## <span data-ttu-id="98c17-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="98c17-110">EXAMPLES</span></span>

### <span data-ttu-id="98c17-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="98c17-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="98c17-112">List all repositories in registry.</span><span class="sxs-lookup"><span data-stu-id="98c17-112">List all repositories in registry.</span></span>

### <span data-ttu-id="98c17-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="98c17-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="98c17-114">List first 3 repositories in registry.</span><span class="sxs-lookup"><span data-stu-id="98c17-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="98c17-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="98c17-115">Example 3</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -Name alpine

Registry             : registry.azurecr.io
ImageName            : alpine
CreatedTime          : 2020-10-13T05:45:25.5896115Z
LastUpdateTime       : 2021-01-04T08:31:46.2406505Z
ManifestCount        : 7
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="98c17-116">Szerezze be a tár alpesi fájlokat a beállításjegyzék alatt.</span><span class="sxs-lookup"><span data-stu-id="98c17-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="98c17-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98c17-117">PARAMETERS</span></span>

### <span data-ttu-id="98c17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c17-118">-DefaultProfile</span></span>
<span data-ttu-id="98c17-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98c17-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98c17-120">-Name</span><span class="sxs-lookup"><span data-stu-id="98c17-120">-Name</span></span>
<span data-ttu-id="98c17-121">Tárnév.</span><span class="sxs-lookup"><span data-stu-id="98c17-121">Repository Name.</span></span>

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

### <span data-ttu-id="98c17-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="98c17-122">-RegistryName</span></span>
<span data-ttu-id="98c17-123">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="98c17-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="98c17-124">-First</span><span class="sxs-lookup"><span data-stu-id="98c17-124">-First</span></span>
<span data-ttu-id="98c17-125">Első n eredmény.</span><span class="sxs-lookup"><span data-stu-id="98c17-125">First n results.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c17-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c17-126">CommonParameters</span></span>
<span data-ttu-id="98c17-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c17-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c17-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98c17-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c17-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98c17-129">INPUTS</span></span>

### <span data-ttu-id="98c17-130">System.String</span><span class="sxs-lookup"><span data-stu-id="98c17-130">System.String</span></span>

## <span data-ttu-id="98c17-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98c17-131">OUTPUTS</span></span>

### <span data-ttu-id="98c17-132">System.String</span><span class="sxs-lookup"><span data-stu-id="98c17-132">System.String</span></span>

### <span data-ttu-id="98c17-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="98c17-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="98c17-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="98c17-134">NOTES</span></span>

## <span data-ttu-id="98c17-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98c17-135">RELATED LINKS</span></span>

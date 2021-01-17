---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: e7d84439b2292d70604f3f7d9e827a0d8cc035e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480639"
---
# <span data-ttu-id="88c93-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="88c93-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="88c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88c93-102">SYNOPSIS</span></span>
<span data-ttu-id="88c93-103">Azure container registry használatának lekérte.</span><span class="sxs-lookup"><span data-stu-id="88c93-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="88c93-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="88c93-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88c93-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="88c93-105">DESCRIPTION</span></span>
<span data-ttu-id="88c93-106">Azure container registry használatának lekérte.</span><span class="sxs-lookup"><span data-stu-id="88c93-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="88c93-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="88c93-107">EXAMPLES</span></span>

### <span data-ttu-id="88c93-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="88c93-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="88c93-109">Azure container registry használatának lekérte.</span><span class="sxs-lookup"><span data-stu-id="88c93-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="88c93-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88c93-110">PARAMETERS</span></span>

### <span data-ttu-id="88c93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c93-111">-DefaultProfile</span></span>
<span data-ttu-id="88c93-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88c93-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88c93-113">-Name</span><span class="sxs-lookup"><span data-stu-id="88c93-113">-Name</span></span>
<span data-ttu-id="88c93-114">Cél beállításjegyzék neve.</span><span class="sxs-lookup"><span data-stu-id="88c93-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c93-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88c93-115">-ResourceGroupName</span></span>
<span data-ttu-id="88c93-116">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="88c93-116">Resource group name.</span></span>

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

### <span data-ttu-id="88c93-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c93-117">CommonParameters</span></span>
<span data-ttu-id="88c93-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88c93-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c93-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88c93-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c93-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88c93-120">INPUTS</span></span>

### <span data-ttu-id="88c93-121">System.String</span><span class="sxs-lookup"><span data-stu-id="88c93-121">System.String</span></span>

## <span data-ttu-id="88c93-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88c93-122">OUTPUTS</span></span>

### <span data-ttu-id="88c93-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="88c93-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="88c93-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="88c93-124">NOTES</span></span>

## <span data-ttu-id="88c93-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88c93-125">RELATED LINKS</span></span>

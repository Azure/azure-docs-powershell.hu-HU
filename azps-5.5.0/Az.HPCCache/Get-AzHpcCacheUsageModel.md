---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 4552de7be0f2a489aa152a922e39df623736f842
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209415"
---
# <span data-ttu-id="20917-101">Get-AzHpcCacheUsageModel</span><span class="sxs-lookup"><span data-stu-id="20917-101">Get-AzHpcCacheUsageModel</span></span>

## <span data-ttu-id="20917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20917-102">SYNOPSIS</span></span>
<span data-ttu-id="20917-103">Az NFS tárterület célhelyének összes használatiModelsét beveszi.</span><span class="sxs-lookup"><span data-stu-id="20917-103">Gets all usageModels for NFS Storage Target.</span></span>

## <span data-ttu-id="20917-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="20917-104">SYNTAX</span></span>

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20917-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="20917-105">DESCRIPTION</span></span>
<span data-ttu-id="20917-106">A **Get-AzHpcCacheUsageModel** parancsmag az NFS Storage Target használati modelljeinek listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="20917-106">The **Get-AzHpcCacheUsageModel** cmdlet returns a list of usage models for NFS Storage Target.</span></span>

## <span data-ttu-id="20917-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="20917-107">EXAMPLES</span></span>

### <span data-ttu-id="20917-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="20917-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheUsageModel
```

## <span data-ttu-id="20917-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20917-109">PARAMETERS</span></span>

### <span data-ttu-id="20917-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20917-110">-DefaultProfile</span></span>
<span data-ttu-id="20917-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20917-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20917-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20917-112">CommonParameters</span></span>
<span data-ttu-id="20917-113">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20917-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20917-114">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20917-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20917-115">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20917-115">INPUTS</span></span>

### <span data-ttu-id="20917-116">Nincs</span><span class="sxs-lookup"><span data-stu-id="20917-116">None</span></span>

## <span data-ttu-id="20917-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20917-117">OUTPUTS</span></span>

### <span data-ttu-id="20917-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span><span class="sxs-lookup"><span data-stu-id="20917-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span></span>

### <span data-ttu-id="20917-119">System.Object</span><span class="sxs-lookup"><span data-stu-id="20917-119">System.Object</span></span>
## <span data-ttu-id="20917-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="20917-120">NOTES</span></span>

## <span data-ttu-id="20917-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20917-121">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 4552de7be0f2a489aa152a922e39df623736f842
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322807"
---
# <span data-ttu-id="7bc9b-101">Get-AzHpcCacheUsageModel</span><span class="sxs-lookup"><span data-stu-id="7bc9b-101">Get-AzHpcCacheUsageModel</span></span>

## <span data-ttu-id="7bc9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bc9b-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc9b-103">Az NFS Storage Target összes használatiModels-ét beveszi.</span><span class="sxs-lookup"><span data-stu-id="7bc9b-103">Gets all usageModels for NFS Storage Target.</span></span>

## <span data-ttu-id="7bc9b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7bc9b-104">SYNTAX</span></span>

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bc9b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7bc9b-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc9b-106">A **Get-AzHpcCacheUsageModel** parancsmag az NFS-tároló célhely használati modelljeinek listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="7bc9b-106">The **Get-AzHpcCacheUsageModel** cmdlet returns a list of usage models for NFS Storage Target.</span></span>

## <span data-ttu-id="7bc9b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7bc9b-107">EXAMPLES</span></span>

### <span data-ttu-id="7bc9b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7bc9b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheUsageModel
```

## <span data-ttu-id="7bc9b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bc9b-109">PARAMETERS</span></span>

### <span data-ttu-id="7bc9b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc9b-110">-DefaultProfile</span></span>
<span data-ttu-id="7bc9b-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bc9b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bc9b-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc9b-112">CommonParameters</span></span>
<span data-ttu-id="7bc9b-113">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc9b-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc9b-114">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bc9b-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc9b-115">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bc9b-115">INPUTS</span></span>

### <span data-ttu-id="7bc9b-116">Nincs</span><span class="sxs-lookup"><span data-stu-id="7bc9b-116">None</span></span>

## <span data-ttu-id="7bc9b-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bc9b-117">OUTPUTS</span></span>

### <span data-ttu-id="7bc9b-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span><span class="sxs-lookup"><span data-stu-id="7bc9b-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span></span>

### <span data-ttu-id="7bc9b-119">System.Object</span><span class="sxs-lookup"><span data-stu-id="7bc9b-119">System.Object</span></span>
## <span data-ttu-id="7bc9b-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7bc9b-120">NOTES</span></span>

## <span data-ttu-id="7bc9b-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bc9b-121">RELATED LINKS</span></span>

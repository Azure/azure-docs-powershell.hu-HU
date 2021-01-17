---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
ms.openlocfilehash: b9b9771cb5e06b4560dc436b738425288c0ad202
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322808"
---
# <span data-ttu-id="593c2-101">Get-AzHpcCacheSku</span><span class="sxs-lookup"><span data-stu-id="593c2-101">Get-AzHpcCacheSku</span></span>

## <span data-ttu-id="593c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="593c2-102">SYNOPSIS</span></span>
<span data-ttu-id="593c2-103">Az előfizetésben elérhető összes SKUs elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="593c2-103">Gets all SKUs available in subscription.</span></span>

## <span data-ttu-id="593c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="593c2-104">SYNTAX</span></span>

```
Get-AzHpcCacheSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="593c2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="593c2-105">DESCRIPTION</span></span>
<span data-ttu-id="593c2-106">A **Get-AzHpcCacheSku** parancsmag az előfizetésben elérhető termékváltozatok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="593c2-106">The **Get-AzHpcCacheSku** cmdlet returns a list of SKUs available in subscription.</span></span>

## <span data-ttu-id="593c2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="593c2-107">EXAMPLES</span></span>

### <span data-ttu-id="593c2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="593c2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheSku
```

## <span data-ttu-id="593c2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="593c2-109">PARAMETERS</span></span>

### <span data-ttu-id="593c2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="593c2-110">-DefaultProfile</span></span>
<span data-ttu-id="593c2-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="593c2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="593c2-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="593c2-112">CommonParameters</span></span>
<span data-ttu-id="593c2-113">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="593c2-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="593c2-114">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="593c2-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="593c2-115">INPUTS</span><span class="sxs-lookup"><span data-stu-id="593c2-115">INPUTS</span></span>

### <span data-ttu-id="593c2-116">Nincs</span><span class="sxs-lookup"><span data-stu-id="593c2-116">None</span></span>

## <span data-ttu-id="593c2-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="593c2-117">OUTPUTS</span></span>

### <span data-ttu-id="593c2-118">Microsoft.Azure.Commands.HPCCache.PSSku</span><span class="sxs-lookup"><span data-stu-id="593c2-118">Microsoft.Azure.Commands.HPCCache.PSSku</span></span>

## <span data-ttu-id="593c2-119">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="593c2-119">NOTES</span></span>

## <span data-ttu-id="593c2-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="593c2-120">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
ms.openlocfilehash: b9b9771cb5e06b4560dc436b738425288c0ad202
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467710"
---
# <span data-ttu-id="d345c-101">Get-AzHpcCacheSku</span><span class="sxs-lookup"><span data-stu-id="d345c-101">Get-AzHpcCacheSku</span></span>

## <span data-ttu-id="d345c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d345c-102">SYNOPSIS</span></span>
<span data-ttu-id="d345c-103">Az előfizetésben elérhető összes SKUs elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="d345c-103">Gets all SKUs available in subscription.</span></span>

## <span data-ttu-id="d345c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d345c-104">SYNTAX</span></span>

```
Get-AzHpcCacheSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d345c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d345c-105">DESCRIPTION</span></span>
<span data-ttu-id="d345c-106">A **Get-AzHpcCacheSku** parancsmag az előfizetésben elérhető termékváltozatok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d345c-106">The **Get-AzHpcCacheSku** cmdlet returns a list of SKUs available in subscription.</span></span>

## <span data-ttu-id="d345c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d345c-107">EXAMPLES</span></span>

### <span data-ttu-id="d345c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d345c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheSku
```

## <span data-ttu-id="d345c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d345c-109">PARAMETERS</span></span>

### <span data-ttu-id="d345c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d345c-110">-DefaultProfile</span></span>
<span data-ttu-id="d345c-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d345c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d345c-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d345c-112">CommonParameters</span></span>
<span data-ttu-id="d345c-113">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d345c-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d345c-114">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d345c-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d345c-115">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d345c-115">INPUTS</span></span>

### <span data-ttu-id="d345c-116">Nincs</span><span class="sxs-lookup"><span data-stu-id="d345c-116">None</span></span>

## <span data-ttu-id="d345c-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d345c-117">OUTPUTS</span></span>

### <span data-ttu-id="d345c-118">Microsoft.Azure.Commands.HPCCache.PSSku</span><span class="sxs-lookup"><span data-stu-id="d345c-118">Microsoft.Azure.Commands.HPCCache.PSSku</span></span>

## <span data-ttu-id="d345c-119">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d345c-119">NOTES</span></span>

## <span data-ttu-id="d345c-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d345c-120">RELATED LINKS</span></span>

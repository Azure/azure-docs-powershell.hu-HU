---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
ms.openlocfilehash: b9b9771cb5e06b4560dc436b738425288c0ad202
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155570"
---
# <span data-ttu-id="fae2e-101">Get-AzHpcCacheSku</span><span class="sxs-lookup"><span data-stu-id="fae2e-101">Get-AzHpcCacheSku</span></span>

## <span data-ttu-id="fae2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fae2e-102">SYNOPSIS</span></span>
<span data-ttu-id="fae2e-103">Az előfizetésben elérhető összes SKUs elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="fae2e-103">Gets all SKUs available in subscription.</span></span>

## <span data-ttu-id="fae2e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fae2e-104">SYNTAX</span></span>

```
Get-AzHpcCacheSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fae2e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fae2e-105">DESCRIPTION</span></span>
<span data-ttu-id="fae2e-106">A **Get-AzHpcCacheSku** parancsmag az előfizetésben elérhető termékváltozatok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="fae2e-106">The **Get-AzHpcCacheSku** cmdlet returns a list of SKUs available in subscription.</span></span>

## <span data-ttu-id="fae2e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fae2e-107">EXAMPLES</span></span>

### <span data-ttu-id="fae2e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fae2e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheSku
```

## <span data-ttu-id="fae2e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fae2e-109">PARAMETERS</span></span>

### <span data-ttu-id="fae2e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae2e-110">-DefaultProfile</span></span>
<span data-ttu-id="fae2e-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fae2e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fae2e-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae2e-112">CommonParameters</span></span>
<span data-ttu-id="fae2e-113">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae2e-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae2e-114">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fae2e-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae2e-115">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fae2e-115">INPUTS</span></span>

### <span data-ttu-id="fae2e-116">Nincs</span><span class="sxs-lookup"><span data-stu-id="fae2e-116">None</span></span>

## <span data-ttu-id="fae2e-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fae2e-117">OUTPUTS</span></span>

### <span data-ttu-id="fae2e-118">Microsoft.Azure.Commands.HPCCache.PSSku</span><span class="sxs-lookup"><span data-stu-id="fae2e-118">Microsoft.Azure.Commands.HPCCache.PSSku</span></span>

## <span data-ttu-id="fae2e-119">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fae2e-119">NOTES</span></span>

## <span data-ttu-id="fae2e-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fae2e-120">RELATED LINKS</span></span>

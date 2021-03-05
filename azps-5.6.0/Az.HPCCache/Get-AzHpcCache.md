---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: c88e7d2b930eb7d04760f963a5ab8ea60ab8d455
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012101"
---
# <span data-ttu-id="db838-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="db838-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="db838-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db838-102">SYNOPSIS</span></span>
<span data-ttu-id="db838-103">Gyorsítótár(ak)t kap.</span><span class="sxs-lookup"><span data-stu-id="db838-103">Gets a cache(s).</span></span>

## <span data-ttu-id="db838-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db838-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db838-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db838-105">DESCRIPTION</span></span>
<span data-ttu-id="db838-106">A **Get-AzHpcCache** parancsmag egyetlen gyorsítótárat, gyorsítótár(ak)t kap egy adott erőforráscsoportban, vagy előfizetéses szintű gyorsítótárlistát kap.</span><span class="sxs-lookup"><span data-stu-id="db838-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="db838-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db838-107">EXAMPLES</span></span>

### <span data-ttu-id="db838-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="db838-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="db838-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="db838-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="db838-110">3. példa</span><span class="sxs-lookup"><span data-stu-id="db838-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="db838-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db838-111">PARAMETERS</span></span>

### <span data-ttu-id="db838-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db838-112">-DefaultProfile</span></span>
<span data-ttu-id="db838-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db838-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db838-114">-Name</span><span class="sxs-lookup"><span data-stu-id="db838-114">-Name</span></span>
<span data-ttu-id="db838-115">Adott gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="db838-115">Name of specific cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db838-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db838-116">-ResourceGroupName</span></span>
<span data-ttu-id="db838-117">Annak az erőforráscsoportnak a neve, amely alatt fel szeretné sorolni a gyorsítótár(ak)t.</span><span class="sxs-lookup"><span data-stu-id="db838-117">Name of resource group under which you want to list cache(s).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db838-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db838-118">CommonParameters</span></span>
<span data-ttu-id="db838-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db838-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db838-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db838-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db838-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db838-121">INPUTS</span></span>

### <span data-ttu-id="db838-122">System.String</span><span class="sxs-lookup"><span data-stu-id="db838-122">System.String</span></span>

## <span data-ttu-id="db838-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db838-123">OUTPUTS</span></span>

### <span data-ttu-id="db838-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="db838-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="db838-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db838-125">NOTES</span></span>

## <span data-ttu-id="db838-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db838-126">RELATED LINKS</span></span>

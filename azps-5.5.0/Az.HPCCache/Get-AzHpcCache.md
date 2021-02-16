---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153066"
---
# <span data-ttu-id="13bf6-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="13bf6-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="13bf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="13bf6-103">Gyorsítótár(ak)t kap.</span><span class="sxs-lookup"><span data-stu-id="13bf6-103">Gets a cache(s).</span></span>

## <span data-ttu-id="13bf6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13bf6-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13bf6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13bf6-105">DESCRIPTION</span></span>
<span data-ttu-id="13bf6-106">A **Get-AzHpcCache** parancsmag egyetlen gyorsítótárat, egy adott erőforráscsoport gyorsítótárát vagy előfizetési szintű gyorsítótárlistát kap.</span><span class="sxs-lookup"><span data-stu-id="13bf6-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="13bf6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13bf6-107">EXAMPLES</span></span>

### <span data-ttu-id="13bf6-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="13bf6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="13bf6-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="13bf6-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="13bf6-110">3. példa</span><span class="sxs-lookup"><span data-stu-id="13bf6-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="13bf6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13bf6-111">PARAMETERS</span></span>

### <span data-ttu-id="13bf6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13bf6-112">-DefaultProfile</span></span>
<span data-ttu-id="13bf6-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13bf6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13bf6-114">-Name</span><span class="sxs-lookup"><span data-stu-id="13bf6-114">-Name</span></span>
<span data-ttu-id="13bf6-115">Adott gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="13bf6-115">Name of specific cache.</span></span>

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

### <span data-ttu-id="13bf6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13bf6-116">-ResourceGroupName</span></span>
<span data-ttu-id="13bf6-117">Annak az erőforráscsoportnak a neve, amely alatt fel szeretné sorolni a gyorsítótár(ak)t.</span><span class="sxs-lookup"><span data-stu-id="13bf6-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="13bf6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13bf6-118">CommonParameters</span></span>
<span data-ttu-id="13bf6-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13bf6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13bf6-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13bf6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13bf6-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13bf6-121">INPUTS</span></span>

### <span data-ttu-id="13bf6-122">System.String</span><span class="sxs-lookup"><span data-stu-id="13bf6-122">System.String</span></span>

## <span data-ttu-id="13bf6-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13bf6-123">OUTPUTS</span></span>

### <span data-ttu-id="13bf6-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="13bf6-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="13bf6-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13bf6-125">NOTES</span></span>

## <span data-ttu-id="13bf6-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13bf6-126">RELATED LINKS</span></span>

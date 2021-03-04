---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 1d5f230070f8b8c269137e07b04af970f314d564
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936618"
---
# <span data-ttu-id="17346-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="17346-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="17346-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17346-102">SYNOPSIS</span></span>
<span data-ttu-id="17346-103">Lekérte a redis-gyorsítótár hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="17346-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="17346-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="17346-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17346-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="17346-105">DESCRIPTION</span></span>
<span data-ttu-id="17346-106">A **Get-AzRedisCacheKey** parancsmag az Azure Redis Cache hozzáférési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="17346-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="17346-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="17346-107">EXAMPLES</span></span>

### <span data-ttu-id="17346-108">1. példa: A redis-gyorsítótár hozzáférési kulcsának lekérte</span><span class="sxs-lookup"><span data-stu-id="17346-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="17346-109">Ez a parancs a MyCacheKey nevű hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="17346-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="17346-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17346-110">PARAMETERS</span></span>

### <span data-ttu-id="17346-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17346-111">-DefaultProfile</span></span>
<span data-ttu-id="17346-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17346-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17346-113">-Name</span><span class="sxs-lookup"><span data-stu-id="17346-113">-Name</span></span>
<span data-ttu-id="17346-114">A redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="17346-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="17346-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17346-115">-ResourceGroupName</span></span>
<span data-ttu-id="17346-116">A redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="17346-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="17346-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17346-117">CommonParameters</span></span>
<span data-ttu-id="17346-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17346-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17346-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17346-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17346-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17346-120">INPUTS</span></span>

### <span data-ttu-id="17346-121">System.String</span><span class="sxs-lookup"><span data-stu-id="17346-121">System.String</span></span>

## <span data-ttu-id="17346-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17346-122">OUTPUTS</span></span>

### <span data-ttu-id="17346-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="17346-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="17346-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="17346-124">NOTES</span></span>

## <span data-ttu-id="17346-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17346-125">RELATED LINKS</span></span>

[<span data-ttu-id="17346-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="17346-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)



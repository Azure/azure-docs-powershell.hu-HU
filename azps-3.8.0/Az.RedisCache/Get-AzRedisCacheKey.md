---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013569"
---
# <span data-ttu-id="44406-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="44406-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="44406-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44406-102">SYNOPSIS</span></span>
<span data-ttu-id="44406-103">A Redis-gyorsítótár elérési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44406-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="44406-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44406-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44406-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="44406-105">DESCRIPTION</span></span>
<span data-ttu-id="44406-106">A **Get-AzRedisCacheKey** parancsmag egy Azure Redis-gyorsítótár elérési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44406-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="44406-107">Példák</span><span class="sxs-lookup"><span data-stu-id="44406-107">EXAMPLES</span></span>

### <span data-ttu-id="44406-108">Példa 1: a Redis-gyorsítótár elérési kulcsainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="44406-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="44406-109">Ez a parancs a MyCacheKey nevű elérési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44406-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="44406-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44406-110">PARAMETERS</span></span>

### <span data-ttu-id="44406-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44406-111">-DefaultProfile</span></span>
<span data-ttu-id="44406-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44406-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44406-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="44406-113">-Name</span></span>
<span data-ttu-id="44406-114">A Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44406-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="44406-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44406-115">-ResourceGroupName</span></span>
<span data-ttu-id="44406-116">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44406-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="44406-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44406-117">CommonParameters</span></span>
<span data-ttu-id="44406-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44406-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44406-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44406-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44406-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44406-120">INPUTS</span></span>

### <span data-ttu-id="44406-121">System. String</span><span class="sxs-lookup"><span data-stu-id="44406-121">System.String</span></span>

## <span data-ttu-id="44406-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44406-122">OUTPUTS</span></span>

### <span data-ttu-id="44406-123">Microsoft. Azure. Management. Redis. models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="44406-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="44406-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44406-124">NOTES</span></span>

## <span data-ttu-id="44406-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44406-125">RELATED LINKS</span></span>

[<span data-ttu-id="44406-126">Új – AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="44406-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)



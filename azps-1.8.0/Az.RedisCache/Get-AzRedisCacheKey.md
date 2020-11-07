---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 96eed93e4020384b0c989a05f549aa21f5482493
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669559"
---
# <span data-ttu-id="9ab90-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="9ab90-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="9ab90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ab90-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab90-103">A Redis-gyorsítótár elérési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9ab90-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="9ab90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ab90-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ab90-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ab90-105">DESCRIPTION</span></span>
<span data-ttu-id="9ab90-106">A **Get-AzRedisCacheKey** parancsmag egy Azure Redis-gyorsítótár elérési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9ab90-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="9ab90-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9ab90-107">EXAMPLES</span></span>

### <span data-ttu-id="9ab90-108">Példa 1: a Redis-gyorsítótár elérési kulcsainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="9ab90-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="9ab90-109">Ez a parancs a MyCacheKey nevű elérési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9ab90-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="9ab90-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ab90-110">PARAMETERS</span></span>

### <span data-ttu-id="9ab90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab90-111">-DefaultProfile</span></span>
<span data-ttu-id="9ab90-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ab90-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ab90-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ab90-113">-Name</span></span>
<span data-ttu-id="9ab90-114">A Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ab90-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="9ab90-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab90-115">-ResourceGroupName</span></span>
<span data-ttu-id="9ab90-116">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ab90-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="9ab90-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab90-117">CommonParameters</span></span>
<span data-ttu-id="9ab90-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ab90-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab90-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ab90-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab90-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ab90-120">INPUTS</span></span>

### <span data-ttu-id="9ab90-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9ab90-121">System.String</span></span>

## <span data-ttu-id="9ab90-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ab90-122">OUTPUTS</span></span>

### <span data-ttu-id="9ab90-123">Microsoft. Azure. Management. Redis. models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="9ab90-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="9ab90-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ab90-124">NOTES</span></span>

## <span data-ttu-id="9ab90-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ab90-125">RELATED LINKS</span></span>

[<span data-ttu-id="9ab90-126">Új – AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="9ab90-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)



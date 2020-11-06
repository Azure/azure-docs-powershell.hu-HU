---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: 297d02fcb77c8fc537831b2b1995bfe43ca90e73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495743"
---
# <span data-ttu-id="bf2c7-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="bf2c7-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="bf2c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="bf2c7-103">A Redis-gyorsítótár elérési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bf2c7-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf2c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf2c7-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf2c7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf2c7-105">DESCRIPTION</span></span>
<span data-ttu-id="bf2c7-106">A **Get-AzureRmRedisCacheKey** parancsmag egy Azure Redis-gyorsítótár elérési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bf2c7-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="bf2c7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf2c7-107">EXAMPLES</span></span>

### <span data-ttu-id="bf2c7-108">Példa 1: a Redis-gyorsítótár elérési kulcsainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="bf2c7-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="bf2c7-109">Ez a parancs a MyCacheKey nevű elérési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bf2c7-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="bf2c7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf2c7-110">PARAMETERS</span></span>

### <span data-ttu-id="bf2c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf2c7-111">-DefaultProfile</span></span>
<span data-ttu-id="bf2c7-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf2c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf2c7-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf2c7-113">-Name</span></span>
<span data-ttu-id="bf2c7-114">A Redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf2c7-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="bf2c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf2c7-115">-ResourceGroupName</span></span>
<span data-ttu-id="bf2c7-116">A Redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf2c7-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="bf2c7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf2c7-117">CommonParameters</span></span>
<span data-ttu-id="bf2c7-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf2c7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf2c7-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf2c7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf2c7-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf2c7-120">INPUTS</span></span>

### <span data-ttu-id="bf2c7-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bf2c7-121">System.String</span></span>

## <span data-ttu-id="bf2c7-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf2c7-122">OUTPUTS</span></span>

### <span data-ttu-id="bf2c7-123">Microsoft. Azure. Management. Redis. models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="bf2c7-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="bf2c7-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf2c7-124">NOTES</span></span>

## <span data-ttu-id="bf2c7-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf2c7-125">RELATED LINKS</span></span>

[<span data-ttu-id="bf2c7-126">Új – AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="bf2c7-126">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)



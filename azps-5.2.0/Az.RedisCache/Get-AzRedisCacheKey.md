---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348053"
---
# <span data-ttu-id="8f2d9-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="8f2d9-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="8f2d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f2d9-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2d9-103">Lekérte a redis-gyorsítótár hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="8f2d9-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="8f2d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f2d9-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f2d9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f2d9-105">DESCRIPTION</span></span>
<span data-ttu-id="8f2d9-106">A **Get-AzRedisCacheKey** parancsmag az Azure Redis Cache hozzáférési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8f2d9-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="8f2d9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f2d9-107">EXAMPLES</span></span>

### <span data-ttu-id="8f2d9-108">1. példa: A redis-gyorsítótár hozzáférési kulcsának lekérte</span><span class="sxs-lookup"><span data-stu-id="8f2d9-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="8f2d9-109">Ez a parancs a MyCacheKey nevű hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8f2d9-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="8f2d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f2d9-110">PARAMETERS</span></span>

### <span data-ttu-id="8f2d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2d9-111">-DefaultProfile</span></span>
<span data-ttu-id="8f2d9-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f2d9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f2d9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8f2d9-113">-Name</span></span>
<span data-ttu-id="8f2d9-114">A redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f2d9-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="8f2d9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2d9-115">-ResourceGroupName</span></span>
<span data-ttu-id="8f2d9-116">A redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f2d9-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="8f2d9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2d9-117">CommonParameters</span></span>
<span data-ttu-id="8f2d9-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2d9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2d9-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f2d9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2d9-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f2d9-120">INPUTS</span></span>

### <span data-ttu-id="8f2d9-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8f2d9-121">System.String</span></span>

## <span data-ttu-id="8f2d9-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f2d9-122">OUTPUTS</span></span>

### <span data-ttu-id="8f2d9-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="8f2d9-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="8f2d9-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f2d9-124">NOTES</span></span>

## <span data-ttu-id="8f2d9-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f2d9-125">RELATED LINKS</span></span>

[<span data-ttu-id="8f2d9-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="8f2d9-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)



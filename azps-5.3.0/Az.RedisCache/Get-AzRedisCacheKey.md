---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378263"
---
# <span data-ttu-id="7ab26-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="7ab26-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="7ab26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ab26-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab26-103">Lekérte a redis-gyorsítótár hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="7ab26-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="7ab26-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ab26-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ab26-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ab26-105">DESCRIPTION</span></span>
<span data-ttu-id="7ab26-106">A **Get-AzRedisCacheKey** parancsmag az Azure Redis Cache hozzáférési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab26-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="7ab26-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ab26-107">EXAMPLES</span></span>

### <span data-ttu-id="7ab26-108">1. példa: A redis-gyorsítótár hozzáférési kulcsának lekérte</span><span class="sxs-lookup"><span data-stu-id="7ab26-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="7ab26-109">Ez a parancs a MyCacheKey nevű hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab26-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="7ab26-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ab26-110">PARAMETERS</span></span>

### <span data-ttu-id="7ab26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab26-111">-DefaultProfile</span></span>
<span data-ttu-id="7ab26-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ab26-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ab26-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7ab26-113">-Name</span></span>
<span data-ttu-id="7ab26-114">A redis-gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab26-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="7ab26-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab26-115">-ResourceGroupName</span></span>
<span data-ttu-id="7ab26-116">A redis-gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab26-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="7ab26-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab26-117">CommonParameters</span></span>
<span data-ttu-id="7ab26-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab26-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab26-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab26-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab26-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ab26-120">INPUTS</span></span>

### <span data-ttu-id="7ab26-121">System.String</span><span class="sxs-lookup"><span data-stu-id="7ab26-121">System.String</span></span>

## <span data-ttu-id="7ab26-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ab26-122">OUTPUTS</span></span>

### <span data-ttu-id="7ab26-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="7ab26-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="7ab26-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ab26-124">NOTES</span></span>

## <span data-ttu-id="7ab26-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ab26-125">RELATED LINKS</span></span>

[<span data-ttu-id="7ab26-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="7ab26-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)



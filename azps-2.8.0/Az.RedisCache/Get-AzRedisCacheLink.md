---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 8129634e940624fe09dad4a1199f96dbcf5162bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838519"
---
# <span data-ttu-id="5efaa-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5efaa-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="5efaa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5efaa-102">SYNOPSIS</span></span>
<span data-ttu-id="5efaa-103">Térinformatikai replikációs hivatkozás beszerzése Redis-gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="5efaa-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="5efaa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5efaa-104">SYNTAX</span></span>

### <span data-ttu-id="5efaa-105">AllLinksForCache (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5efaa-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5efaa-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="5efaa-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5efaa-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="5efaa-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5efaa-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="5efaa-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5efaa-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5efaa-109">DESCRIPTION</span></span>
<span data-ttu-id="5efaa-110">Négy különböző módon juthat hozzá a Geo-replikációs hivatkozás részleteihez.</span><span class="sxs-lookup"><span data-stu-id="5efaa-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="5efaa-111">Adjon meg paraméteres nevet vagy PrimaryServerName, illetve SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="5efaa-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="5efaa-112">A név akkor jelenik meg, ha az összes olyan hivatkozás van megadva, ahová a gyorsítótár létezik.</span><span class="sxs-lookup"><span data-stu-id="5efaa-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="5efaa-113">Ha csak az PrimaryServerName-ot adja meg, akkor minden olyan hivatkozás, ahol a gyorsítótár elsődlegesen vissza fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="5efaa-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="5efaa-114">Ha csak a SecondaryServerName-t adja meg, akkor az összes olyan hivatkozás, ahol a gyorsítótár a másodlagos, vissza lesz adva.</span><span class="sxs-lookup"><span data-stu-id="5efaa-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="5efaa-115">Ha a PrimaryServerName és a SecondaryServerName egyaránt meg van adva, akkor a megfelelő szerepkört visszaadó hivatkozás jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="5efaa-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="5efaa-116">Példák</span><span class="sxs-lookup"><span data-stu-id="5efaa-116">EXAMPLES</span></span>

### <span data-ttu-id="5efaa-117">Példa 1: a paraméteres set AllLinksForCache beszerzése</span><span class="sxs-lookup"><span data-stu-id="5efaa-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="5efaa-118">Ez a parancs a mycache1 nevű Redis-gyorsítótár minden geo-replikációs hivatkozását bekapja.</span><span class="sxs-lookup"><span data-stu-id="5efaa-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="5efaa-119">2. példa: a paraméteres set AllLinksForPrimaryCache beszerzése</span><span class="sxs-lookup"><span data-stu-id="5efaa-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="5efaa-120">Ez a parancs geo-replikációs hivatkozásokat kap, amelyekben az Redis-gyorsítótár mycache1 elsődleges.</span><span class="sxs-lookup"><span data-stu-id="5efaa-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="5efaa-121">3. példa: a paraméteres set AllLinksForSecondaryCache beszerzése</span><span class="sxs-lookup"><span data-stu-id="5efaa-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="5efaa-122">Ez a parancs geo-replikációs hivatkozásokat kap, ahol a Redis-gyorsítótár mycache2 másodlagos.</span><span class="sxs-lookup"><span data-stu-id="5efaa-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="5efaa-123">Példa 4: a paraméteres set SingleLink beszerzése</span><span class="sxs-lookup"><span data-stu-id="5efaa-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="5efaa-124">Ez a parancs egy olyan geo-replikációs hivatkozásokat kap, amelyekben az mycache1 nevű Redis-gyorsítótár az elsődleges, a Redis gyorsítótára pedig másodlagos.</span><span class="sxs-lookup"><span data-stu-id="5efaa-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="5efaa-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5efaa-125">PARAMETERS</span></span>

### <span data-ttu-id="5efaa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5efaa-126">-DefaultProfile</span></span>
<span data-ttu-id="5efaa-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5efaa-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5efaa-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5efaa-128">-Name</span></span>
<span data-ttu-id="5efaa-129">A Redis-gyorsítótár neve</span><span class="sxs-lookup"><span data-stu-id="5efaa-129">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5efaa-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="5efaa-130">-PrimaryServerName</span></span>
<span data-ttu-id="5efaa-131">Az elsődleges Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="5efaa-131">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5efaa-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="5efaa-132">-SecondaryServerName</span></span>
<span data-ttu-id="5efaa-133">A másodlagos Redis-gyorsítótár neve hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="5efaa-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5efaa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5efaa-134">CommonParameters</span></span>
<span data-ttu-id="5efaa-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5efaa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5efaa-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5efaa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5efaa-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5efaa-137">INPUTS</span></span>

### <span data-ttu-id="5efaa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5efaa-138">System.String</span></span>

## <span data-ttu-id="5efaa-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5efaa-139">OUTPUTS</span></span>

### <span data-ttu-id="5efaa-140">Microsoft. Azure. Command. RedisCache. models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="5efaa-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="5efaa-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5efaa-141">NOTES</span></span>

## <span data-ttu-id="5efaa-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5efaa-142">RELATED LINKS</span></span>

[<span data-ttu-id="5efaa-143">Új – AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5efaa-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="5efaa-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5efaa-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="5efaa-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5efaa-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="5efaa-146">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5efaa-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="5efaa-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5efaa-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5efaa-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5efaa-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)
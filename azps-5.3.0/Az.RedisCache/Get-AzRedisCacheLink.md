---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378250"
---
# <span data-ttu-id="cb0cd-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="cb0cd-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="cb0cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0cd-103">A Redis Cache geo replikációs hivatkozásának le kérése.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="cb0cd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb0cd-104">SYNTAX</span></span>

### <span data-ttu-id="cb0cd-105">AllLinksForCache (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb0cd-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb0cd-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="cb0cd-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb0cd-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="cb0cd-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb0cd-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="cb0cd-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb0cd-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb0cd-109">DESCRIPTION</span></span>
<span data-ttu-id="cb0cd-110">Négy különböző módon lehet lekérte a georeplikáció hivatkozásának részleteit.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="cb0cd-111">Adja meg a name vagy PrimaryServerName és/vagy SecondaryServerName paramétert.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="cb0cd-112">A rendszer ekkor visszaadja a gyorsítótárat tároló összes hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="cb0cd-113">Ha csak PrimaryServerName van megadva, akkor az összes olyan hivatkozást visszaadja a rendszer, ahol a gyorsítótár az elsődleges.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="cb0cd-114">Ha csak SecondaryServerName van megadva, akkor az összes olyan hivatkozást visszaadja a rendszer, ahol a gyorsítótár másodlagos.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="cb0cd-115">Ha a PrimaryServerName és a SecondaryServerName is meg van adva, akkor a helyes szerepkörű konkrét hivatkozást ad vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="cb0cd-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb0cd-116">EXAMPLES</span></span>

### <span data-ttu-id="cb0cd-117">1. példa: Az AllLinksForCache paraméterkészlet használata</span><span class="sxs-lookup"><span data-stu-id="cb0cd-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="cb0cd-118">Ez a parancs a mycache1 nevű Redis cache összes georeplikációs hivatkozását lekérte.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="cb0cd-119">2. példa: Az AllLinksForPrimaryCache paraméterkészlet használata</span><span class="sxs-lookup"><span data-stu-id="cb0cd-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="cb0cd-120">Ez a parancs földrajzi replikációs hivatkozásokat kap, ahol a Mycache1 nevű redis gyorsítótár elsődleges hely.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="cb0cd-121">3. példa: Az AllLinksForSecondaryCache paraméterkészlet használata</span><span class="sxs-lookup"><span data-stu-id="cb0cd-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="cb0cd-122">Ez a parancs georeplikációs hivatkozásokat kap, ahol a Mycache2 nevű Redis cache másodlagos.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="cb0cd-123">4. példa: Paraméterkészlet használata SingleLink</span><span class="sxs-lookup"><span data-stu-id="cb0cd-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="cb0cd-124">Ez a parancs egyetlen georeplikációs kapcsolatot kap, ahol a mycache1 nevű Redis Cache elsődleges, a Redis Cache pedig másodlagos.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="cb0cd-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb0cd-125">PARAMETERS</span></span>

### <span data-ttu-id="cb0cd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0cd-126">-DefaultProfile</span></span>
<span data-ttu-id="cb0cd-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb0cd-128">-Name</span><span class="sxs-lookup"><span data-stu-id="cb0cd-128">-Name</span></span>
<span data-ttu-id="cb0cd-129">A redis cache neve.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="cb0cd-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="cb0cd-130">-PrimaryServerName</span></span>
<span data-ttu-id="cb0cd-131">A csatolásban lévő elsődleges redis cache neve.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="cb0cd-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="cb0cd-132">-SecondaryServerName</span></span>
<span data-ttu-id="cb0cd-133">A másodlagos redis-gyorsítótár neve a csatolásban.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="cb0cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0cd-134">CommonParameters</span></span>
<span data-ttu-id="cb0cd-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb0cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0cd-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb0cd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0cd-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb0cd-137">INPUTS</span></span>

### <span data-ttu-id="cb0cd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cb0cd-138">System.String</span></span>

## <span data-ttu-id="cb0cd-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb0cd-139">OUTPUTS</span></span>

### <span data-ttu-id="cb0cd-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="cb0cd-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="cb0cd-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb0cd-141">NOTES</span></span>

## <span data-ttu-id="cb0cd-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb0cd-142">RELATED LINKS</span></span>

[<span data-ttu-id="cb0cd-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="cb0cd-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="cb0cd-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="cb0cd-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="cb0cd-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cb0cd-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="cb0cd-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cb0cd-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="cb0cd-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cb0cd-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="cb0cd-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cb0cd-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)
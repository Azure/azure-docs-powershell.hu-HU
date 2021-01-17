---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: 8416c18ac945eaab5ae9dbd758d2660c4f950417
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378236"
---
# <span data-ttu-id="586b9-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="586b9-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="586b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="586b9-102">SYNOPSIS</span></span>
<span data-ttu-id="586b9-103">A művelet állapotának lekérte.</span><span class="sxs-lookup"><span data-stu-id="586b9-103">Gets the status of operation.</span></span>

## <span data-ttu-id="586b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="586b9-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="586b9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="586b9-105">DESCRIPTION</span></span>
<span data-ttu-id="586b9-106">A művelet állapotának lekérte.</span><span class="sxs-lookup"><span data-stu-id="586b9-106">Gets the status of operation.</span></span>

## <span data-ttu-id="586b9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="586b9-107">EXAMPLES</span></span>

### <span data-ttu-id="586b9-108">1. példa: A művelet állapotának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="586b9-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="586b9-109">Ez a parancs egy művelet állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="586b9-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="586b9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="586b9-110">PARAMETERS</span></span>

### <span data-ttu-id="586b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="586b9-111">-DefaultProfile</span></span>
<span data-ttu-id="586b9-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="586b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="586b9-113">-Location</span><span class="sxs-lookup"><span data-stu-id="586b9-113">-Location</span></span>
<span data-ttu-id="586b9-114">A művelet régiójában.</span><span class="sxs-lookup"><span data-stu-id="586b9-114">The region the operation is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="586b9-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="586b9-115">-OperationId</span></span>
<span data-ttu-id="586b9-116">A művelet egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="586b9-116">The operation's unique identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="586b9-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="586b9-117">-SubscriptionId</span></span>
<span data-ttu-id="586b9-118">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="586b9-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="586b9-119">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="586b9-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="586b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="586b9-120">CommonParameters</span></span>
<span data-ttu-id="586b9-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="586b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="586b9-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="586b9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="586b9-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="586b9-123">INPUTS</span></span>

## <span data-ttu-id="586b9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="586b9-124">OUTPUTS</span></span>

### <span data-ttu-id="586b9-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="586b9-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="586b9-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="586b9-126">NOTES</span></span>

<span data-ttu-id="586b9-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="586b9-127">ALIASES</span></span>

## <span data-ttu-id="586b9-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="586b9-128">RELATED LINKS</span></span>


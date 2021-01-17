---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466617"
---
# <span data-ttu-id="50e03-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="50e03-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="50e03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50e03-102">SYNOPSIS</span></span>
<span data-ttu-id="50e03-103">Letiltja a diagnosztika az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="50e03-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="50e03-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="50e03-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50e03-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="50e03-105">DESCRIPTION</span></span>
<span data-ttu-id="50e03-106">A **Remove-AzRedisCacheDiagnostic** parancsmag letiltja a diagnosztika az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="50e03-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="50e03-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="50e03-107">EXAMPLES</span></span>

### <span data-ttu-id="50e03-108">1. példa: A diagnosztika letiltása</span><span class="sxs-lookup"><span data-stu-id="50e03-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="50e03-109">Ez a parancs letiltja a diagnosztikát a megadott Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="50e03-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="50e03-110">Ez letiltja az összes Azure Redis-gyorsítótár diagnosztikát az előfizetéshez ugyanabban a régióban.</span><span class="sxs-lookup"><span data-stu-id="50e03-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="50e03-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50e03-111">PARAMETERS</span></span>

### <span data-ttu-id="50e03-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e03-112">-DefaultProfile</span></span>
<span data-ttu-id="50e03-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50e03-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50e03-114">-Name</span><span class="sxs-lookup"><span data-stu-id="50e03-114">-Name</span></span>
<span data-ttu-id="50e03-115">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50e03-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="50e03-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50e03-116">-ResourceGroupName</span></span>
<span data-ttu-id="50e03-117">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50e03-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="50e03-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50e03-118">-Confirm</span></span>
<span data-ttu-id="50e03-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="50e03-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50e03-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50e03-120">-WhatIf</span></span>
<span data-ttu-id="50e03-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="50e03-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50e03-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50e03-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50e03-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e03-123">CommonParameters</span></span>
<span data-ttu-id="50e03-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50e03-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e03-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50e03-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e03-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50e03-126">INPUTS</span></span>

### <span data-ttu-id="50e03-127">System.String</span><span class="sxs-lookup"><span data-stu-id="50e03-127">System.String</span></span>

## <span data-ttu-id="50e03-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50e03-128">OUTPUTS</span></span>

### <span data-ttu-id="50e03-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="50e03-129">System.Void</span></span>

## <span data-ttu-id="50e03-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="50e03-130">NOTES</span></span>
* <span data-ttu-id="50e03-131">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, redis, cache, web, webapp, webhely</span><span class="sxs-lookup"><span data-stu-id="50e03-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="50e03-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50e03-132">RELATED LINKS</span></span>

[<span data-ttu-id="50e03-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="50e03-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)



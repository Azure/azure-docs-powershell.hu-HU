---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337757"
---
# <span data-ttu-id="d8969-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d8969-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="d8969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8969-102">SYNOPSIS</span></span>
<span data-ttu-id="d8969-103">Letiltja a diagnosztika az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="d8969-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="d8969-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8969-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8969-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8969-105">DESCRIPTION</span></span>
<span data-ttu-id="d8969-106">A **Remove-AzRedisCacheDiagnostic** parancsmag letiltja a diagnosztika az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="d8969-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="d8969-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8969-107">EXAMPLES</span></span>

### <span data-ttu-id="d8969-108">1. példa: A diagnosztika letiltása</span><span class="sxs-lookup"><span data-stu-id="d8969-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="d8969-109">Ez a parancs letiltja a diagnosztikát a megadott Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="d8969-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="d8969-110">Ez letiltja az összes Azure Redis-gyorsítótár diagnosztikát az előfizetéshez ugyanabban a régióban.</span><span class="sxs-lookup"><span data-stu-id="d8969-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="d8969-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8969-111">PARAMETERS</span></span>

### <span data-ttu-id="d8969-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8969-112">-DefaultProfile</span></span>
<span data-ttu-id="d8969-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8969-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8969-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d8969-114">-Name</span></span>
<span data-ttu-id="d8969-115">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8969-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="d8969-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8969-116">-ResourceGroupName</span></span>
<span data-ttu-id="d8969-117">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8969-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="d8969-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8969-118">-Confirm</span></span>
<span data-ttu-id="d8969-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8969-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8969-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8969-120">-WhatIf</span></span>
<span data-ttu-id="d8969-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8969-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8969-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8969-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8969-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8969-123">CommonParameters</span></span>
<span data-ttu-id="d8969-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8969-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8969-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8969-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8969-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8969-126">INPUTS</span></span>

### <span data-ttu-id="d8969-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d8969-127">System.String</span></span>

## <span data-ttu-id="d8969-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8969-128">OUTPUTS</span></span>

### <span data-ttu-id="d8969-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="d8969-129">System.Void</span></span>

## <span data-ttu-id="d8969-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8969-130">NOTES</span></span>
* <span data-ttu-id="d8969-131">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, redis, cache, web, webapp, webhely</span><span class="sxs-lookup"><span data-stu-id="d8969-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d8969-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8969-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8969-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d8969-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)



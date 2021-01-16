---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352481"
---
# <span data-ttu-id="870d6-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="870d6-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="870d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="870d6-102">SYNOPSIS</span></span>
<span data-ttu-id="870d6-103">Engedélyezi a diagnosztika az Azure Redis-gyorsítótárban.</span><span class="sxs-lookup"><span data-stu-id="870d6-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="870d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="870d6-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="870d6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="870d6-105">DESCRIPTION</span></span>
<span data-ttu-id="870d6-106">A **Set-AzRedisCacheDiagnostic** parancsmag diagnosztikai funkciókat tesz lehetővé az Azure Redis-gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="870d6-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="870d6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="870d6-107">EXAMPLES</span></span>

### <span data-ttu-id="870d6-108">1. példa: A diagnosztika engedélyezése</span><span class="sxs-lookup"><span data-stu-id="870d6-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="870d6-109">Ez a parancs diagnosztikai funkciókat tesz lehetővé az Azure Redis gyorsítótárához.</span><span class="sxs-lookup"><span data-stu-id="870d6-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="870d6-110">Ez a parancs engedélyezi a diagnosztikát, vagy frissíti a tárfiókot az előfizetéshez ugyanabban a régióban található Összes Azure Redis-gyorsítótárhoz.</span><span class="sxs-lookup"><span data-stu-id="870d6-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="870d6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="870d6-111">PARAMETERS</span></span>

### <span data-ttu-id="870d6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870d6-112">-DefaultProfile</span></span>
<span data-ttu-id="870d6-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="870d6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="870d6-114">-Name</span><span class="sxs-lookup"><span data-stu-id="870d6-114">-Name</span></span>
<span data-ttu-id="870d6-115">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="870d6-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="870d6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="870d6-116">-ResourceGroupName</span></span>
<span data-ttu-id="870d6-117">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="870d6-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="870d6-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="870d6-118">-StorageAccountId</span></span>
<span data-ttu-id="870d6-119">A diagnosztikai adatok tárolásához használt tárfiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="870d6-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="870d6-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="870d6-120">-Confirm</span></span>
<span data-ttu-id="870d6-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="870d6-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870d6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="870d6-122">-WhatIf</span></span>
<span data-ttu-id="870d6-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="870d6-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="870d6-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="870d6-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870d6-125">CommonParameters</span></span>
<span data-ttu-id="870d6-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="870d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870d6-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="870d6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870d6-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="870d6-128">INPUTS</span></span>

### <span data-ttu-id="870d6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="870d6-129">System.String</span></span>

## <span data-ttu-id="870d6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="870d6-130">OUTPUTS</span></span>

### <span data-ttu-id="870d6-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="870d6-131">System.Void</span></span>

## <span data-ttu-id="870d6-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="870d6-132">NOTES</span></span>
* <span data-ttu-id="870d6-133">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, redis, cache, web, webapp, webhely</span><span class="sxs-lookup"><span data-stu-id="870d6-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="870d6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="870d6-134">RELATED LINKS</span></span>

[<span data-ttu-id="870d6-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="870d6-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)



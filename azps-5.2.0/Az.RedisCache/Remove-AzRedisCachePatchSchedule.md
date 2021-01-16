---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 8e66391ff613578d1306543c626908763a932d06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352518"
---
# <span data-ttu-id="c9492-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="c9492-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="c9492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9492-102">SYNOPSIS</span></span>
<span data-ttu-id="c9492-103">Eltávolítja a javítás ütemezését.</span><span class="sxs-lookup"><span data-stu-id="c9492-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="c9492-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9492-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9492-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9492-105">DESCRIPTION</span></span>
<span data-ttu-id="c9492-106">A **Remove-AzRedisCachePatchSchedule** parancsmag eltávolítja a javítás ütemezését a gyorsítótárból az Azure Redis Cache-ben.</span><span class="sxs-lookup"><span data-stu-id="c9492-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="c9492-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9492-107">EXAMPLES</span></span>

### <span data-ttu-id="c9492-108">1. példa: A javítás ütemezésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c9492-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="c9492-109">Ez a parancs eltávolítja a javítás ütemezését a RedisCache06 nevű gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="c9492-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="c9492-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9492-110">PARAMETERS</span></span>

### <span data-ttu-id="c9492-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9492-111">-DefaultProfile</span></span>
<span data-ttu-id="c9492-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9492-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9492-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c9492-113">-Name</span></span>
<span data-ttu-id="c9492-114">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9492-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="c9492-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9492-115">-PassThru</span></span>
<span data-ttu-id="c9492-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c9492-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9492-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9492-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9492-118">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9492-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="c9492-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9492-119">-Confirm</span></span>
<span data-ttu-id="c9492-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c9492-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9492-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9492-121">-WhatIf</span></span>
<span data-ttu-id="c9492-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c9492-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9492-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9492-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9492-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9492-124">CommonParameters</span></span>
<span data-ttu-id="c9492-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9492-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9492-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9492-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9492-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9492-127">INPUTS</span></span>

### <span data-ttu-id="c9492-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c9492-128">System.String</span></span>

## <span data-ttu-id="c9492-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9492-129">OUTPUTS</span></span>

### <span data-ttu-id="c9492-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c9492-130">System.Boolean</span></span>

## <span data-ttu-id="c9492-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9492-131">NOTES</span></span>
* <span data-ttu-id="c9492-132">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, redis, cache, web, webapp, webhely</span><span class="sxs-lookup"><span data-stu-id="c9492-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="c9492-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9492-133">RELATED LINKS</span></span>

[<span data-ttu-id="c9492-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="c9492-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="c9492-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="c9492-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="c9492-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="c9492-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)



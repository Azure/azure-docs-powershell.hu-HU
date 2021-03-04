---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: ecd5771478f3d3ff3cee4a5045d6c72eb707af11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939402"
---
# <span data-ttu-id="f9fa3-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="f9fa3-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="f9fa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="f9fa3-103">Előfizetés hozzáadása felügyeleti csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="f9fa3-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="f9fa3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9fa3-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9fa3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="f9fa3-106">A **New-AzManagementGroupSubscription** parancsmag hozzáad egy előfizetést egy felügyeleti csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="f9fa3-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="f9fa3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9fa3-107">EXAMPLES</span></span>

### <span data-ttu-id="f9fa3-108">1. példa: Előfizetés hozzáadása felügyeleti csoporthoz</span><span class="sxs-lookup"><span data-stu-id="f9fa3-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="f9fa3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9fa3-109">PARAMETERS</span></span>

### <span data-ttu-id="f9fa3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9fa3-110">-DefaultProfile</span></span>
<span data-ttu-id="f9fa3-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9fa3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9fa3-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="f9fa3-112">-GroupName</span></span>
<span data-ttu-id="f9fa3-113">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="f9fa3-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fa3-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9fa3-114">-PassThru</span></span>
<span data-ttu-id="f9fa3-115">A `true` sikeres végrehajtás visszaküldése</span><span class="sxs-lookup"><span data-stu-id="f9fa3-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="f9fa3-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9fa3-116">-SubscriptionId</span></span>
<span data-ttu-id="f9fa3-117">A kezeléshez társított előfizetés előfizetés-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f9fa3-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fa3-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9fa3-118">-Confirm</span></span>
<span data-ttu-id="f9fa3-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f9fa3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9fa3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9fa3-120">-WhatIf</span></span>
<span data-ttu-id="f9fa3-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f9fa3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9fa3-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9fa3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9fa3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9fa3-123">CommonParameters</span></span>
<span data-ttu-id="f9fa3-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9fa3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9fa3-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9fa3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9fa3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9fa3-126">INPUTS</span></span>

### <span data-ttu-id="f9fa3-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="f9fa3-127">None</span></span>

## <span data-ttu-id="f9fa3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9fa3-128">OUTPUTS</span></span>

### <span data-ttu-id="f9fa3-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f9fa3-129">System.Boolean</span></span>

## <span data-ttu-id="f9fa3-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9fa3-130">NOTES</span></span>

## <span data-ttu-id="f9fa3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9fa3-131">RELATED LINKS</span></span>

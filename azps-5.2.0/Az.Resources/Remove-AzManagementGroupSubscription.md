---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 843a510376e49a1416129d719c141d72ec80df35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355530"
---
# <span data-ttu-id="f7a37-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="f7a37-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="f7a37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7a37-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a37-103">Eltávolít egy előfizetést egy felügyeleti csoportból.</span><span class="sxs-lookup"><span data-stu-id="f7a37-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="f7a37-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f7a37-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7a37-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f7a37-105">DESCRIPTION</span></span>
<span data-ttu-id="f7a37-106">A **Remove-AzManagementGroupSubscription** parancsmag eltávolít egy előfizetést egy felügyeleti csoportból.</span><span class="sxs-lookup"><span data-stu-id="f7a37-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="f7a37-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f7a37-107">EXAMPLES</span></span>

### <span data-ttu-id="f7a37-108">1. példa: Előfizetés eltávolítása egy felügyeleti csoportból</span><span class="sxs-lookup"><span data-stu-id="f7a37-108">Example 1: Remove Subscription from a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="f7a37-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7a37-109">PARAMETERS</span></span>

### <span data-ttu-id="f7a37-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a37-110">-DefaultProfile</span></span>
<span data-ttu-id="f7a37-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7a37-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7a37-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="f7a37-112">-GroupName</span></span>
<span data-ttu-id="f7a37-113">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="f7a37-113">Management Group Id</span></span>

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

### <span data-ttu-id="f7a37-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7a37-114">-PassThru</span></span>
<span data-ttu-id="f7a37-115">A `true` sikeres végrehajtás visszaküldése</span><span class="sxs-lookup"><span data-stu-id="f7a37-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="f7a37-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7a37-116">-SubscriptionId</span></span>
<span data-ttu-id="f7a37-117">A kezeléshez társított előfizetés előfizetés-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f7a37-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="f7a37-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7a37-118">-Confirm</span></span>
<span data-ttu-id="f7a37-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f7a37-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7a37-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7a37-120">-WhatIf</span></span>
<span data-ttu-id="f7a37-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f7a37-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7a37-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7a37-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7a37-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a37-123">CommonParameters</span></span>
<span data-ttu-id="f7a37-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7a37-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a37-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7a37-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a37-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7a37-126">INPUTS</span></span>

### <span data-ttu-id="f7a37-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="f7a37-127">None</span></span>

## <span data-ttu-id="f7a37-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7a37-128">OUTPUTS</span></span>

### <span data-ttu-id="f7a37-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7a37-129">System.Boolean</span></span>

## <span data-ttu-id="f7a37-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f7a37-130">NOTES</span></span>

## <span data-ttu-id="f7a37-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7a37-131">RELATED LINKS</span></span>

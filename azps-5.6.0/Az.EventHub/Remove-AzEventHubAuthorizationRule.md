---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 496806b6d5ab6b7d6e1c788b7b42424b7e97a8c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939593"
---
# <span data-ttu-id="d92c7-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d92c7-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="d92c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d92c7-102">SYNOPSIS</span></span>
<span data-ttu-id="d92c7-103">Eltávolítja a megadott eseményközpont engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="d92c7-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="d92c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d92c7-104">SYNTAX</span></span>

### <span data-ttu-id="d92c7-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d92c7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d92c7-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d92c7-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d92c7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d92c7-107">DESCRIPTION</span></span>
<span data-ttu-id="d92c7-108">A Remove-AzEventHubAuthorizationRule parancsmag eltávolítja és törli a megadott engedélyezési szabályt a megadott eseményközpontból.</span><span class="sxs-lookup"><span data-stu-id="d92c7-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="d92c7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d92c7-109">EXAMPLES</span></span>

### <span data-ttu-id="d92c7-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d92c7-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="d92c7-111">Eltávolítja a \` MyAuthRuleName engedélyezési szabályt \` a Namespace \` MyNamespaceName \` névtérből.</span><span class="sxs-lookup"><span data-stu-id="d92c7-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="d92c7-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d92c7-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="d92c7-113">Eltávolítja a \` MyAuthRuleName engedélyezési szabályt \` a \` MyEventHubName \` eseményközpontból.</span><span class="sxs-lookup"><span data-stu-id="d92c7-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="d92c7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d92c7-114">PARAMETERS</span></span>

### <span data-ttu-id="d92c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d92c7-115">-DefaultProfile</span></span>
<span data-ttu-id="d92c7-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d92c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d92c7-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d92c7-117">-EventHub</span></span>
<span data-ttu-id="d92c7-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="d92c7-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d92c7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d92c7-119">-Force</span></span>
<span data-ttu-id="d92c7-120">Ne kérjen megerősítést</span><span class="sxs-lookup"><span data-stu-id="d92c7-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="d92c7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d92c7-121">-Name</span></span>
<span data-ttu-id="d92c7-122">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="d92c7-122">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d92c7-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d92c7-123">-Namespace</span></span>
<span data-ttu-id="d92c7-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="d92c7-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d92c7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d92c7-125">-PassThru</span></span>
<span data-ttu-id="d92c7-126">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="d92c7-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d92c7-127">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d92c7-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d92c7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d92c7-128">-ResourceGroupName</span></span>
<span data-ttu-id="d92c7-129">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d92c7-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d92c7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d92c7-130">-Confirm</span></span>
<span data-ttu-id="d92c7-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d92c7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d92c7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d92c7-132">-WhatIf</span></span>
<span data-ttu-id="d92c7-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d92c7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d92c7-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d92c7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d92c7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d92c7-135">CommonParameters</span></span>
<span data-ttu-id="d92c7-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d92c7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d92c7-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d92c7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d92c7-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d92c7-138">INPUTS</span></span>

### <span data-ttu-id="d92c7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d92c7-139">System.String</span></span>

## <span data-ttu-id="d92c7-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d92c7-140">OUTPUTS</span></span>

### <span data-ttu-id="d92c7-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d92c7-141">System.Boolean</span></span>

## <span data-ttu-id="d92c7-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d92c7-142">NOTES</span></span>

## <span data-ttu-id="d92c7-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d92c7-143">RELATED LINKS</span></span>

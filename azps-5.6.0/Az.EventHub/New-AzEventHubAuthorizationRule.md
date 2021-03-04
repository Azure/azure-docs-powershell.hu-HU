---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: fde71fed26c074efa705d0b1dc181dfb46bae44e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921193"
---
# <span data-ttu-id="0cee7-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0cee7-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="0cee7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cee7-102">SYNOPSIS</span></span>
<span data-ttu-id="0cee7-103">Létrehoz egy új Eseményközpontok engedélyezési szabályt a namespace vagy az eventhub számára.</span><span class="sxs-lookup"><span data-stu-id="0cee7-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="0cee7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0cee7-104">SYNTAX</span></span>

### <span data-ttu-id="0cee7-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0cee7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cee7-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0cee7-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cee7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0cee7-107">DESCRIPTION</span></span>
<span data-ttu-id="0cee7-108">A New-AzEventHubAuthorizationRule parancsmag létrehoz egy új Eseményközpontok engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="0cee7-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="0cee7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0cee7-109">EXAMPLES</span></span>

### <span data-ttu-id="0cee7-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="0cee7-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="0cee7-111">Létrehoz egy engedélyezési szabályt, amely a MyAuthRuleName engedélyt adja a \` \` MyNamespaceName nevű névtérnek \` a \` \` MyResourceGroupName \` erőforráscsoporttal.</span><span class="sxs-lookup"><span data-stu-id="0cee7-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0cee7-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0cee7-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="0cee7-113">Létrehoz egy engedélyezési szabályt, amely a MyAuthRuleName engedélyt adja a \` \` \` \` \` \` \` MyResourceGroupName \` nevű erőforráscsoporttal az Eseményközpont MyEventHubName nevű eseményközpontja számára a MyNamespaceName névterében.</span><span class="sxs-lookup"><span data-stu-id="0cee7-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0cee7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cee7-114">PARAMETERS</span></span>

### <span data-ttu-id="0cee7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cee7-115">-DefaultProfile</span></span>
<span data-ttu-id="0cee7-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cee7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cee7-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="0cee7-117">-EventHub</span></span>
<span data-ttu-id="0cee7-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="0cee7-118">EventHub Name</span></span>

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

### <span data-ttu-id="0cee7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0cee7-119">-Name</span></span>
<span data-ttu-id="0cee7-120">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="0cee7-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="0cee7-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0cee7-121">-Namespace</span></span>
<span data-ttu-id="0cee7-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="0cee7-122">Namespace Name</span></span>

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

### <span data-ttu-id="0cee7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cee7-123">-ResourceGroupName</span></span>
<span data-ttu-id="0cee7-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0cee7-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0cee7-125">-Rights</span><span class="sxs-lookup"><span data-stu-id="0cee7-125">-Rights</span></span>
<span data-ttu-id="0cee7-126">Jogok, például "Figyel", "Küldés", "Kezelés"</span><span class="sxs-lookup"><span data-stu-id="0cee7-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cee7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cee7-127">-Confirm</span></span>
<span data-ttu-id="0cee7-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0cee7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cee7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cee7-129">-WhatIf</span></span>
<span data-ttu-id="0cee7-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0cee7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cee7-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0cee7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cee7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cee7-132">CommonParameters</span></span>
<span data-ttu-id="0cee7-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cee7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cee7-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cee7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cee7-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0cee7-135">INPUTS</span></span>

### <span data-ttu-id="0cee7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0cee7-136">System.String</span></span>

### <span data-ttu-id="0cee7-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0cee7-137">System.String[]</span></span>

## <span data-ttu-id="0cee7-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cee7-138">OUTPUTS</span></span>

### <span data-ttu-id="0cee7-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0cee7-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0cee7-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0cee7-140">NOTES</span></span>

## <span data-ttu-id="0cee7-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cee7-141">RELATED LINKS</span></span>

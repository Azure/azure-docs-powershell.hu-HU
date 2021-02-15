---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147915"
---
# <span data-ttu-id="da513-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="da513-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="da513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da513-102">SYNOPSIS</span></span>
<span data-ttu-id="da513-103">Létrehoz egy új Eseményközpontok engedélyezési szabályt a namespace vagy az eventhub számára.</span><span class="sxs-lookup"><span data-stu-id="da513-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="da513-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da513-104">SYNTAX</span></span>

### <span data-ttu-id="da513-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da513-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da513-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="da513-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da513-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da513-107">DESCRIPTION</span></span>
<span data-ttu-id="da513-108">A New-AzEventHubAuthorizationRule parancsmag létrehoz egy új Eseményközpontok engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="da513-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="da513-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da513-109">EXAMPLES</span></span>

### <span data-ttu-id="da513-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="da513-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="da513-111">Létrehoz egy engedélyezési szabályt, amely a MyAuthRuleName engedélyt adja a \` \` MyNamespaceName nevű névtérnek \` a \` \` MyResourceGroupName \` erőforráscsoporttal.</span><span class="sxs-lookup"><span data-stu-id="da513-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="da513-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="da513-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="da513-113">Létrehoz egy engedélyezési szabályt, amely a MyAuthRuleName engedélyt adja a MyResourceGroupName nevű erőforráscsoporttal a \` \` \` \` \` \` \` MyResourceHubName eseményközpont MyEventHubName nevű eseményközpontjában. \`</span><span class="sxs-lookup"><span data-stu-id="da513-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="da513-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da513-114">PARAMETERS</span></span>

### <span data-ttu-id="da513-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da513-115">-DefaultProfile</span></span>
<span data-ttu-id="da513-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da513-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da513-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="da513-117">-EventHub</span></span>
<span data-ttu-id="da513-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="da513-118">EventHub Name</span></span>

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

### <span data-ttu-id="da513-119">-Name</span><span class="sxs-lookup"><span data-stu-id="da513-119">-Name</span></span>
<span data-ttu-id="da513-120">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="da513-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="da513-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="da513-121">-Namespace</span></span>
<span data-ttu-id="da513-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="da513-122">Namespace Name</span></span>

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

### <span data-ttu-id="da513-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da513-123">-ResourceGroupName</span></span>
<span data-ttu-id="da513-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="da513-124">Resource Group Name</span></span>

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

### <span data-ttu-id="da513-125">-Rights</span><span class="sxs-lookup"><span data-stu-id="da513-125">-Rights</span></span>
<span data-ttu-id="da513-126">Jogok, például "Figyel", "Küldés", "Kezelés"</span><span class="sxs-lookup"><span data-stu-id="da513-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="da513-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da513-127">-Confirm</span></span>
<span data-ttu-id="da513-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="da513-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da513-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da513-129">-WhatIf</span></span>
<span data-ttu-id="da513-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="da513-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da513-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da513-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da513-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da513-132">CommonParameters</span></span>
<span data-ttu-id="da513-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da513-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da513-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da513-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da513-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da513-135">INPUTS</span></span>

### <span data-ttu-id="da513-136">System.String</span><span class="sxs-lookup"><span data-stu-id="da513-136">System.String</span></span>

### <span data-ttu-id="da513-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="da513-137">System.String[]</span></span>

## <span data-ttu-id="da513-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da513-138">OUTPUTS</span></span>

### <span data-ttu-id="da513-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="da513-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="da513-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da513-140">NOTES</span></span>

## <span data-ttu-id="da513-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da513-141">RELATED LINKS</span></span>

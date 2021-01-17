---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 862b6f295a997b2027520a3f9c6a9f4f9cfb5ae9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466147"
---
# <span data-ttu-id="fae86-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fae86-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="fae86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fae86-102">SYNOPSIS</span></span>
<span data-ttu-id="fae86-103">Frissíti a megadott engedélyezési szabályt egy eseményközpontban.</span><span class="sxs-lookup"><span data-stu-id="fae86-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="fae86-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fae86-104">SYNTAX</span></span>

### <span data-ttu-id="fae86-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fae86-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae86-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fae86-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae86-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fae86-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fae86-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fae86-108">DESCRIPTION</span></span>
<span data-ttu-id="fae86-109">A Set-AzEventHubAuthorizationRule parancsmag frissíti a megadott engedélyezési szabályt a megadott eseményközpontban.</span><span class="sxs-lookup"><span data-stu-id="fae86-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="fae86-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fae86-110">EXAMPLES</span></span>

### <span data-ttu-id="fae86-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fae86-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="fae86-112">Frissíti a MyAuthRuleName engedélyezési szabályt, hogy a MyEventHubName eseményközpontra vonatkozó, a \` MyNamespaceName névtér által hatókörbe tartozó manage rightsot \` \` \` \` biztosítsa. \`</span><span class="sxs-lookup"><span data-stu-id="fae86-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="fae86-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fae86-113">PARAMETERS</span></span>

### <span data-ttu-id="fae86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae86-114">-DefaultProfile</span></span>
<span data-ttu-id="fae86-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fae86-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fae86-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="fae86-116">-EventHub</span></span>
<span data-ttu-id="fae86-117">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="fae86-117">EventHub Name</span></span>

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

### <span data-ttu-id="fae86-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fae86-118">-InputObject</span></span>
<span data-ttu-id="fae86-119">AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="fae86-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fae86-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fae86-120">-Name</span></span>
<span data-ttu-id="fae86-121">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="fae86-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="fae86-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fae86-122">-Namespace</span></span>
<span data-ttu-id="fae86-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="fae86-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fae86-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae86-124">-ResourceGroupName</span></span>
<span data-ttu-id="fae86-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fae86-125">Resource Group Name</span></span>

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

### <span data-ttu-id="fae86-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="fae86-126">-Rights</span></span>
<span data-ttu-id="fae86-127">Jogok, például @("Hallgatás","Küldés","Kezelés")</span><span class="sxs-lookup"><span data-stu-id="fae86-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fae86-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fae86-128">-Confirm</span></span>
<span data-ttu-id="fae86-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fae86-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae86-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae86-130">-WhatIf</span></span>
<span data-ttu-id="fae86-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fae86-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fae86-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fae86-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae86-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae86-133">CommonParameters</span></span>
<span data-ttu-id="fae86-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae86-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae86-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae86-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae86-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fae86-136">INPUTS</span></span>

### <span data-ttu-id="fae86-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fae86-137">System.String</span></span>

### <span data-ttu-id="fae86-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fae86-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="fae86-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="fae86-139">System.String[]</span></span>

## <span data-ttu-id="fae86-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fae86-140">OUTPUTS</span></span>

### <span data-ttu-id="fae86-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fae86-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="fae86-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fae86-142">NOTES</span></span>

## <span data-ttu-id="fae86-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fae86-143">RELATED LINKS</span></span>

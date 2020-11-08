---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 862b6f295a997b2027520a3f9c6a9f4f9cfb5ae9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184961"
---
# <span data-ttu-id="00fd3-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="00fd3-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="00fd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="00fd3-103">A megadott engedélyezési szabály frissítése az esemény központjában.</span><span class="sxs-lookup"><span data-stu-id="00fd3-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="00fd3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00fd3-104">SYNTAX</span></span>

### <span data-ttu-id="00fd3-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00fd3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00fd3-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="00fd3-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00fd3-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="00fd3-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00fd3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="00fd3-108">DESCRIPTION</span></span>
<span data-ttu-id="00fd3-109">A Set-AzEventHubAuthorizationRule parancsmag a megadott engedélyezési szabályt frissíti az esemény központjában.</span><span class="sxs-lookup"><span data-stu-id="00fd3-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="00fd3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="00fd3-110">EXAMPLES</span></span>

### <span data-ttu-id="00fd3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="00fd3-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="00fd3-112">Frissíti az MyAuthRuleName-as engedélyezési szabályt, \` \` amely az esemény-hub \` MyEventHubName \` , a névtér MyNamespaceName alapján kezeli a jogosultságokat \` \` .</span><span class="sxs-lookup"><span data-stu-id="00fd3-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="00fd3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00fd3-113">PARAMETERS</span></span>

### <span data-ttu-id="00fd3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fd3-114">-DefaultProfile</span></span>
<span data-ttu-id="00fd3-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00fd3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00fd3-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="00fd3-116">-EventHub</span></span>
<span data-ttu-id="00fd3-117">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="00fd3-117">EventHub Name</span></span>

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

### <span data-ttu-id="00fd3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00fd3-118">-InputObject</span></span>
<span data-ttu-id="00fd3-119">AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="00fd3-119">AuthorizationRule Object</span></span>

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

### <span data-ttu-id="00fd3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="00fd3-120">-Name</span></span>
<span data-ttu-id="00fd3-121">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="00fd3-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="00fd3-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="00fd3-122">-Namespace</span></span>
<span data-ttu-id="00fd3-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="00fd3-123">Namespace Name</span></span>

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

### <span data-ttu-id="00fd3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00fd3-124">-ResourceGroupName</span></span>
<span data-ttu-id="00fd3-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="00fd3-125">Resource Group Name</span></span>

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

### <span data-ttu-id="00fd3-126">– Jogok</span><span class="sxs-lookup"><span data-stu-id="00fd3-126">-Rights</span></span>
<span data-ttu-id="00fd3-127">Jogok, például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="00fd3-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="00fd3-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="00fd3-128">-Confirm</span></span>
<span data-ttu-id="00fd3-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="00fd3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00fd3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00fd3-130">-WhatIf</span></span>
<span data-ttu-id="00fd3-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="00fd3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00fd3-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00fd3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00fd3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fd3-133">CommonParameters</span></span>
<span data-ttu-id="00fd3-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00fd3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fd3-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00fd3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fd3-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00fd3-136">INPUTS</span></span>

### <span data-ttu-id="00fd3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="00fd3-137">System.String</span></span>

### <span data-ttu-id="00fd3-138">Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="00fd3-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="00fd3-139">System. string []</span><span class="sxs-lookup"><span data-stu-id="00fd3-139">System.String[]</span></span>

## <span data-ttu-id="00fd3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00fd3-140">OUTPUTS</span></span>

### <span data-ttu-id="00fd3-141">Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="00fd3-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="00fd3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00fd3-142">NOTES</span></span>

## <span data-ttu-id="00fd3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00fd3-143">RELATED LINKS</span></span>

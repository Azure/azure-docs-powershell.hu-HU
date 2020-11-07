---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 89a3d5678aec88d209ab2ef7d9ada87bcf407410
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670840"
---
# <span data-ttu-id="9e5d2-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9e5d2-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="9e5d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5d2-103">Új esemény-hubok engedélyezési szabályának létrehozása a névtérhez vagy a eventhub.</span><span class="sxs-lookup"><span data-stu-id="9e5d2-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="9e5d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e5d2-104">SYNTAX</span></span>

### <span data-ttu-id="9e5d2-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e5d2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e5d2-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e5d2-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e5d2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e5d2-107">DESCRIPTION</span></span>
<span data-ttu-id="9e5d2-108">Az New-AzEventHubAuthorizationRule parancsmag új esemény-hubok engedélyezési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9e5d2-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="9e5d2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9e5d2-109">EXAMPLES</span></span>

### <span data-ttu-id="9e5d2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9e5d2-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="9e5d2-111">Létrehoz egy engedélyezési szabályt \` \` , amely megadhatja a MyAuthRuleName, amely figyeli és elküldi a jogosultságokat a névtér \` MyNamespaceName \` , az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9e5d2-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9e5d2-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="9e5d2-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="9e5d2-113">Létrehoz egy engedélyezési szabályt \` \` , amely megadhatja a MyAuthRuleName, amely figyeli és elküldi a jogosultságokat az esemény központi \` MyEventHubName a \` MyNamespaceName névtér- \` \` , az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9e5d2-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="9e5d2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e5d2-114">PARAMETERS</span></span>

### <span data-ttu-id="9e5d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5d2-115">-DefaultProfile</span></span>
<span data-ttu-id="9e5d2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e5d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e5d2-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="9e5d2-117">-EventHub</span></span>
<span data-ttu-id="9e5d2-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="9e5d2-118">EventHub Name</span></span>

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

### <span data-ttu-id="9e5d2-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e5d2-119">-Name</span></span>
<span data-ttu-id="9e5d2-120">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="9e5d2-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="9e5d2-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9e5d2-121">-Namespace</span></span>
<span data-ttu-id="9e5d2-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="9e5d2-122">Namespace Name</span></span>

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

### <span data-ttu-id="9e5d2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e5d2-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e5d2-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9e5d2-124">Resource Group Name</span></span>

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

### <span data-ttu-id="9e5d2-125">– Jogok</span><span class="sxs-lookup"><span data-stu-id="9e5d2-125">-Rights</span></span>
<span data-ttu-id="9e5d2-126">Jogok (például "Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="9e5d2-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="9e5d2-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9e5d2-127">-Confirm</span></span>
<span data-ttu-id="9e5d2-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e5d2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e5d2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e5d2-129">-WhatIf</span></span>
<span data-ttu-id="9e5d2-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9e5d2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e5d2-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e5d2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e5d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5d2-132">CommonParameters</span></span>
<span data-ttu-id="9e5d2-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e5d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5d2-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e5d2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5d2-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e5d2-135">INPUTS</span></span>

### <span data-ttu-id="9e5d2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9e5d2-136">System.String</span></span>

### <span data-ttu-id="9e5d2-137">System. string []</span><span class="sxs-lookup"><span data-stu-id="9e5d2-137">System.String[]</span></span>

## <span data-ttu-id="9e5d2-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e5d2-138">OUTPUTS</span></span>

### <span data-ttu-id="9e5d2-139">Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9e5d2-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9e5d2-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e5d2-140">NOTES</span></span>

## <span data-ttu-id="9e5d2-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e5d2-141">RELATED LINKS</span></span>

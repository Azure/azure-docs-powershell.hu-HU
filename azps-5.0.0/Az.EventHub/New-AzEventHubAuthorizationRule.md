---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194390"
---
# <span data-ttu-id="f3d67-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f3d67-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="f3d67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3d67-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d67-103">Új esemény-hubok engedélyezési szabályának létrehozása a névtérhez vagy a eventhub.</span><span class="sxs-lookup"><span data-stu-id="f3d67-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="f3d67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3d67-104">SYNTAX</span></span>

### <span data-ttu-id="f3d67-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3d67-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d67-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f3d67-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3d67-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3d67-107">DESCRIPTION</span></span>
<span data-ttu-id="f3d67-108">Az New-AzEventHubAuthorizationRule parancsmag új esemény-hubok engedélyezési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f3d67-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="f3d67-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f3d67-109">EXAMPLES</span></span>

### <span data-ttu-id="f3d67-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f3d67-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="f3d67-111">Létrehoz egy engedélyezési szabályt \` \` , amely megadhatja a MyAuthRuleName, amely figyeli és elküldi a jogosultságokat a névtér \` MyNamespaceName \` , az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f3d67-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f3d67-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="f3d67-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="f3d67-113">Létrehoz egy engedélyezési szabályt \` \` , amely megadhatja a MyAuthRuleName, amely figyeli és elküldi a jogosultságokat az esemény központi \` MyEventHubName a \` MyNamespaceName névtér- \` \` , az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f3d67-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f3d67-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3d67-114">PARAMETERS</span></span>

### <span data-ttu-id="f3d67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d67-115">-DefaultProfile</span></span>
<span data-ttu-id="f3d67-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3d67-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3d67-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f3d67-117">-EventHub</span></span>
<span data-ttu-id="f3d67-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="f3d67-118">EventHub Name</span></span>

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

### <span data-ttu-id="f3d67-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3d67-119">-Name</span></span>
<span data-ttu-id="f3d67-120">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="f3d67-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f3d67-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f3d67-121">-Namespace</span></span>
<span data-ttu-id="f3d67-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f3d67-122">Namespace Name</span></span>

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

### <span data-ttu-id="f3d67-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d67-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3d67-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f3d67-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f3d67-125">– Jogok</span><span class="sxs-lookup"><span data-stu-id="f3d67-125">-Rights</span></span>
<span data-ttu-id="f3d67-126">Jogok (például "Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="f3d67-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="f3d67-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3d67-127">-Confirm</span></span>
<span data-ttu-id="f3d67-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3d67-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3d67-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3d67-129">-WhatIf</span></span>
<span data-ttu-id="f3d67-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3d67-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3d67-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3d67-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3d67-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d67-132">CommonParameters</span></span>
<span data-ttu-id="f3d67-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3d67-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d67-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d67-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d67-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3d67-135">INPUTS</span></span>

### <span data-ttu-id="f3d67-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f3d67-136">System.String</span></span>

### <span data-ttu-id="f3d67-137">System. string []</span><span class="sxs-lookup"><span data-stu-id="f3d67-137">System.String[]</span></span>

## <span data-ttu-id="f3d67-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3d67-138">OUTPUTS</span></span>

### <span data-ttu-id="f3d67-139">Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f3d67-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f3d67-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3d67-140">NOTES</span></span>

## <span data-ttu-id="f3d67-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3d67-141">RELATED LINKS</span></span>

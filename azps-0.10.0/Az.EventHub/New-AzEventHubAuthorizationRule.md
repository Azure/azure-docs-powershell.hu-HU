---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: c59a58e458ceed2c183978a8839de1cd864ffaa7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842326"
---
# <span data-ttu-id="ab55a-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ab55a-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="ab55a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab55a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab55a-103">Új esemény-hubok engedélyezési szabályának létrehozása a névtérhez vagy a eventhub.</span><span class="sxs-lookup"><span data-stu-id="ab55a-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="ab55a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab55a-104">SYNTAX</span></span>

### <span data-ttu-id="ab55a-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab55a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab55a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ab55a-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab55a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab55a-107">DESCRIPTION</span></span>
<span data-ttu-id="ab55a-108">Az New-AzEventHubAuthorizationRule parancsmag új esemény-hubok engedélyezési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ab55a-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="ab55a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ab55a-109">EXAMPLES</span></span>

### <span data-ttu-id="ab55a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ab55a-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="ab55a-111">Létrehoz egy engedélyezési szabályt \` \` , amely megadhatja a MyAuthRuleName, amely figyeli és elküldi a jogosultságokat a névtér \` MyNamespaceName \` , az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ab55a-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ab55a-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="ab55a-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="ab55a-113">Létrehoz egy engedélyezési szabályt \` \` , amely megadhatja a MyAuthRuleName, amely figyeli és elküldi a jogosultságokat az esemény központi \` MyEventHubName a \` MyNamespaceName névtér- \` \` , az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ab55a-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ab55a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab55a-114">PARAMETERS</span></span>

### <span data-ttu-id="ab55a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab55a-115">-DefaultProfile</span></span>
<span data-ttu-id="ab55a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab55a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab55a-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ab55a-117">-EventHub</span></span>
<span data-ttu-id="ab55a-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="ab55a-118">EventHub Name</span></span>

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

### <span data-ttu-id="ab55a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab55a-119">-Name</span></span>
<span data-ttu-id="ab55a-120">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="ab55a-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="ab55a-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ab55a-121">-Namespace</span></span>
<span data-ttu-id="ab55a-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="ab55a-122">Namespace Name</span></span>

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

### <span data-ttu-id="ab55a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab55a-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab55a-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ab55a-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ab55a-125">– Jogok</span><span class="sxs-lookup"><span data-stu-id="ab55a-125">-Rights</span></span>
<span data-ttu-id="ab55a-126">Jogok (például "Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="ab55a-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="ab55a-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ab55a-127">-Confirm</span></span>
<span data-ttu-id="ab55a-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ab55a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab55a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab55a-129">-WhatIf</span></span>
<span data-ttu-id="ab55a-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ab55a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab55a-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab55a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab55a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab55a-132">CommonParameters</span></span>
<span data-ttu-id="ab55a-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab55a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab55a-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab55a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab55a-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab55a-135">INPUTS</span></span>

### <span data-ttu-id="ab55a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ab55a-136">System.String</span></span>

### <span data-ttu-id="ab55a-137">System. string []</span><span class="sxs-lookup"><span data-stu-id="ab55a-137">System.String[]</span></span>

## <span data-ttu-id="ab55a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab55a-138">OUTPUTS</span></span>

### <span data-ttu-id="ab55a-139">Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ab55a-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ab55a-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab55a-140">NOTES</span></span>

## <span data-ttu-id="ab55a-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab55a-141">RELATED LINKS</span></span>

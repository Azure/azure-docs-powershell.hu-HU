---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4965fb6047ca31d2c5b70276a777235d2a3cb050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496572"
---
# <span data-ttu-id="5892d-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5892d-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="5892d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5892d-102">SYNOPSIS</span></span>
<span data-ttu-id="5892d-103">A megadott engedélyezési szabály frissítése az esemény központjában.</span><span class="sxs-lookup"><span data-stu-id="5892d-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5892d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5892d-104">SYNTAX</span></span>

### <span data-ttu-id="5892d-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5892d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5892d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5892d-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5892d-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5892d-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5892d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5892d-108">DESCRIPTION</span></span>
<span data-ttu-id="5892d-109">A Set-AzureRmEventHubAuthorizationRule parancsmag a megadott engedélyezési szabályt frissíti az esemény központjában.</span><span class="sxs-lookup"><span data-stu-id="5892d-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="5892d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5892d-110">EXAMPLES</span></span>

### <span data-ttu-id="5892d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5892d-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="5892d-112">Frissíti az MyAuthRuleName-as engedélyezési szabályt, \` \` amely az esemény-hub \` MyEventHubName \` , a névtér MyNamespaceName alapján kezeli a jogosultságokat \` \` .</span><span class="sxs-lookup"><span data-stu-id="5892d-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="5892d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5892d-113">PARAMETERS</span></span>

### <span data-ttu-id="5892d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5892d-114">-DefaultProfile</span></span>
<span data-ttu-id="5892d-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5892d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5892d-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5892d-116">-EventHub</span></span>
<span data-ttu-id="5892d-117">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="5892d-117">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5892d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5892d-118">-InputObject</span></span>
<span data-ttu-id="5892d-119">AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="5892d-119">AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5892d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5892d-120">-Name</span></span>
<span data-ttu-id="5892d-121">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="5892d-121">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5892d-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5892d-122">-Namespace</span></span>
<span data-ttu-id="5892d-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="5892d-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5892d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5892d-124">-ResourceGroupName</span></span>
<span data-ttu-id="5892d-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5892d-125">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5892d-126">– Jogok</span><span class="sxs-lookup"><span data-stu-id="5892d-126">-Rights</span></span>
<span data-ttu-id="5892d-127">Jogok, például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="5892d-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5892d-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5892d-128">-Confirm</span></span>
<span data-ttu-id="5892d-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5892d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5892d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5892d-130">-WhatIf</span></span>
<span data-ttu-id="5892d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5892d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5892d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5892d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5892d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5892d-133">CommonParameters</span></span>
<span data-ttu-id="5892d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5892d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5892d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5892d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5892d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5892d-136">INPUTS</span></span>

### <span data-ttu-id="5892d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5892d-137">System.String</span></span>
<span data-ttu-id="5892d-138">Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes System. string []</span><span class="sxs-lookup"><span data-stu-id="5892d-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="5892d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5892d-139">OUTPUTS</span></span>

### <span data-ttu-id="5892d-140">Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5892d-140">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="5892d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5892d-141">NOTES</span></span>

## <span data-ttu-id="5892d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5892d-142">RELATED LINKS</span></span>

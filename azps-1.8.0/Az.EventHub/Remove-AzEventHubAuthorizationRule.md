---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 9e7cfbe1ec0810b9d18f884306535d37a6110dd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670831"
---
# <span data-ttu-id="411c8-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="411c8-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="411c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="411c8-102">SYNOPSIS</span></span>
<span data-ttu-id="411c8-103">Eltávolítja a megadott esemény központi engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="411c8-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="411c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="411c8-104">SYNTAX</span></span>

### <span data-ttu-id="411c8-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="411c8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="411c8-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="411c8-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="411c8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="411c8-107">DESCRIPTION</span></span>
<span data-ttu-id="411c8-108">A Remove-AzEventHubAuthorizationRule parancsmag eltávolítja és törli a megadott engedélyezési szabályt az esemény központból.</span><span class="sxs-lookup"><span data-stu-id="411c8-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="411c8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="411c8-109">EXAMPLES</span></span>

### <span data-ttu-id="411c8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="411c8-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="411c8-111">Eltávolítja az engedélyezési szabályt \` \` a MyAuthRuleName a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="411c8-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="411c8-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="411c8-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="411c8-113">Eltávolítja az MyAuthRuleName-as engedélyezési szabályt \` \` az esemény központi \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="411c8-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="411c8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="411c8-114">PARAMETERS</span></span>

### <span data-ttu-id="411c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="411c8-115">-DefaultProfile</span></span>
<span data-ttu-id="411c8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="411c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="411c8-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="411c8-117">-EventHub</span></span>
<span data-ttu-id="411c8-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="411c8-118">EventHub Name</span></span>

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

### <span data-ttu-id="411c8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="411c8-119">-Force</span></span>
<span data-ttu-id="411c8-120">Ne kérjen megerősítést</span><span class="sxs-lookup"><span data-stu-id="411c8-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="411c8-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="411c8-121">-Name</span></span>
<span data-ttu-id="411c8-122">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="411c8-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="411c8-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="411c8-123">-Namespace</span></span>
<span data-ttu-id="411c8-124">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="411c8-124">Namespace Name</span></span>

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

### <span data-ttu-id="411c8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="411c8-125">-PassThru</span></span>
<span data-ttu-id="411c8-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="411c8-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="411c8-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="411c8-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="411c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="411c8-128">-ResourceGroupName</span></span>
<span data-ttu-id="411c8-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="411c8-129">Resource Group Name</span></span>

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

### <span data-ttu-id="411c8-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="411c8-130">-Confirm</span></span>
<span data-ttu-id="411c8-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="411c8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="411c8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="411c8-132">-WhatIf</span></span>
<span data-ttu-id="411c8-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="411c8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="411c8-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="411c8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="411c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="411c8-135">CommonParameters</span></span>
<span data-ttu-id="411c8-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="411c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="411c8-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="411c8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="411c8-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="411c8-138">INPUTS</span></span>

### <span data-ttu-id="411c8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="411c8-139">System.String</span></span>

## <span data-ttu-id="411c8-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="411c8-140">OUTPUTS</span></span>

### <span data-ttu-id="411c8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="411c8-141">System.Boolean</span></span>

## <span data-ttu-id="411c8-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="411c8-142">NOTES</span></span>

## <span data-ttu-id="411c8-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="411c8-143">RELATED LINKS</span></span>

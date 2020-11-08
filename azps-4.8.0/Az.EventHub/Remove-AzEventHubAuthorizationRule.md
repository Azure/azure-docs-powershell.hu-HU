---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182235"
---
# <span data-ttu-id="b983e-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b983e-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="b983e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b983e-102">SYNOPSIS</span></span>
<span data-ttu-id="b983e-103">Eltávolítja a megadott esemény központi engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="b983e-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="b983e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b983e-104">SYNTAX</span></span>

### <span data-ttu-id="b983e-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b983e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b983e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b983e-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b983e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b983e-107">DESCRIPTION</span></span>
<span data-ttu-id="b983e-108">A Remove-AzEventHubAuthorizationRule parancsmag eltávolítja és törli a megadott engedélyezési szabályt az esemény központból.</span><span class="sxs-lookup"><span data-stu-id="b983e-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="b983e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b983e-109">EXAMPLES</span></span>

### <span data-ttu-id="b983e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b983e-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="b983e-111">Eltávolítja az engedélyezési szabályt \` \` a MyAuthRuleName a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="b983e-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="b983e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="b983e-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="b983e-113">Eltávolítja az MyAuthRuleName-as engedélyezési szabályt \` \` az esemény központi \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="b983e-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="b983e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b983e-114">PARAMETERS</span></span>

### <span data-ttu-id="b983e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b983e-115">-DefaultProfile</span></span>
<span data-ttu-id="b983e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b983e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b983e-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b983e-117">-EventHub</span></span>
<span data-ttu-id="b983e-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="b983e-118">EventHub Name</span></span>

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

### <span data-ttu-id="b983e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b983e-119">-Force</span></span>
<span data-ttu-id="b983e-120">Ne kérjen megerősítést</span><span class="sxs-lookup"><span data-stu-id="b983e-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="b983e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b983e-121">-Name</span></span>
<span data-ttu-id="b983e-122">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="b983e-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b983e-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b983e-123">-Namespace</span></span>
<span data-ttu-id="b983e-124">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="b983e-124">Namespace Name</span></span>

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

### <span data-ttu-id="b983e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b983e-125">-PassThru</span></span>
<span data-ttu-id="b983e-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b983e-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b983e-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b983e-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b983e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b983e-128">-ResourceGroupName</span></span>
<span data-ttu-id="b983e-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b983e-129">Resource Group Name</span></span>

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

### <span data-ttu-id="b983e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b983e-130">-Confirm</span></span>
<span data-ttu-id="b983e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b983e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b983e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b983e-132">-WhatIf</span></span>
<span data-ttu-id="b983e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b983e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b983e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b983e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b983e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b983e-135">CommonParameters</span></span>
<span data-ttu-id="b983e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b983e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b983e-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b983e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b983e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b983e-138">INPUTS</span></span>

### <span data-ttu-id="b983e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b983e-139">System.String</span></span>

## <span data-ttu-id="b983e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b983e-140">OUTPUTS</span></span>

### <span data-ttu-id="b983e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b983e-141">System.Boolean</span></span>

## <span data-ttu-id="b983e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b983e-142">NOTES</span></span>

## <span data-ttu-id="b983e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b983e-143">RELATED LINKS</span></span>

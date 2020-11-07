---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 35e3889603dc7e86a7d10679864adfd34a880b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672615"
---
# <span data-ttu-id="19187-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="19187-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="19187-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19187-102">SYNOPSIS</span></span>
<span data-ttu-id="19187-103">Eltávolítja a megadott esemény központi engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="19187-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19187-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19187-104">SYNTAX</span></span>

### <span data-ttu-id="19187-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19187-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19187-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="19187-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19187-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="19187-107">DESCRIPTION</span></span>
<span data-ttu-id="19187-108">A Remove-AzureRmEventHubAuthorizationRule parancsmag eltávolítja és törli a megadott engedélyezési szabályt az esemény központból.</span><span class="sxs-lookup"><span data-stu-id="19187-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="19187-109">Példák</span><span class="sxs-lookup"><span data-stu-id="19187-109">EXAMPLES</span></span>

### <span data-ttu-id="19187-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19187-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="19187-111">Eltávolítja az engedélyezési szabályt \` \` a MyAuthRuleName a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="19187-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="19187-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="19187-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="19187-113">Eltávolítja az MyAuthRuleName-as engedélyezési szabályt \` \` az esemény központi \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="19187-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="19187-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19187-114">PARAMETERS</span></span>

### <span data-ttu-id="19187-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19187-115">-DefaultProfile</span></span>
<span data-ttu-id="19187-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19187-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19187-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="19187-117">-EventHub</span></span>
<span data-ttu-id="19187-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="19187-118">EventHub Name</span></span>

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

### <span data-ttu-id="19187-119">-Force</span><span class="sxs-lookup"><span data-stu-id="19187-119">-Force</span></span>
<span data-ttu-id="19187-120">Ne kérjen megerősítést</span><span class="sxs-lookup"><span data-stu-id="19187-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="19187-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19187-121">-Name</span></span>
<span data-ttu-id="19187-122">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="19187-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="19187-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="19187-123">-Namespace</span></span>
<span data-ttu-id="19187-124">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="19187-124">Namespace Name</span></span>

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

### <span data-ttu-id="19187-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19187-125">-PassThru</span></span>
<span data-ttu-id="19187-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="19187-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="19187-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="19187-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19187-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19187-128">-ResourceGroupName</span></span>
<span data-ttu-id="19187-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="19187-129">Resource Group Name</span></span>

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

### <span data-ttu-id="19187-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19187-130">-Confirm</span></span>
<span data-ttu-id="19187-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19187-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19187-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19187-132">-WhatIf</span></span>
<span data-ttu-id="19187-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19187-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19187-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19187-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19187-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19187-135">CommonParameters</span></span>
<span data-ttu-id="19187-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19187-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19187-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19187-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19187-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19187-138">INPUTS</span></span>

### <span data-ttu-id="19187-139">System. String</span><span class="sxs-lookup"><span data-stu-id="19187-139">System.String</span></span>

## <span data-ttu-id="19187-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19187-140">OUTPUTS</span></span>

### <span data-ttu-id="19187-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19187-141">System.Boolean</span></span>

## <span data-ttu-id="19187-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19187-142">NOTES</span></span>

## <span data-ttu-id="19187-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19187-143">RELATED LINKS</span></span>

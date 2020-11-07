---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 66e32c19001586972cb408e61397545fb1c25d44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666498"
---
# <span data-ttu-id="f8a85-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f8a85-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="f8a85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8a85-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a85-103">Egy engedélyezési szabály részleteit kapja meg, vagy megkapja az engedélyezési szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="f8a85-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="f8a85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8a85-104">SYNTAX</span></span>

### <span data-ttu-id="f8a85-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8a85-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a85-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a85-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a85-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a85-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8a85-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8a85-108">DESCRIPTION</span></span>
<span data-ttu-id="f8a85-109">A Get-AzEventHubAuthorizationRule parancsmag egy engedélyezési szabály részleteit vagy egy adott esemény központhoz tartozó összes engedélyezési szabály listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="f8a85-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="f8a85-110">Ha egy engedélyezési szabály neve meg van határozva, az adott egyetlen engedélyezési szabály részleteit adja vissza a függvény.</span><span class="sxs-lookup"><span data-stu-id="f8a85-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="f8a85-111">Ha egy engedélyezési szabály neve nem jelenik meg, akkor a megadott esemény központjának minden engedélyezési szabályát a program visszaadja.</span><span class="sxs-lookup"><span data-stu-id="f8a85-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="f8a85-112">Ha (katasztrófa-helyreállítási) alias név, a rendszer az aliashoz konfigurált névtér engedélyezési szabályának részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="f8a85-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="f8a85-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f8a85-113">EXAMPLES</span></span>

### <span data-ttu-id="f8a85-114">Példa 1,0-AuthorizationRule a névtérhez</span><span class="sxs-lookup"><span data-stu-id="f8a85-114">Example 1.0 - AuthorizationRule for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="f8a85-115">Az engedélyezési szabály \` MyAuthRuleName a \` névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="f8a85-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="f8a85-116">Példa 1,1-AuthorizationRules a névtérhez</span><span class="sxs-lookup"><span data-stu-id="f8a85-116">Example 1.1 - AuthorizationRules for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="f8a85-117">A névtér MyNamespaceName az összes engedélyezési szabály listáját kapja \` \` .</span><span class="sxs-lookup"><span data-stu-id="f8a85-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="f8a85-118">Példa 2,0-AuthorizationRule a EventHub</span><span class="sxs-lookup"><span data-stu-id="f8a85-118">Example 2.0 - AuthorizationRule for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="f8a85-119">Az \` MyAuthRuleName az \` esemény központi \` MyEventHubName kapja \` , amelyet a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="f8a85-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="f8a85-120">Példa 2,1-AuthorizationRules a EventHub</span><span class="sxs-lookup"><span data-stu-id="f8a85-120">Example 2.1 - AuthorizationRules for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="f8a85-121">A lista engedélyezési szabályait kapja meg az esemény központi \` MyEventHubName \` , amelyet a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="f8a85-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="f8a85-122">Példa 3,0-AuthorizationRule aliashoz (GeoRecovery-konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="f8a85-122">Example 3.0 - AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="f8a85-123">Az engedélyezési szabály \` MyAuthRuleName a \` névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="f8a85-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="f8a85-124">Példa 3,1-AuthorizationRules aliashoz (GeoRecovery-konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="f8a85-124">Example 3.1 -AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="f8a85-125">Beolvassa az összes engedélyezési szabály \` MyAuthRuleName listáját \` a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="f8a85-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="f8a85-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8a85-126">PARAMETERS</span></span>

### <span data-ttu-id="f8a85-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="f8a85-127">-AliasName</span></span>
<span data-ttu-id="f8a85-128">Alias neve</span><span class="sxs-lookup"><span data-stu-id="f8a85-128">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8a85-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a85-129">-DefaultProfile</span></span>
<span data-ttu-id="f8a85-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8a85-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8a85-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="f8a85-131">-Eventhub</span></span>
<span data-ttu-id="f8a85-132">Eventhub neve</span><span class="sxs-lookup"><span data-stu-id="f8a85-132">Eventhub Name</span></span>

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

### <span data-ttu-id="f8a85-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f8a85-133">-Name</span></span>
<span data-ttu-id="f8a85-134">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="f8a85-134">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8a85-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f8a85-135">-Namespace</span></span>
<span data-ttu-id="f8a85-136">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f8a85-136">Namespace Name</span></span>

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

### <span data-ttu-id="f8a85-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a85-137">-ResourceGroupName</span></span>
<span data-ttu-id="f8a85-138">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f8a85-138">Resource Group Name</span></span>

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

### <span data-ttu-id="f8a85-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a85-139">CommonParameters</span></span>
<span data-ttu-id="f8a85-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8a85-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a85-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8a85-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a85-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8a85-142">INPUTS</span></span>

### <span data-ttu-id="f8a85-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f8a85-143">System.String</span></span>

## <span data-ttu-id="f8a85-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8a85-144">OUTPUTS</span></span>

### <span data-ttu-id="f8a85-145">Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f8a85-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f8a85-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8a85-146">NOTES</span></span>

## <span data-ttu-id="f8a85-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8a85-147">RELATED LINKS</span></span>

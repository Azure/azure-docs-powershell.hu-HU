---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194409"
---
# <span data-ttu-id="416f3-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="416f3-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="416f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="416f3-102">SYNOPSIS</span></span>
<span data-ttu-id="416f3-103">Egy engedélyezési szabály részleteit kapja meg, vagy megkapja az engedélyezési szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="416f3-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="416f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="416f3-104">SYNTAX</span></span>

### <span data-ttu-id="416f3-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="416f3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="416f3-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="416f3-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="416f3-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="416f3-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="416f3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="416f3-108">DESCRIPTION</span></span>
<span data-ttu-id="416f3-109">A Get-AzEventHubAuthorizationRule parancsmag egy engedélyezési szabály részleteit vagy egy adott esemény központhoz tartozó összes engedélyezési szabály listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="416f3-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="416f3-110">Ha egy engedélyezési szabály neve meg van határozva, az adott egyetlen engedélyezési szabály részleteit adja vissza a függvény.</span><span class="sxs-lookup"><span data-stu-id="416f3-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="416f3-111">Ha egy engedélyezési szabály neve nem jelenik meg, akkor a megadott esemény központjának minden engedélyezési szabályát a program visszaadja.</span><span class="sxs-lookup"><span data-stu-id="416f3-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="416f3-112">Ha (katasztrófa-helyreállítási) alias név, a rendszer az aliashoz konfigurált névtér engedélyezési szabályának részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="416f3-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="416f3-113">Példák</span><span class="sxs-lookup"><span data-stu-id="416f3-113">EXAMPLES</span></span>

### <span data-ttu-id="416f3-114">1. példa: AuthorizationRule a névtérhez</span><span class="sxs-lookup"><span data-stu-id="416f3-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="416f3-115">Az engedélyezési szabály \` MyAuthRuleName a \` névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="416f3-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="416f3-116">2. példa: AuthorizationRules a névtérhez</span><span class="sxs-lookup"><span data-stu-id="416f3-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="416f3-117">A névtér MyNamespaceName az összes engedélyezési szabály listáját kapja \` \` .</span><span class="sxs-lookup"><span data-stu-id="416f3-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="416f3-118">3. példa: AuthorizationRule for EventHub</span><span class="sxs-lookup"><span data-stu-id="416f3-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="416f3-119">Az \` MyAuthRuleName az \` esemény központi \` MyEventHubName kapja \` , amelyet a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="416f3-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="416f3-120">4. példa: AuthorizationRules for EventHub</span><span class="sxs-lookup"><span data-stu-id="416f3-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="416f3-121">A lista engedélyezési szabályait kapja meg az esemény központi \` MyEventHubName \` , amelyet a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="416f3-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="416f3-122">5. példa: AuthorizationRule aliashoz (GeoRecovery-konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="416f3-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="416f3-123">Az engedélyezési szabály \` MyAuthRuleName a \` névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="416f3-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="416f3-124">6. példa: AuthorizationRules aliashoz (GeoRecovery-konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="416f3-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="416f3-125">Beolvassa az összes engedélyezési szabály \` MyAuthRuleName listáját \` a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="416f3-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="416f3-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="416f3-126">PARAMETERS</span></span>

### <span data-ttu-id="416f3-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="416f3-127">-AliasName</span></span>
<span data-ttu-id="416f3-128">Alias neve</span><span class="sxs-lookup"><span data-stu-id="416f3-128">Alias Name</span></span>

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

### <span data-ttu-id="416f3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="416f3-129">-DefaultProfile</span></span>
<span data-ttu-id="416f3-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="416f3-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="416f3-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="416f3-131">-Eventhub</span></span>
<span data-ttu-id="416f3-132">Eventhub neve</span><span class="sxs-lookup"><span data-stu-id="416f3-132">Eventhub Name</span></span>

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

### <span data-ttu-id="416f3-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="416f3-133">-Name</span></span>
<span data-ttu-id="416f3-134">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="416f3-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="416f3-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="416f3-135">-Namespace</span></span>
<span data-ttu-id="416f3-136">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="416f3-136">Namespace Name</span></span>

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

### <span data-ttu-id="416f3-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="416f3-137">-ResourceGroupName</span></span>
<span data-ttu-id="416f3-138">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="416f3-138">Resource Group Name</span></span>

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

### <span data-ttu-id="416f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="416f3-139">CommonParameters</span></span>
<span data-ttu-id="416f3-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="416f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="416f3-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="416f3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="416f3-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="416f3-142">INPUTS</span></span>

### <span data-ttu-id="416f3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="416f3-143">System.String</span></span>

## <span data-ttu-id="416f3-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="416f3-144">OUTPUTS</span></span>

### <span data-ttu-id="416f3-145">Microsoft. Azure. Command. EventHub. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="416f3-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="416f3-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="416f3-146">NOTES</span></span>

## <span data-ttu-id="416f3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="416f3-147">RELATED LINKS</span></span>
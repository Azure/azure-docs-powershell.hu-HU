---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376695"
---
# <span data-ttu-id="82c8e-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="82c8e-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="82c8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="82c8e-103">Lekérte egy engedélyezési szabály részleteit, vagy lekérte az engedélyezési szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="82c8e-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="82c8e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82c8e-104">SYNTAX</span></span>

### <span data-ttu-id="82c8e-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82c8e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82c8e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="82c8e-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82c8e-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="82c8e-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c8e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82c8e-108">DESCRIPTION</span></span>
<span data-ttu-id="82c8e-109">A Get-AzEventHubAuthorizationRule parancsmag vagy egy engedélyezési szabály adatait, vagy egy adott eseményközpont összes engedélyezési szabályának listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="82c8e-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="82c8e-110">Ha meg van biztosítanak egy engedélyezési szabály nevét, a rendszer visszaadja az adott egyszeres engedélyezési szabály részleteit.</span><span class="sxs-lookup"><span data-stu-id="82c8e-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="82c8e-111">Ha nem adja meg egy engedélyezési szabály nevét, a rendszer visszaadja a megadott eseményközpont összes engedélyezési szabályának listáját.</span><span class="sxs-lookup"><span data-stu-id="82c8e-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="82c8e-112">Ha a (Katasztrófavédelem) alias neve meg van állítva, a rendszer visszaadja a konfigurált Alias névterének engedélyezési szabályának részleteit.</span><span class="sxs-lookup"><span data-stu-id="82c8e-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="82c8e-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82c8e-113">EXAMPLES</span></span>

### <span data-ttu-id="82c8e-114">1. példa: A névtér engedélyezésiszabálya</span><span class="sxs-lookup"><span data-stu-id="82c8e-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="82c8e-115">Beveszi a MyAuthRuleName engedélyezési szabályt a \` \` \` MyNamespaceName nevű \` névtérbe.</span><span class="sxs-lookup"><span data-stu-id="82c8e-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="82c8e-116">2. példa: A névtér engedélyezésiszabályai</span><span class="sxs-lookup"><span data-stu-id="82c8e-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="82c8e-117">A MyNamespaceName névterében található összes engedélyezési szabály \` listáját \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="82c8e-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="82c8e-118">3. példa: AuthorizationRule for EventHub</span><span class="sxs-lookup"><span data-stu-id="82c8e-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="82c8e-119">A MyAuthRuleName engedélyezési szabályt a MyEventHubName eseményközpontban kapja meg, amelynek hatóköre a \` \` \` \` \` MyNamespaceName névtér. \`</span><span class="sxs-lookup"><span data-stu-id="82c8e-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="82c8e-120">4. példa: AuthorizationRules for EventHub</span><span class="sxs-lookup"><span data-stu-id="82c8e-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="82c8e-121">Listaengedélyezési szabályokat kap az Event Hub MyEventHubName eseményközpontban, amelynek hatóköre a \` \` MyNamespaceName nevű névtér \` szerint van megszűrve. \`</span><span class="sxs-lookup"><span data-stu-id="82c8e-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="82c8e-122">5. példa: Alias engedélyezésiszabálya (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="82c8e-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="82c8e-123">Beveszi a MyAuthRuleName engedélyezési szabályt a \` \` \` MyNamespaceName nevű \` névtérbe.</span><span class="sxs-lookup"><span data-stu-id="82c8e-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="82c8e-124">6. példa: Alias engedélyezésiszabályai (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="82c8e-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="82c8e-125">A \` MyNamespaceName nevű névtér myAuthRuleName engedélyezési \` \` szabályának listáját \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="82c8e-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="82c8e-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82c8e-126">PARAMETERS</span></span>

### <span data-ttu-id="82c8e-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="82c8e-127">-AliasName</span></span>
<span data-ttu-id="82c8e-128">Alias Name</span><span class="sxs-lookup"><span data-stu-id="82c8e-128">Alias Name</span></span>

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

### <span data-ttu-id="82c8e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c8e-129">-DefaultProfile</span></span>
<span data-ttu-id="82c8e-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82c8e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82c8e-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="82c8e-131">-Eventhub</span></span>
<span data-ttu-id="82c8e-132">Eventhub Name</span><span class="sxs-lookup"><span data-stu-id="82c8e-132">Eventhub Name</span></span>

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

### <span data-ttu-id="82c8e-133">-Name</span><span class="sxs-lookup"><span data-stu-id="82c8e-133">-Name</span></span>
<span data-ttu-id="82c8e-134">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="82c8e-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="82c8e-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="82c8e-135">-Namespace</span></span>
<span data-ttu-id="82c8e-136">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="82c8e-136">Namespace Name</span></span>

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

### <span data-ttu-id="82c8e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c8e-137">-ResourceGroupName</span></span>
<span data-ttu-id="82c8e-138">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="82c8e-138">Resource Group Name</span></span>

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

### <span data-ttu-id="82c8e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c8e-139">CommonParameters</span></span>
<span data-ttu-id="82c8e-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c8e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c8e-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c8e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c8e-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82c8e-142">INPUTS</span></span>

### <span data-ttu-id="82c8e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="82c8e-143">System.String</span></span>

## <span data-ttu-id="82c8e-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82c8e-144">OUTPUTS</span></span>

### <span data-ttu-id="82c8e-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="82c8e-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="82c8e-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82c8e-146">NOTES</span></span>

## <span data-ttu-id="82c8e-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82c8e-147">RELATED LINKS</span></span>

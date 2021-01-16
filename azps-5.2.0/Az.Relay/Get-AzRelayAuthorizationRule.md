---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357193"
---
# <span data-ttu-id="7774d-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7774d-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="7774d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7774d-102">SYNOPSIS</span></span>
<span data-ttu-id="7774d-103">Egy adott továbbítási entitáshoz (Namespace/WcfRelay/HybridConnection) megadott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7774d-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="7774d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7774d-104">SYNTAX</span></span>

### <span data-ttu-id="7774d-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7774d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7774d-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7774d-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7774d-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7774d-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7774d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7774d-108">DESCRIPTION</span></span>
<span data-ttu-id="7774d-109">A **Get-AzRelayAuthorizationRule** parancsmag megkapja a megadott engedélyezési szabály leírását a megadott továbbítási entitásban (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="7774d-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="7774d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7774d-110">EXAMPLES</span></span>

### <span data-ttu-id="7774d-111">1. példa: Namespace</span><span class="sxs-lookup"><span data-stu-id="7774d-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="7774d-112">Egy megadott névtér engedélyezési szabályának leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7774d-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="7774d-113">2. példa: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7774d-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="7774d-114">Visszaadja egy adott WcfRelay engedélyezési szabályának megadott leírását.</span><span class="sxs-lookup"><span data-stu-id="7774d-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="7774d-115">3. példa: Hibrid összekapcsolás</span><span class="sxs-lookup"><span data-stu-id="7774d-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="7774d-116">Egy adott HybridConnection engedélyezési szabályának megadott leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7774d-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="7774d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7774d-117">PARAMETERS</span></span>

### <span data-ttu-id="7774d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7774d-118">-DefaultProfile</span></span>
<span data-ttu-id="7774d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7774d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7774d-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="7774d-120">-HybridConnection</span></span>
<span data-ttu-id="7774d-121">Hibrid összekapcsolás neve.</span><span class="sxs-lookup"><span data-stu-id="7774d-121">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7774d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7774d-122">-Name</span></span>
<span data-ttu-id="7774d-123">AuthorizationRule Name (EngedélyezésiSzabály neve) stb.</span><span class="sxs-lookup"><span data-stu-id="7774d-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7774d-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7774d-124">-Namespace</span></span>
<span data-ttu-id="7774d-125">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="7774d-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7774d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7774d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7774d-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7774d-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="7774d-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7774d-128">-WcfRelay</span></span>
<span data-ttu-id="7774d-129">WcfRelay Name.</span><span class="sxs-lookup"><span data-stu-id="7774d-129">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7774d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7774d-130">CommonParameters</span></span>
<span data-ttu-id="7774d-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7774d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7774d-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7774d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7774d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7774d-133">INPUTS</span></span>

### <span data-ttu-id="7774d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7774d-134">System.String</span></span>

## <span data-ttu-id="7774d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7774d-135">OUTPUTS</span></span>

### <span data-ttu-id="7774d-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7774d-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7774d-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7774d-137">NOTES</span></span>

## <span data-ttu-id="7774d-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7774d-138">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 7fa9cb54a6790a473be419dd934927ed26783d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921218"
---
# <span data-ttu-id="ca9bd-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca9bd-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="ca9bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9bd-103">Az aktuális Azure-előfizetés névterének Event Hubs NetworkruleSet-ének adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ca9bd-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ca9bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ca9bd-104">SYNTAX</span></span>

### <span data-ttu-id="ca9bd-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca9bd-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca9bd-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="ca9bd-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca9bd-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca9bd-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca9bd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ca9bd-108">DESCRIPTION</span></span>
<span data-ttu-id="ca9bd-109">Az aktuális Azure-előfizetés névterének Event Hubs NetworkruleSet-ének adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ca9bd-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ca9bd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ca9bd-110">EXAMPLES</span></span>

### <span data-ttu-id="ca9bd-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ca9bd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="ca9bd-112">Az Event Hubs NetworkruleSet névtérről a ResourceGroup és a Namespace paramétereit használva olvashatja le a részleteket.</span><span class="sxs-lookup"><span data-stu-id="ca9bd-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="ca9bd-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ca9bd-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="ca9bd-114">Az aktuális előfizetésben lévő Namespace segítségével lekérte az Event Hubs NetworkruleSet névterének részleteit.</span><span class="sxs-lookup"><span data-stu-id="ca9bd-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="ca9bd-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="ca9bd-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="ca9bd-116">Az Event Hubs NetworkruleSet névtérről, más névtér erőforrás-azonosítójával</span><span class="sxs-lookup"><span data-stu-id="ca9bd-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="ca9bd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca9bd-117">PARAMETERS</span></span>

### <span data-ttu-id="ca9bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9bd-118">-DefaultProfile</span></span>
<span data-ttu-id="ca9bd-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca9bd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca9bd-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ca9bd-120">-Namespace</span></span>
<span data-ttu-id="ca9bd-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ca9bd-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9bd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9bd-122">-ResourceGroupName</span></span>
<span data-ttu-id="ca9bd-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ca9bd-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9bd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca9bd-124">-ResourceId</span></span>
<span data-ttu-id="ca9bd-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="ca9bd-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9bd-126">CommonParameters</span></span>
<span data-ttu-id="ca9bd-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca9bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ca9bd-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9bd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9bd-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca9bd-129">INPUTS</span></span>

### <span data-ttu-id="ca9bd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ca9bd-130">System.String</span></span>

## <span data-ttu-id="ca9bd-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca9bd-131">OUTPUTS</span></span>

### <span data-ttu-id="ca9bd-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ca9bd-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ca9bd-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ca9bd-133">NOTES</span></span>

## <span data-ttu-id="ca9bd-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca9bd-134">RELATED LINKS</span></span>
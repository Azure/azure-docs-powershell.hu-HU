---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153163"
---
# <span data-ttu-id="2c346-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c346-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="2c346-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c346-102">SYNOPSIS</span></span>
<span data-ttu-id="2c346-103">Az aktuális Azure-előfizetés névterének Event Hubs NetworkruleSet-ének adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2c346-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="2c346-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2c346-104">SYNTAX</span></span>

### <span data-ttu-id="2c346-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c346-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c346-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2c346-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c346-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c346-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c346-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2c346-108">DESCRIPTION</span></span>
<span data-ttu-id="2c346-109">Az aktuális Azure-előfizetés névterének Eseményközpontok NetworkruleSet-ének adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2c346-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="2c346-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2c346-110">EXAMPLES</span></span>

### <span data-ttu-id="2c346-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2c346-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="2c346-112">Az Event Hubs NetworkruleSet névtérről az ResourceGroup és a Namespace paraméter használatával olvashatja le a részleteket.</span><span class="sxs-lookup"><span data-stu-id="2c346-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="2c346-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2c346-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="2c346-114">Az aktuális előfizetésben lévő Namespace segítségével lekérte az Event Hubs NetworkruleSet névterének részleteit.</span><span class="sxs-lookup"><span data-stu-id="2c346-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="2c346-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="2c346-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="2c346-116">Az Event Hubs NetworkruleSet névtérről, más névtér erőforrás-azonosítójával</span><span class="sxs-lookup"><span data-stu-id="2c346-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="2c346-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c346-117">PARAMETERS</span></span>

### <span data-ttu-id="2c346-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c346-118">-DefaultProfile</span></span>
<span data-ttu-id="2c346-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c346-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c346-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2c346-120">-Namespace</span></span>
<span data-ttu-id="2c346-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="2c346-121">Namespace Name</span></span>

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

### <span data-ttu-id="2c346-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c346-122">-ResourceGroupName</span></span>
<span data-ttu-id="2c346-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2c346-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2c346-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c346-124">-ResourceId</span></span>
<span data-ttu-id="2c346-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="2c346-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2c346-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c346-126">CommonParameters</span></span>
<span data-ttu-id="2c346-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c346-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2c346-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c346-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c346-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c346-129">INPUTS</span></span>

### <span data-ttu-id="2c346-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2c346-130">System.String</span></span>

## <span data-ttu-id="2c346-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c346-131">OUTPUTS</span></span>

### <span data-ttu-id="2c346-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="2c346-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="2c346-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2c346-133">NOTES</span></span>

## <span data-ttu-id="2c346-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c346-134">RELATED LINKS</span></span>
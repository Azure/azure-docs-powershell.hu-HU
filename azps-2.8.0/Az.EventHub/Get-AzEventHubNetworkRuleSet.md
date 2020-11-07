---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: cbac380f317025154f25c3c4dfe449832c864741
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666489"
---
# <span data-ttu-id="d6081-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6081-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="d6081-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6081-102">SYNOPSIS</span></span>
<span data-ttu-id="d6081-103">Az aktuális Azure-előfizetésben az esemény-hubok NetworkruleSet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d6081-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d6081-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6081-104">SYNTAX</span></span>

### <span data-ttu-id="d6081-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6081-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6081-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d6081-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6081-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6081-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6081-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6081-108">DESCRIPTION</span></span>
<span data-ttu-id="d6081-109">Az aktuális Azure-előfizetésben az esemény-hubok NetworkruleSet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d6081-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d6081-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d6081-110">EXAMPLES</span></span>

### <span data-ttu-id="d6081-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d6081-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="d6081-112">A ResourceGroup és a NAMESPACE paraméterrel megtudhatja, hogy miként érheti el az esemény-hubok NetworkruleSet.</span><span class="sxs-lookup"><span data-stu-id="d6081-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="d6081-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d6081-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="d6081-114">Az esemény-hubok NetworkruleSet az aktuális előfizetésben található névtérrel megtudhatja.</span><span class="sxs-lookup"><span data-stu-id="d6081-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="d6081-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="d6081-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="d6081-116">Az esemény-hubok NetworkruleSet a többi névtér erőforrás-azonosítójának használatával</span><span class="sxs-lookup"><span data-stu-id="d6081-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="d6081-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6081-117">PARAMETERS</span></span>

### <span data-ttu-id="d6081-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6081-118">-DefaultProfile</span></span>
<span data-ttu-id="d6081-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6081-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6081-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d6081-120">-Namespace</span></span>
<span data-ttu-id="d6081-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="d6081-121">Namespace Name</span></span>

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

### <span data-ttu-id="d6081-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6081-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6081-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d6081-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d6081-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6081-124">-ResourceId</span></span>
<span data-ttu-id="d6081-125">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="d6081-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="d6081-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6081-126">CommonParameters</span></span>
<span data-ttu-id="d6081-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6081-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d6081-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6081-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6081-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6081-129">INPUTS</span></span>

### <span data-ttu-id="d6081-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d6081-130">System.String</span></span>

## <span data-ttu-id="d6081-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6081-131">OUTPUTS</span></span>

### <span data-ttu-id="d6081-132">Microsoft. Azure. Command. EventHub. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d6081-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="d6081-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6081-133">NOTES</span></span>

## <span data-ttu-id="d6081-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6081-134">RELATED LINKS</span></span>
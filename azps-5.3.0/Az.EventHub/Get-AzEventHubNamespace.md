---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: ba2209f7b58951bdc52976fb3cbab10fa15da98a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387041"
---
# <span data-ttu-id="11add-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="11add-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="11add-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11add-102">SYNOPSIS</span></span>
<span data-ttu-id="11add-103">Lekérte egy Eseményközpont névterének adatait, vagy lekérte az aktuális Azure-előfizetés összes Event Hubs névterét.</span><span class="sxs-lookup"><span data-stu-id="11add-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="11add-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11add-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11add-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11add-105">DESCRIPTION</span></span>
<span data-ttu-id="11add-106">A Get-AzEventHubNamespace parancsmag vagy egy megadott Event Hubs névtér adatait, vagy az aktuális Azure-előfizetés összes Eseményközpont névterének listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="11add-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="11add-107">Ha meg van biztosítanak egy névteret, a visszaadott érték egyetlen Eseményközpont névterének adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="11add-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="11add-108">Ha a névtér neve nem szerepel a listában, a visszaadott névterek listája lesz az eredmény.</span><span class="sxs-lookup"><span data-stu-id="11add-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="11add-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11add-109">EXAMPLES</span></span>

### <span data-ttu-id="11add-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="11add-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="11add-111">A MyResourceGroupName erőforráscsoportban a \` \` \` MyNamespaceName névtér adatait \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="11add-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="11add-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11add-112">PARAMETERS</span></span>

### <span data-ttu-id="11add-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11add-113">-DefaultProfile</span></span>
<span data-ttu-id="11add-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11add-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11add-115">-Name</span><span class="sxs-lookup"><span data-stu-id="11add-115">-Name</span></span>
<span data-ttu-id="11add-116">EventHub Namespace Name</span><span class="sxs-lookup"><span data-stu-id="11add-116">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11add-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11add-117">-ResourceGroupName</span></span>
<span data-ttu-id="11add-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="11add-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11add-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11add-119">CommonParameters</span></span>
<span data-ttu-id="11add-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11add-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11add-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11add-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11add-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11add-122">INPUTS</span></span>

### <span data-ttu-id="11add-123">System.String</span><span class="sxs-lookup"><span data-stu-id="11add-123">System.String</span></span>

## <span data-ttu-id="11add-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11add-124">OUTPUTS</span></span>

### <span data-ttu-id="11add-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="11add-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="11add-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11add-126">NOTES</span></span>

## <span data-ttu-id="11add-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11add-127">RELATED LINKS</span></span>

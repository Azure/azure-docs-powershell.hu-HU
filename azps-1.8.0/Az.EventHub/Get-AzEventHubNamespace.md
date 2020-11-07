---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: c39a85fe148461d5daa680a62b5cfd09b4a3e4e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670846"
---
# <span data-ttu-id="10b33-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="10b33-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="10b33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10b33-102">SYNOPSIS</span></span>
<span data-ttu-id="10b33-103">Beolvassa az esemény-hubok névterének részleteit, vagy az aktuális Azure-előfizetésből az összes esemény-hubok névterének listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="10b33-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="10b33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10b33-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10b33-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10b33-105">DESCRIPTION</span></span>
<span data-ttu-id="10b33-106">A Get-AzEventHubNamespace parancsmag az aktuális Azure-előfizetésben lévő adott esemény-hubok névterének részleteit vagy az összes esemény hubok névterét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="10b33-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="10b33-107">Ha a névtér neve meg van határozva, az egyetlen esemény-hubok névtér részleteit adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="10b33-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="10b33-108">Ha a névtér neve nincs megadva, a program a névterek listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="10b33-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="10b33-109">Példák</span><span class="sxs-lookup"><span data-stu-id="10b33-109">EXAMPLES</span></span>

### <span data-ttu-id="10b33-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="10b33-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="10b33-111">A Namespace MyNamespaceName részleteit \` kapja \` meg az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="10b33-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="10b33-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10b33-112">PARAMETERS</span></span>

### <span data-ttu-id="10b33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b33-113">-DefaultProfile</span></span>
<span data-ttu-id="10b33-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10b33-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10b33-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="10b33-115">-Name</span></span>
<span data-ttu-id="10b33-116">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="10b33-116">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="10b33-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10b33-117">-ResourceGroupName</span></span>
<span data-ttu-id="10b33-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="10b33-118">Resource Group Name</span></span>

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

### <span data-ttu-id="10b33-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b33-119">CommonParameters</span></span>
<span data-ttu-id="10b33-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10b33-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b33-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b33-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b33-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b33-122">INPUTS</span></span>

### <span data-ttu-id="10b33-123">System. String</span><span class="sxs-lookup"><span data-stu-id="10b33-123">System.String</span></span>

## <span data-ttu-id="10b33-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b33-124">OUTPUTS</span></span>

### <span data-ttu-id="10b33-125">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="10b33-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="10b33-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10b33-126">NOTES</span></span>

## <span data-ttu-id="10b33-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10b33-127">RELATED LINKS</span></span>

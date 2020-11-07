---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: fe0991296ad5f2dc8be89c92117e74c4231b495c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679721"
---
# <span data-ttu-id="161b5-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="161b5-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="161b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="161b5-102">SYNOPSIS</span></span>
<span data-ttu-id="161b5-103">A megadott továbbítási névtér leírását kapja az erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="161b5-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="161b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="161b5-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="161b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="161b5-105">DESCRIPTION</span></span>
<span data-ttu-id="161b5-106">A **Get-AzureRmRelayNamespace** parancsmag leírását kapja a megadott továbbítási névtérhez az erőforráscsoporten belül.</span><span class="sxs-lookup"><span data-stu-id="161b5-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="161b5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="161b5-107">EXAMPLES</span></span>

### <span data-ttu-id="161b5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="161b5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="161b5-109">A megadott továbbítási névtér leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="161b5-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="161b5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="161b5-110">PARAMETERS</span></span>

### <span data-ttu-id="161b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="161b5-111">-DefaultProfile</span></span>
<span data-ttu-id="161b5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="161b5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161b5-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="161b5-113">-Name</span></span>
<span data-ttu-id="161b5-114">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="161b5-114">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="161b5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="161b5-115">-ResourceGroupName</span></span>
<span data-ttu-id="161b5-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="161b5-116">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="161b5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="161b5-117">CommonParameters</span></span>
<span data-ttu-id="161b5-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="161b5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="161b5-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="161b5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="161b5-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="161b5-120">INPUTS</span></span>

### <span data-ttu-id="161b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="161b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="161b5-122">System. String</span><span class="sxs-lookup"><span data-stu-id="161b5-122">System.String</span></span>

### <span data-ttu-id="161b5-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="161b5-123">-Name</span></span>
 <span data-ttu-id="161b5-124">System. String</span><span class="sxs-lookup"><span data-stu-id="161b5-124">System.String</span></span>

## <span data-ttu-id="161b5-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="161b5-125">OUTPUTS</span></span>

### <span data-ttu-id="161b5-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Relay. models. RelayNamespaceAttributes, Microsoft. Azure. Command. Relay, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="161b5-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="161b5-127">ProvisioningState: sikeres CreatedAt: 4/12/2017 12:38:47 AM UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId: 854d368f-1828-428f-8f3c-f2affa9b2f7d: testnamespace-relay1: West US Tags: {[Tag1, Tag1Value]} ID: TestNameSpace-Relay1/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1</span><span class="sxs-lookup"><span data-stu-id="161b5-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="161b5-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="161b5-128">NOTES</span></span>

## <span data-ttu-id="161b5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="161b5-129">RELATED LINKS</span></span>


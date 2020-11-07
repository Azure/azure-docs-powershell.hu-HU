---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: 3ef4934ce98b48051f052e2644dc7707fe89650f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669520"
---
# <span data-ttu-id="13d26-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="13d26-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="13d26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13d26-102">SYNOPSIS</span></span>
<span data-ttu-id="13d26-103">A megadott továbbítási névtér leírását kapja az erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="13d26-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="13d26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13d26-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13d26-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13d26-105">DESCRIPTION</span></span>
<span data-ttu-id="13d26-106">A **Get-AzRelayNamespace** parancsmag leírását kapja a megadott továbbítási névtérhez az erőforráscsoporten belül.</span><span class="sxs-lookup"><span data-stu-id="13d26-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="13d26-107">Példák</span><span class="sxs-lookup"><span data-stu-id="13d26-107">EXAMPLES</span></span>

### <span data-ttu-id="13d26-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13d26-108">Example 1</span></span>
```
PS C:\> Get-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="13d26-109">A megadott továbbítási névtér leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="13d26-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="13d26-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13d26-110">PARAMETERS</span></span>

### <span data-ttu-id="13d26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d26-111">-DefaultProfile</span></span>
<span data-ttu-id="13d26-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13d26-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13d26-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13d26-113">-Name</span></span>
<span data-ttu-id="13d26-114">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="13d26-114">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13d26-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d26-115">-ResourceGroupName</span></span>
<span data-ttu-id="13d26-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="13d26-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="13d26-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d26-117">CommonParameters</span></span>
<span data-ttu-id="13d26-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13d26-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d26-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13d26-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d26-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d26-120">INPUTS</span></span>

### <span data-ttu-id="13d26-121">System. String</span><span class="sxs-lookup"><span data-stu-id="13d26-121">System.String</span></span>

## <span data-ttu-id="13d26-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d26-122">OUTPUTS</span></span>

### <span data-ttu-id="13d26-123">Microsoft. Azure. Command. Relay. models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="13d26-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="13d26-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13d26-124">NOTES</span></span>

## <span data-ttu-id="13d26-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13d26-125">RELATED LINKS</span></span>

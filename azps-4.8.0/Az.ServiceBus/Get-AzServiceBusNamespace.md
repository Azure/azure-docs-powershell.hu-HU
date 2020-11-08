---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 359ff0ce6de0c017d1ea2a65adc1d4573e45c17f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017625"
---
# <span data-ttu-id="3479b-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="3479b-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="3479b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3479b-102">SYNOPSIS</span></span>
<span data-ttu-id="3479b-103">A megadott szolgáltatási busz névterének leírását adja meg az erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="3479b-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="3479b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3479b-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3479b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3479b-105">DESCRIPTION</span></span>
<span data-ttu-id="3479b-106">A **Get-AzServiceBusNamespace** parancsmag leírását kapja a megadott szolgáltatási busz névtérhez az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="3479b-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="3479b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3479b-107">EXAMPLES</span></span>

### <span data-ttu-id="3479b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3479b-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="3479b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3479b-109">PARAMETERS</span></span>

### <span data-ttu-id="3479b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3479b-110">-DefaultProfile</span></span>
<span data-ttu-id="3479b-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3479b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3479b-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3479b-112">-Name</span></span>
<span data-ttu-id="3479b-113">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="3479b-113">Namespace Name.</span></span>

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

### <span data-ttu-id="3479b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3479b-114">-ResourceGroupName</span></span>
<span data-ttu-id="3479b-115">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3479b-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3479b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3479b-116">CommonParameters</span></span>
<span data-ttu-id="3479b-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3479b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3479b-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3479b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3479b-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3479b-119">INPUTS</span></span>

### <span data-ttu-id="3479b-120">System. String</span><span class="sxs-lookup"><span data-stu-id="3479b-120">System.String</span></span>

## <span data-ttu-id="3479b-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3479b-121">OUTPUTS</span></span>

### <span data-ttu-id="3479b-122">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3479b-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3479b-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3479b-123">NOTES</span></span>

## <span data-ttu-id="3479b-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3479b-124">RELATED LINKS</span></span>

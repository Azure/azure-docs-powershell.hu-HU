---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672194"
---
# <span data-ttu-id="0c67f-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="0c67f-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="0c67f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c67f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c67f-103">A megadott szolgáltatási busz névterének leírását adja meg az erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="0c67f-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c67f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c67f-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c67f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c67f-105">DESCRIPTION</span></span>
<span data-ttu-id="0c67f-106">A **Get-AzureRmServiceBusNamespace** parancsmag leírását kapja a megadott szolgáltatási busz névtérhez az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="0c67f-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="0c67f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0c67f-107">EXAMPLES</span></span>

### <span data-ttu-id="0c67f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0c67f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="0c67f-109">A megadott szolgáltatási busz névterének leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c67f-109">Returns a description of the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0c67f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c67f-110">PARAMETERS</span></span>

### <span data-ttu-id="0c67f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c67f-111">-DefaultProfile</span></span>
<span data-ttu-id="0c67f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c67f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c67f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c67f-113">-Name</span></span>
<span data-ttu-id="0c67f-114">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="0c67f-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c67f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c67f-115">-ResourceGroupName</span></span>
<span data-ttu-id="0c67f-116">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0c67f-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c67f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c67f-117">CommonParameters</span></span>
<span data-ttu-id="0c67f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c67f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c67f-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c67f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c67f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c67f-120">INPUTS</span></span>

### <span data-ttu-id="0c67f-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0c67f-121">-ResourceGroup</span></span>
<span data-ttu-id="0c67f-122">System. String</span><span class="sxs-lookup"><span data-stu-id="0c67f-122">System.String</span></span>

### <span data-ttu-id="0c67f-123">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0c67f-123">-NamespaceName</span></span>
 <span data-ttu-id="0c67f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0c67f-124">System.String</span></span>

## <span data-ttu-id="0c67f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c67f-125">OUTPUTS</span></span>

### <span data-ttu-id="0c67f-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. NamespaceAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0c67f-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0c67f-127">Név: SB-Example1 azonosító:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 hely: Nyugat-amerikai SKU: név: standard, kapacitás: 1, Tier: standard ProvisioningState: örökölt állapot: Active CreatedAt: 1/20/2017 1:40:01 AM UpdatedAt: 1/20/2017 1:40:24 AM ServiceBusEndpoint: https://SB-Example1.servicebus.windows.net:443/ enabled: true</span><span class="sxs-lookup"><span data-stu-id="0c67f-127">Name               : SB-Example1 Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 Location           : West US Sku                : Name : Standard , Capacity : 1 , Tier : Standard ProvisioningState  : Succeeded Status             : Active CreatedAt          : 1/20/2017 1:40:01 AM UpdatedAt          : 1/20/2017 1:40:24 AM ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/ Enabled            : True</span></span>

## <span data-ttu-id="0c67f-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c67f-128">NOTES</span></span>
## <span data-ttu-id="0c67f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c67f-129">RELATED LINKS</span></span>

## <span data-ttu-id="0c67f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c67f-130">RELATED LINKS</span></span>


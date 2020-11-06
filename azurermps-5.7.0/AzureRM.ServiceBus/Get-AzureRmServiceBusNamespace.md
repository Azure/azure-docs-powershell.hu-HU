---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2584630c8c1d0981f354ffc920af4f8ed9ff979f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494340"
---
# <span data-ttu-id="b4471-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="b4471-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="b4471-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4471-102">SYNOPSIS</span></span>
<span data-ttu-id="b4471-103">A megadott szolgáltatási busz névterének leírását adja meg az erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="b4471-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4471-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4471-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4471-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4471-105">DESCRIPTION</span></span>
<span data-ttu-id="b4471-106">A **Get-AzureRmServiceBusNamespace** parancsmag leírását kapja a megadott szolgáltatási busz névtérhez az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="b4471-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="b4471-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b4471-107">EXAMPLES</span></span>

### <span data-ttu-id="b4471-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b4471-108">Example 1</span></span>

```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/

```

## <span data-ttu-id="b4471-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4471-109">PARAMETERS</span></span>

### <span data-ttu-id="b4471-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4471-110">-DefaultProfile</span></span>
<span data-ttu-id="b4471-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4471-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4471-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4471-112">-Name</span></span>
<span data-ttu-id="b4471-113">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="b4471-113">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4471-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4471-114">-ResourceGroupName</span></span>
<span data-ttu-id="b4471-115">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b4471-115">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4471-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4471-116">CommonParameters</span></span>
<span data-ttu-id="b4471-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4471-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4471-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4471-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4471-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4471-119">INPUTS</span></span>

### <span data-ttu-id="b4471-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b4471-120">-ResourceGroup</span></span>
<span data-ttu-id="b4471-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b4471-121">System.String</span></span>

### <span data-ttu-id="b4471-122">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b4471-122">-NamespaceName</span></span>
 <span data-ttu-id="b4471-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b4471-123">System.String</span></span>

## <span data-ttu-id="b4471-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4471-124">OUTPUTS</span></span>

### <span data-ttu-id="b4471-125">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b4471-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b4471-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4471-126">NOTES</span></span>

## <span data-ttu-id="b4471-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4471-127">RELATED LINKS</span></span>


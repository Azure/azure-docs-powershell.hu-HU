---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 37d142947c09c211c947f3bd80455a812f96844f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494916"
---
# <span data-ttu-id="db8a6-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="db8a6-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="db8a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="db8a6-103">A megadott szolgáltatási busz névterének leírását adja meg az erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="db8a6-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db8a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db8a6-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db8a6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db8a6-105">DESCRIPTION</span></span>
<span data-ttu-id="db8a6-106">A **Get-AzureRmServiceBusNamespace** parancsmag leírását kapja a megadott szolgáltatási busz névtérhez az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="db8a6-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="db8a6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="db8a6-107">EXAMPLES</span></span>

### <span data-ttu-id="db8a6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="db8a6-108">Example 1</span></span>

```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="db8a6-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db8a6-109">PARAMETERS</span></span>

### <span data-ttu-id="db8a6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db8a6-110">-DefaultProfile</span></span>
<span data-ttu-id="db8a6-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db8a6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db8a6-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db8a6-112">-Name</span></span>
<span data-ttu-id="db8a6-113">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="db8a6-113">Namespace Name.</span></span>

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

### <span data-ttu-id="db8a6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db8a6-114">-ResourceGroupName</span></span>
<span data-ttu-id="db8a6-115">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="db8a6-115">The name of the resource group</span></span>

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

### <span data-ttu-id="db8a6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db8a6-116">CommonParameters</span></span>
<span data-ttu-id="db8a6-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db8a6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db8a6-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db8a6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db8a6-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db8a6-119">INPUTS</span></span>

### <span data-ttu-id="db8a6-120">System. String</span><span class="sxs-lookup"><span data-stu-id="db8a6-120">System.String</span></span>

## <span data-ttu-id="db8a6-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db8a6-121">OUTPUTS</span></span>

### <span data-ttu-id="db8a6-122">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="db8a6-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="db8a6-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db8a6-123">NOTES</span></span>

## <span data-ttu-id="db8a6-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db8a6-124">RELATED LINKS</span></span>

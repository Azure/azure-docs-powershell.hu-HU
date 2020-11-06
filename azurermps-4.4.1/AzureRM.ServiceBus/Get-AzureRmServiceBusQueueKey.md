---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 4faca15a0c348ee1011789db5acd227c06ee1b85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501607"
---
# <span data-ttu-id="724fa-101">Get-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="724fa-101">Get-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="724fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="724fa-102">SYNOPSIS</span></span>
<span data-ttu-id="724fa-103">Megkapja az elsődleges és a másodlagos kapcsolat karakterláncát a megadott szolgáltatás busz várólistájához.</span><span class="sxs-lookup"><span data-stu-id="724fa-103">Gets the primary and secondary connection strings for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="724fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="724fa-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueKey [-ResourceGroup] <String> -Namespace <String> -Queue <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="724fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="724fa-105">DESCRIPTION</span></span>
<span data-ttu-id="724fa-106">A **Get-AzureRmServiceBusQueueKey** parancsmag az elsődleges és másodlagos kapcsolati karakterláncokat adja eredményül a megadott szolgáltatás busz várólistájában.</span><span class="sxs-lookup"><span data-stu-id="724fa-106">The **Get-AzureRmServiceBusQueueKey** cmdlet returns the primary and secondary connection strings for the given Service Bus queue.</span></span> 

## <span data-ttu-id="724fa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="724fa-107">EXAMPLES</span></span>

### <span data-ttu-id="724fa-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="724fa-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="724fa-109">Az elsődleges és másodlagos kapcsolati karakterláncokat adja eredményül a megadott Service Bus várólistához.</span><span class="sxs-lookup"><span data-stu-id="724fa-109">Returns the primary and secondary connection strings for the specified Service Bus queue.</span></span>

## <span data-ttu-id="724fa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="724fa-110">PARAMETERS</span></span>

### <span data-ttu-id="724fa-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="724fa-111">-ResourceGroup</span></span>
<span data-ttu-id="724fa-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="724fa-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="724fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724fa-113">-DefaultProfile</span></span>
<span data-ttu-id="724fa-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="724fa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="724fa-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="724fa-115">-Name</span></span>
<span data-ttu-id="724fa-116">A ServiceBus-várólista AuthorizationRule neve.</span><span class="sxs-lookup"><span data-stu-id="724fa-116">ServiceBus Queue AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="724fa-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="724fa-117">-Namespace</span></span>
<span data-ttu-id="724fa-118">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="724fa-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="724fa-119">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="724fa-119">-Queue</span></span>
<span data-ttu-id="724fa-120">ServiceBus-várólista neve</span><span class="sxs-lookup"><span data-stu-id="724fa-120">ServiceBus Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="724fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724fa-121">CommonParameters</span></span>
<span data-ttu-id="724fa-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="724fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724fa-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="724fa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724fa-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="724fa-124">INPUTS</span></span>

### <span data-ttu-id="724fa-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="724fa-125">-ResourceGroup</span></span>
 <span data-ttu-id="724fa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="724fa-126">System.String</span></span>
 

### <span data-ttu-id="724fa-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="724fa-127">-NamespaceName</span></span>
 <span data-ttu-id="724fa-128">System. String</span><span class="sxs-lookup"><span data-stu-id="724fa-128">System.String</span></span>
 

### <span data-ttu-id="724fa-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="724fa-129">-QueueName</span></span>
 <span data-ttu-id="724fa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="724fa-130">System.String</span></span>
 

### <span data-ttu-id="724fa-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="724fa-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="724fa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="724fa-132">System.String</span></span>

## <span data-ttu-id="724fa-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="724fa-133">OUTPUTS</span></span>

### <span data-ttu-id="724fa-134">Microsoft. Azure. Command. ServiceBus. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="724fa-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="724fa-135">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-érték}; EntityPath = SB-Queue_e xampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-érték}; EntityPath = SB-Queue_e xampl1 PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey Value} kulcsnév: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="724fa-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="724fa-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="724fa-136">NOTES</span></span>

## <span data-ttu-id="724fa-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="724fa-137">RELATED LINKS</span></span>


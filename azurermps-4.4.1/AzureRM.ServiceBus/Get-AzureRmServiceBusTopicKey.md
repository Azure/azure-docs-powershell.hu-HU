---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: 24041c299f2f242126f265ad232db3e0c5d526b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503203"
---
# <span data-ttu-id="afe7c-101">Get-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="afe7c-101">Get-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="afe7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="afe7c-102">SYNOPSIS</span></span>
<span data-ttu-id="afe7c-103">Az elsődleges és másodlagos kapcsolati karakterláncokat kapja a Bus témakörben.</span><span class="sxs-lookup"><span data-stu-id="afe7c-103">Gets the primary and secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afe7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="afe7c-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afe7c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="afe7c-105">DESCRIPTION</span></span>
<span data-ttu-id="afe7c-106">A **Get-AzureRmServiceBusTopicKey** parancsmag az elsődleges és másodlagos kapcsolati karakterláncokat adja eredményül a megadott buszvezető-témakörben.</span><span class="sxs-lookup"><span data-stu-id="afe7c-106">The **Get-AzureRmServiceBusTopicKey** cmdlet returns the primary and secondary connection strings for the given Service Bus topic.</span></span>

## <span data-ttu-id="afe7c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="afe7c-107">EXAMPLES</span></span>

### <span data-ttu-id="afe7c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="afe7c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="afe7c-109">Az elsődleges és másodlagos kapcsolati karakterláncokat adja eredményül a megadott Bus-témakörben.</span><span class="sxs-lookup"><span data-stu-id="afe7c-109">Returns the primary and secondary connection strings for the specified Service Bus topic.</span></span>

## <span data-ttu-id="afe7c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="afe7c-110">PARAMETERS</span></span>

### <span data-ttu-id="afe7c-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="afe7c-111">-ResourceGroup</span></span>
<span data-ttu-id="afe7c-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="afe7c-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="afe7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe7c-113">-DefaultProfile</span></span>
<span data-ttu-id="afe7c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="afe7c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afe7c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="afe7c-115">-Name</span></span>
<span data-ttu-id="afe7c-116">A AuthorizationRule témakör neve</span><span class="sxs-lookup"><span data-stu-id="afe7c-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="afe7c-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="afe7c-117">-Namespace</span></span>
<span data-ttu-id="afe7c-118">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="afe7c-118">Namespace Name.</span></span>

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

### <span data-ttu-id="afe7c-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="afe7c-119">-Topic</span></span>
<span data-ttu-id="afe7c-120">A téma neve</span><span class="sxs-lookup"><span data-stu-id="afe7c-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afe7c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe7c-121">CommonParameters</span></span>
<span data-ttu-id="afe7c-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="afe7c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe7c-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afe7c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe7c-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="afe7c-124">INPUTS</span></span>

### <span data-ttu-id="afe7c-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="afe7c-125">-ResourceGroup</span></span>
 <span data-ttu-id="afe7c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="afe7c-126">System.String</span></span>
 

### <span data-ttu-id="afe7c-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="afe7c-127">-NamespaceName</span></span>
 <span data-ttu-id="afe7c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="afe7c-128">System.String</span></span>
 

### <span data-ttu-id="afe7c-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="afe7c-129">-TopicName</span></span>
 <span data-ttu-id="afe7c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="afe7c-130">System.String</span></span>
 

### <span data-ttu-id="afe7c-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="afe7c-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="afe7c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="afe7c-132">System.String</span></span>

## <span data-ttu-id="afe7c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="afe7c-133">OUTPUTS</span></span>

### <span data-ttu-id="afe7c-134">Microsoft. Azure. Command. ServiceBus. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="afe7c-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="afe7c-135">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-érték}; EntityPath = SB-to pic_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-érték}; EntityPath = SB-to pic_exampl1 PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey Value} kulcsnév: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="afe7c-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="afe7c-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="afe7c-136">NOTES</span></span>

## <span data-ttu-id="afe7c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="afe7c-137">RELATED LINKS</span></span>


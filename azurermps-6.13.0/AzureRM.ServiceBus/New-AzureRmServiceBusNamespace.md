---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 532135578418a90e9ce6887602723c2165f28aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499403"
---
# <span data-ttu-id="d4c53-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="d4c53-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="d4c53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4c53-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c53-103">Új szolgáltatási busz névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d4c53-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4c53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4c53-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4c53-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4c53-105">DESCRIPTION</span></span>
<span data-ttu-id="d4c53-106">A **New-AzureRmServiceBusNamespace** parancsmag új szolgáltatási busz névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d4c53-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="d4c53-107">A létrehozás után a névtér-erőforrás jegyzékfájlja nem állandó.</span><span class="sxs-lookup"><span data-stu-id="d4c53-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="d4c53-108">Ez a művelet idempotent.</span><span class="sxs-lookup"><span data-stu-id="d4c53-108">This operation is idempotent.</span></span>

## <span data-ttu-id="d4c53-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d4c53-109">EXAMPLES</span></span>

### <span data-ttu-id="d4c53-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d4c53-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="d4c53-111">Új szolgáltatási busz névteret hoz létre a megadott erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="d4c53-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="d4c53-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4c53-112">PARAMETERS</span></span>

### <span data-ttu-id="d4c53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c53-113">-DefaultProfile</span></span>
<span data-ttu-id="d4c53-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4c53-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4c53-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="d4c53-115">-Location</span></span>
<span data-ttu-id="d4c53-116">A szolgáltatás busz névtérének helye.</span><span class="sxs-lookup"><span data-stu-id="d4c53-116">The Service Bus namespace location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c53-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4c53-117">-Name</span></span>
<span data-ttu-id="d4c53-118">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="d4c53-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c53-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c53-119">-ResourceGroupName</span></span>
<span data-ttu-id="d4c53-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d4c53-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c53-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d4c53-121">-SkuCapacity</span></span>
<span data-ttu-id="d4c53-122">A Service Bus Premium névtér átviteli egységei, 1 vagy 2 vagy 4 megengedett érték</span><span class="sxs-lookup"><span data-stu-id="d4c53-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c53-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d4c53-123">-SkuName</span></span>
<span data-ttu-id="d4c53-124">A Service Bus névtér SKU-neve.</span><span class="sxs-lookup"><span data-stu-id="d4c53-124">The Service Bus namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c53-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="d4c53-125">-Tag</span></span>
<span data-ttu-id="d4c53-126">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="d4c53-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="d4c53-127">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="d4c53-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c53-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4c53-128">-Confirm</span></span>
<span data-ttu-id="d4c53-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4c53-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c53-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4c53-130">-WhatIf</span></span>
<span data-ttu-id="d4c53-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4c53-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4c53-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4c53-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c53-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c53-133">CommonParameters</span></span>
<span data-ttu-id="d4c53-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4c53-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c53-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4c53-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c53-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4c53-136">INPUTS</span></span>

### <span data-ttu-id="d4c53-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d4c53-137">System.String</span></span>

### <span data-ttu-id="d4c53-138">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d4c53-138">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d4c53-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d4c53-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d4c53-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4c53-140">OUTPUTS</span></span>

### <span data-ttu-id="d4c53-141">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d4c53-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="d4c53-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4c53-142">NOTES</span></span>

## <span data-ttu-id="d4c53-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4c53-143">RELATED LINKS</span></span>

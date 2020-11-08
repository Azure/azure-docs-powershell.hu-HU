---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013718"
---
# <span data-ttu-id="e39c4-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="e39c4-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="e39c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e39c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e39c4-103">Új szolgáltatási busz névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e39c4-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="e39c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e39c4-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e39c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e39c4-105">DESCRIPTION</span></span>
<span data-ttu-id="e39c4-106">A **New-AzServiceBusNamespace** parancsmag új szolgáltatási busz névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e39c4-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="e39c4-107">A létrehozás után a névtér-erőforrás jegyzékfájlja nem állandó.</span><span class="sxs-lookup"><span data-stu-id="e39c4-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="e39c4-108">Ez a művelet idempotent.</span><span class="sxs-lookup"><span data-stu-id="e39c4-108">This operation is idempotent.</span></span>

## <span data-ttu-id="e39c4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e39c4-109">EXAMPLES</span></span>

### <span data-ttu-id="e39c4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e39c4-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="e39c4-111">Új szolgáltatási busz névteret hoz létre a megadott erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="e39c4-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="e39c4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e39c4-112">PARAMETERS</span></span>

### <span data-ttu-id="e39c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e39c4-113">-DefaultProfile</span></span>
<span data-ttu-id="e39c4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e39c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e39c4-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="e39c4-115">-Location</span></span>
<span data-ttu-id="e39c4-116">A szolgáltatás busz névtérének helye.</span><span class="sxs-lookup"><span data-stu-id="e39c4-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="e39c4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e39c4-117">-Name</span></span>
<span data-ttu-id="e39c4-118">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="e39c4-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="e39c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e39c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="e39c4-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e39c4-120">The resource group name.</span></span>

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

### <span data-ttu-id="e39c4-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e39c4-121">-SkuCapacity</span></span>
<span data-ttu-id="e39c4-122">A Service Bus Premium névtér átviteli egységei, 1 vagy 2 vagy 4 megengedett érték</span><span class="sxs-lookup"><span data-stu-id="e39c4-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="e39c4-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e39c4-123">-SkuName</span></span>
<span data-ttu-id="e39c4-124">A Service Bus névtér SKU-neve.</span><span class="sxs-lookup"><span data-stu-id="e39c4-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="e39c4-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="e39c4-125">-Tag</span></span>
<span data-ttu-id="e39c4-126">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="e39c4-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="e39c4-127">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="e39c4-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e39c4-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e39c4-128">-Confirm</span></span>
<span data-ttu-id="e39c4-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e39c4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e39c4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e39c4-130">-WhatIf</span></span>
<span data-ttu-id="e39c4-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e39c4-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e39c4-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e39c4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e39c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39c4-133">CommonParameters</span></span>
<span data-ttu-id="e39c4-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e39c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39c4-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e39c4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39c4-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e39c4-136">INPUTS</span></span>

### <span data-ttu-id="e39c4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e39c4-137">System.String</span></span>

### <span data-ttu-id="e39c4-138">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e39c4-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e39c4-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e39c4-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e39c4-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e39c4-140">OUTPUTS</span></span>

### <span data-ttu-id="e39c4-141">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e39c4-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e39c4-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e39c4-142">NOTES</span></span>

## <span data-ttu-id="e39c4-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e39c4-143">RELATED LINKS</span></span>

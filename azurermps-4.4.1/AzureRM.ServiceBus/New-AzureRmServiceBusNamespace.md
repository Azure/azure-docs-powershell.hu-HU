---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 79b55b62c3f4add24e52a36756f83bd16466edbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503199"
---
# <span data-ttu-id="94d43-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="94d43-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="94d43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94d43-102">SYNOPSIS</span></span>
<span data-ttu-id="94d43-103">Új szolgáltatási busz névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="94d43-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94d43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94d43-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-NamespaceName] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94d43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94d43-105">DESCRIPTION</span></span>
<span data-ttu-id="94d43-106">A **New-AzureRmServiceBusNamespace** parancsmag új szolgáltatási busz névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="94d43-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="94d43-107">A létrehozás után a névtér-erőforrás jegyzékfájlja nem állandó.</span><span class="sxs-lookup"><span data-stu-id="94d43-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="94d43-108">Ez a művelet idempotent.</span><span class="sxs-lookup"><span data-stu-id="94d43-108">This operation is idempotent.</span></span>

## <span data-ttu-id="94d43-109">Példák</span><span class="sxs-lookup"><span data-stu-id="94d43-109">EXAMPLES</span></span>

### <span data-ttu-id="94d43-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94d43-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
Status             : Active
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
Enabled            : True
```

<span data-ttu-id="94d43-111">Új szolgáltatási busz névteret hoz létre a megadott erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="94d43-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="94d43-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94d43-112">PARAMETERS</span></span>

### <span data-ttu-id="94d43-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="94d43-113">-Location</span></span>
<span data-ttu-id="94d43-114">A szolgáltatás busz névtérének helye.</span><span class="sxs-lookup"><span data-stu-id="94d43-114">The Service Bus namespace location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d43-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="94d43-115">-NamespaceName</span></span>
<span data-ttu-id="94d43-116">A szolgáltatás Buszjának névtér neve.</span><span class="sxs-lookup"><span data-stu-id="94d43-116">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d43-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d43-117">-ResourceGroupName</span></span>
<span data-ttu-id="94d43-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="94d43-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d43-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="94d43-119">-SkuName</span></span>
<span data-ttu-id="94d43-120">A Service Bus névtér SKU-neve.</span><span class="sxs-lookup"><span data-stu-id="94d43-120">The Service Bus namespace SKU name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d43-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="94d43-121">-Tag</span></span>
<span data-ttu-id="94d43-122">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="94d43-122">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="94d43-123">Példa:</span><span class="sxs-lookup"><span data-stu-id="94d43-123">For example:</span></span>

<span data-ttu-id="94d43-124">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="94d43-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d43-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94d43-125">-Confirm</span></span>
<span data-ttu-id="94d43-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94d43-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d43-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94d43-127">-WhatIf</span></span>
<span data-ttu-id="94d43-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94d43-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94d43-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94d43-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d43-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d43-130">CommonParameters</span></span>
<span data-ttu-id="94d43-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94d43-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d43-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d43-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d43-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94d43-133">INPUTS</span></span>

### <span data-ttu-id="94d43-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94d43-134">-ResourceGroup</span></span>
 <span data-ttu-id="94d43-135">System. String</span><span class="sxs-lookup"><span data-stu-id="94d43-135">System.String</span></span>

### <span data-ttu-id="94d43-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="94d43-136">-NamespaceName</span></span>
 <span data-ttu-id="94d43-137">System. String</span><span class="sxs-lookup"><span data-stu-id="94d43-137">System.String</span></span>

### <span data-ttu-id="94d43-138">-Hely</span><span class="sxs-lookup"><span data-stu-id="94d43-138">-Location</span></span>
 <span data-ttu-id="94d43-139">System. String</span><span class="sxs-lookup"><span data-stu-id="94d43-139">System.String</span></span>

### <span data-ttu-id="94d43-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="94d43-140">-SkuName</span></span>
 <span data-ttu-id="94d43-141">System. String</span><span class="sxs-lookup"><span data-stu-id="94d43-141">System.String</span></span>

### <span data-ttu-id="94d43-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="94d43-142">-Tag</span></span>
 <span data-ttu-id="94d43-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="94d43-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="94d43-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94d43-144">OUTPUTS</span></span>

### <span data-ttu-id="94d43-145">Microsoft. Azure. Command. ServiceBus. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="94d43-145">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="94d43-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94d43-146">NOTES</span></span>

## <span data-ttu-id="94d43-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94d43-147">RELATED LINKS</span></span>

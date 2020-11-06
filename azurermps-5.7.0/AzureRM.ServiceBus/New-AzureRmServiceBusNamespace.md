---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 1834adfdb275bc5454e16e72732b649c82704a34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498827"
---
# <span data-ttu-id="9f62a-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9f62a-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="9f62a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f62a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f62a-103">Új szolgáltatási busz névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9f62a-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f62a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f62a-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f62a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f62a-105">DESCRIPTION</span></span>
<span data-ttu-id="9f62a-106">A **New-AzureRmServiceBusNamespace** parancsmag új szolgáltatási busz névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9f62a-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="9f62a-107">A létrehozás után a névtér-erőforrás jegyzékfájlja nem állandó.</span><span class="sxs-lookup"><span data-stu-id="9f62a-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="9f62a-108">Ez a művelet idempotent.</span><span class="sxs-lookup"><span data-stu-id="9f62a-108">This operation is idempotent.</span></span>

## <span data-ttu-id="9f62a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9f62a-109">EXAMPLES</span></span>

### <span data-ttu-id="9f62a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9f62a-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="9f62a-111">Új szolgáltatási busz névteret hoz létre a megadott erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="9f62a-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="9f62a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f62a-112">PARAMETERS</span></span>

### <span data-ttu-id="9f62a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f62a-113">-DefaultProfile</span></span>
<span data-ttu-id="9f62a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f62a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f62a-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="9f62a-115">-Location</span></span>
<span data-ttu-id="9f62a-116">A szolgáltatás busz névtérének helye.</span><span class="sxs-lookup"><span data-stu-id="9f62a-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="9f62a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f62a-117">-Name</span></span>
<span data-ttu-id="9f62a-118">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="9f62a-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f62a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f62a-119">-ResourceGroupName</span></span>
<span data-ttu-id="9f62a-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9f62a-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f62a-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9f62a-121">-SkuName</span></span>
<span data-ttu-id="9f62a-122">A Service Bus névtér SKU-neve.</span><span class="sxs-lookup"><span data-stu-id="9f62a-122">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="9f62a-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="9f62a-123">-Tag</span></span>
<span data-ttu-id="9f62a-124">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="9f62a-124">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="9f62a-125">Példa:</span><span class="sxs-lookup"><span data-stu-id="9f62a-125">For example:</span></span>

<span data-ttu-id="9f62a-126">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="9f62a-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9f62a-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f62a-127">-Confirm</span></span>
<span data-ttu-id="9f62a-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f62a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f62a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f62a-129">-WhatIf</span></span>
<span data-ttu-id="9f62a-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f62a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f62a-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f62a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f62a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f62a-132">CommonParameters</span></span>
<span data-ttu-id="9f62a-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f62a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f62a-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f62a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f62a-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f62a-135">INPUTS</span></span>

### <span data-ttu-id="9f62a-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f62a-136">-ResourceGroup</span></span>
 <span data-ttu-id="9f62a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9f62a-137">System.String</span></span>

### <span data-ttu-id="9f62a-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9f62a-138">-NamespaceName</span></span>
 <span data-ttu-id="9f62a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9f62a-139">System.String</span></span>

### <span data-ttu-id="9f62a-140">-Hely</span><span class="sxs-lookup"><span data-stu-id="9f62a-140">-Location</span></span>
 <span data-ttu-id="9f62a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9f62a-141">System.String</span></span>

### <span data-ttu-id="9f62a-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9f62a-142">-SkuName</span></span>
 <span data-ttu-id="9f62a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9f62a-143">System.String</span></span>

### <span data-ttu-id="9f62a-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="9f62a-144">-Tag</span></span>
 <span data-ttu-id="9f62a-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9f62a-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9f62a-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f62a-146">OUTPUTS</span></span>

### <span data-ttu-id="9f62a-147">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9f62a-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="9f62a-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f62a-148">NOTES</span></span>

## <span data-ttu-id="9f62a-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f62a-149">RELATED LINKS</span></span>


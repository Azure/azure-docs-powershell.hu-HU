---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 134e0d20566a8310a381a38297984202b7509250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680228"
---
# <span data-ttu-id="9ad92-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9ad92-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="9ad92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ad92-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad92-103">Frissíti egy meglévő szolgáltatási busz névtérének leírását.</span><span class="sxs-lookup"><span data-stu-id="9ad92-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ad92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ad92-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> -Name <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ad92-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ad92-105">DESCRIPTION</span></span>
<span data-ttu-id="9ad92-106">A **set-AzureRmServiceBusNamespace** parancsmag az erőforrás csoporton belül frissíti a megadott szolgáltatás busz névtér leírását.</span><span class="sxs-lookup"><span data-stu-id="9ad92-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="9ad92-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9ad92-107">EXAMPLES</span></span>

### <span data-ttu-id="9ad92-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9ad92-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 10 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 10 , Tier : Standard
ProvisioningState  : Succeeded
Status             :
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
Enabled            : False
```

<span data-ttu-id="9ad92-109">Frissíti a szolgáltatás busz-névterét egy új leírással.</span><span class="sxs-lookup"><span data-stu-id="9ad92-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="9ad92-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ad92-110">PARAMETERS</span></span>

### <span data-ttu-id="9ad92-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="9ad92-111">-Location</span></span>
<span data-ttu-id="9ad92-112">A szolgáltatás busz névtérének helye.</span><span class="sxs-lookup"><span data-stu-id="9ad92-112">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="9ad92-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad92-113">-ResourceGroupName</span></span>
<span data-ttu-id="9ad92-114">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9ad92-114">The resource group name.</span></span>

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

### <span data-ttu-id="9ad92-115">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9ad92-115">-SkuCapacity</span></span>
<span data-ttu-id="9ad92-116">Namespace SKU kapacitás</span><span class="sxs-lookup"><span data-stu-id="9ad92-116">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="9ad92-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9ad92-117">-SkuName</span></span>
<span data-ttu-id="9ad92-118">A névtér SKU neve.</span><span class="sxs-lookup"><span data-stu-id="9ad92-118">The namespace SKU name.</span></span>

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

### <span data-ttu-id="9ad92-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="9ad92-119">-Tag</span></span>
<span data-ttu-id="9ad92-120">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="9ad92-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9ad92-121">Példa:</span><span class="sxs-lookup"><span data-stu-id="9ad92-121">For example:</span></span>

<span data-ttu-id="9ad92-122">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="9ad92-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9ad92-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9ad92-123">-Confirm</span></span>
<span data-ttu-id="9ad92-124">Frissíti a szolgáltatás Buszjának névterét a megadott adatokkal.</span><span class="sxs-lookup"><span data-stu-id="9ad92-124">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="9ad92-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ad92-125">-WhatIf</span></span>
<span data-ttu-id="9ad92-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9ad92-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ad92-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ad92-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ad92-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad92-128">-DefaultProfile</span></span>
<span data-ttu-id="9ad92-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ad92-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ad92-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ad92-130">-Name</span></span>
<span data-ttu-id="9ad92-131">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="9ad92-131">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="9ad92-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad92-132">CommonParameters</span></span>
<span data-ttu-id="9ad92-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ad92-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad92-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad92-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad92-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ad92-135">INPUTS</span></span>

### <span data-ttu-id="9ad92-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9ad92-136">-ResourceGroup</span></span>
 <span data-ttu-id="9ad92-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad92-137">System.String</span></span>

### <span data-ttu-id="9ad92-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9ad92-138">-NamespaceName</span></span>
 <span data-ttu-id="9ad92-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad92-139">System.String</span></span>

### <span data-ttu-id="9ad92-140">-Hely</span><span class="sxs-lookup"><span data-stu-id="9ad92-140">-Location</span></span>
 <span data-ttu-id="9ad92-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad92-141">System.String</span></span>

### <span data-ttu-id="9ad92-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9ad92-142">-SkuName</span></span>
 <span data-ttu-id="9ad92-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad92-143">System.String</span></span>

### <span data-ttu-id="9ad92-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="9ad92-144">-Tag</span></span>
 <span data-ttu-id="9ad92-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9ad92-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9ad92-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ad92-146">OUTPUTS</span></span>

### <span data-ttu-id="9ad92-147">Microsoft. Azure. Command. ServiceBus. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9ad92-147">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="9ad92-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ad92-148">NOTES</span></span>
## <span data-ttu-id="9ad92-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ad92-149">RELATED LINKS</span></span>

## <span data-ttu-id="9ad92-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ad92-150">RELATED LINKS</span></span>


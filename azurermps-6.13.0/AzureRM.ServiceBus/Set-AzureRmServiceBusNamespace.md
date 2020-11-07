---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 6ac46fc8b8f94480e11f00d44efc690d97ee56a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679507"
---
# <span data-ttu-id="e4741-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="e4741-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="e4741-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4741-102">SYNOPSIS</span></span>
<span data-ttu-id="e4741-103">Frissíti egy meglévő szolgáltatási busz névtérének leírását.</span><span class="sxs-lookup"><span data-stu-id="e4741-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4741-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4741-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4741-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4741-105">DESCRIPTION</span></span>
<span data-ttu-id="e4741-106">A **set-AzureRmServiceBusNamespace** parancsmag az erőforrás csoporton belül frissíti a megadott szolgáltatás busz névtér leírását.</span><span class="sxs-lookup"><span data-stu-id="e4741-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="e4741-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4741-107">EXAMPLES</span></span>

### <span data-ttu-id="e4741-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e4741-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="e4741-109">Frissíti a szolgáltatás busz-névterét egy új leírással.</span><span class="sxs-lookup"><span data-stu-id="e4741-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="e4741-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4741-110">PARAMETERS</span></span>

### <span data-ttu-id="e4741-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4741-111">-DefaultProfile</span></span>
<span data-ttu-id="e4741-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4741-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4741-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="e4741-113">-Location</span></span>
<span data-ttu-id="e4741-114">A szolgáltatás busz névtérének helye.</span><span class="sxs-lookup"><span data-stu-id="e4741-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="e4741-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4741-115">-Name</span></span>
<span data-ttu-id="e4741-116">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="e4741-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="e4741-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4741-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4741-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4741-118">The resource group name.</span></span>

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

### <span data-ttu-id="e4741-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e4741-119">-SkuCapacity</span></span>
<span data-ttu-id="e4741-120">Namespace SKU kapacitás</span><span class="sxs-lookup"><span data-stu-id="e4741-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="e4741-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e4741-121">-SkuName</span></span>
<span data-ttu-id="e4741-122">A névtér SKU neve.</span><span class="sxs-lookup"><span data-stu-id="e4741-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="e4741-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="e4741-123">-Tag</span></span>
<span data-ttu-id="e4741-124">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="e4741-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e4741-125">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="e4741-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e4741-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4741-126">-Confirm</span></span>
<span data-ttu-id="e4741-127">Frissíti a szolgáltatás Buszjának névterét a megadott adatokkal.</span><span class="sxs-lookup"><span data-stu-id="e4741-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="e4741-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4741-128">-WhatIf</span></span>
<span data-ttu-id="e4741-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4741-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4741-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4741-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4741-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4741-131">CommonParameters</span></span>
<span data-ttu-id="e4741-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4741-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4741-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4741-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4741-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4741-134">INPUTS</span></span>

### <span data-ttu-id="e4741-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e4741-135">System.String</span></span>

### <span data-ttu-id="e4741-136">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e4741-136">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e4741-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4741-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e4741-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4741-138">OUTPUTS</span></span>

### <span data-ttu-id="e4741-139">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e4741-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e4741-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4741-140">NOTES</span></span>

## <span data-ttu-id="e4741-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4741-141">RELATED LINKS</span></span>

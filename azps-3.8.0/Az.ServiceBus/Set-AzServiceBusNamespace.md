---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014308"
---
# <span data-ttu-id="30c78-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="30c78-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="30c78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30c78-102">SYNOPSIS</span></span>
<span data-ttu-id="30c78-103">Frissíti egy meglévő szolgáltatási busz névtérének leírását.</span><span class="sxs-lookup"><span data-stu-id="30c78-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="30c78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30c78-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30c78-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30c78-105">DESCRIPTION</span></span>
<span data-ttu-id="30c78-106">A **set-AzServiceBusNamespace** parancsmag az erőforrás csoporton belül frissíti a megadott szolgáltatás busz névtér leírását.</span><span class="sxs-lookup"><span data-stu-id="30c78-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="30c78-107">Példák</span><span class="sxs-lookup"><span data-stu-id="30c78-107">EXAMPLES</span></span>

### <span data-ttu-id="30c78-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="30c78-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="30c78-109">Frissíti a szolgáltatás busz-névterét egy új leírással.</span><span class="sxs-lookup"><span data-stu-id="30c78-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="30c78-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30c78-110">PARAMETERS</span></span>

### <span data-ttu-id="30c78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c78-111">-DefaultProfile</span></span>
<span data-ttu-id="30c78-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30c78-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c78-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="30c78-113">-Location</span></span>
<span data-ttu-id="30c78-114">A szolgáltatás busz névtérének helye.</span><span class="sxs-lookup"><span data-stu-id="30c78-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="30c78-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="30c78-115">-Name</span></span>
<span data-ttu-id="30c78-116">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="30c78-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="30c78-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c78-117">-ResourceGroupName</span></span>
<span data-ttu-id="30c78-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="30c78-118">The resource group name.</span></span>

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

### <span data-ttu-id="30c78-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="30c78-119">-SkuCapacity</span></span>
<span data-ttu-id="30c78-120">Namespace SKU kapacitás</span><span class="sxs-lookup"><span data-stu-id="30c78-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="30c78-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="30c78-121">-SkuName</span></span>
<span data-ttu-id="30c78-122">A névtér SKU neve.</span><span class="sxs-lookup"><span data-stu-id="30c78-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="30c78-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="30c78-123">-Tag</span></span>
<span data-ttu-id="30c78-124">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="30c78-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="30c78-125">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="30c78-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="30c78-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="30c78-126">-Confirm</span></span>
<span data-ttu-id="30c78-127">Frissíti a szolgáltatás Buszjának névterét a megadott adatokkal.</span><span class="sxs-lookup"><span data-stu-id="30c78-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="30c78-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c78-128">-WhatIf</span></span>
<span data-ttu-id="30c78-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="30c78-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30c78-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30c78-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30c78-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c78-131">CommonParameters</span></span>
<span data-ttu-id="30c78-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30c78-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c78-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30c78-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c78-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30c78-134">INPUTS</span></span>

### <span data-ttu-id="30c78-135">System. String</span><span class="sxs-lookup"><span data-stu-id="30c78-135">System.String</span></span>

### <span data-ttu-id="30c78-136">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="30c78-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="30c78-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="30c78-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="30c78-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30c78-138">OUTPUTS</span></span>

### <span data-ttu-id="30c78-139">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="30c78-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="30c78-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30c78-140">NOTES</span></span>

## <span data-ttu-id="30c78-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30c78-141">RELATED LINKS</span></span>

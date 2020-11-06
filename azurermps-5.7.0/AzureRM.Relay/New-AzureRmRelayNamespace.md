---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 1eed6f722487e3c37d9d12785b07e90516406f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498875"
---
# <span data-ttu-id="26776-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="26776-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="26776-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26776-102">SYNOPSIS</span></span>
<span data-ttu-id="26776-103">Új továbbító névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26776-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26776-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26776-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26776-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26776-105">DESCRIPTION</span></span>
<span data-ttu-id="26776-106">A **New-AzureRmRelayNamespace** parancsmag új továbbítási névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26776-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="26776-107">A létrehozás után a névtér-erőforrás jegyzékfájlja nem állandó.</span><span class="sxs-lookup"><span data-stu-id="26776-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="26776-108">Példák</span><span class="sxs-lookup"><span data-stu-id="26776-108">EXAMPLES</span></span>

### <span data-ttu-id="26776-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="26776-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="26776-110">Új továbbítási névteret hoz létre a megadott erőforráscsoport-csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="26776-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="26776-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26776-111">PARAMETERS</span></span>

### <span data-ttu-id="26776-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26776-112">-DefaultProfile</span></span>
<span data-ttu-id="26776-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26776-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26776-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="26776-114">-Location</span></span>
<span data-ttu-id="26776-115">A továbbítási névtér helye.</span><span class="sxs-lookup"><span data-stu-id="26776-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="26776-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26776-116">-Name</span></span>
<span data-ttu-id="26776-117">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="26776-117">Relay Namespace Name</span></span>

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

### <span data-ttu-id="26776-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26776-118">-ResourceGroupName</span></span>
<span data-ttu-id="26776-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="26776-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="26776-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="26776-120">-Tag</span></span>
<span data-ttu-id="26776-121">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="26776-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="26776-122">Példa:</span><span class="sxs-lookup"><span data-stu-id="26776-122">For example:</span></span>

<span data-ttu-id="26776-123">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="26776-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="26776-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="26776-124">-Confirm</span></span>
<span data-ttu-id="26776-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="26776-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26776-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26776-126">-WhatIf</span></span>
<span data-ttu-id="26776-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="26776-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26776-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26776-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26776-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26776-129">CommonParameters</span></span>
<span data-ttu-id="26776-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26776-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26776-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26776-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26776-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26776-132">INPUTS</span></span>

### <span data-ttu-id="26776-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26776-133">-ResourceGroupName</span></span>
 <span data-ttu-id="26776-134">System. String</span><span class="sxs-lookup"><span data-stu-id="26776-134">System.String</span></span>

### <span data-ttu-id="26776-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="26776-135">-NamespaceName</span></span>
 <span data-ttu-id="26776-136">System. String</span><span class="sxs-lookup"><span data-stu-id="26776-136">System.String</span></span>

### <span data-ttu-id="26776-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="26776-137">-Location</span></span>
 <span data-ttu-id="26776-138">System. String</span><span class="sxs-lookup"><span data-stu-id="26776-138">System.String</span></span>

### <span data-ttu-id="26776-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="26776-139">-SkuName</span></span>
 <span data-ttu-id="26776-140">System. String</span><span class="sxs-lookup"><span data-stu-id="26776-140">System.String</span></span>

### <span data-ttu-id="26776-141">-Címke</span><span class="sxs-lookup"><span data-stu-id="26776-141">-Tag</span></span>
 <span data-ttu-id="26776-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="26776-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="26776-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26776-143">OUTPUTS</span></span>

### <span data-ttu-id="26776-144">Microsoft. Azure. Command. Relay. models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="26776-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="26776-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26776-145">NOTES</span></span>

## <span data-ttu-id="26776-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26776-146">RELATED LINKS</span></span>


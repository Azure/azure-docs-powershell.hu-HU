---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 09c601e2ecfddf417e90efd60b58bcdd1a51ff5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494383"
---
# <span data-ttu-id="002ec-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="002ec-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="002ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="002ec-102">SYNOPSIS</span></span>
<span data-ttu-id="002ec-103">Frissíti egy meglévő továbbítási névtér leírását.</span><span class="sxs-lookup"><span data-stu-id="002ec-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="002ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="002ec-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="002ec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="002ec-105">DESCRIPTION</span></span>
<span data-ttu-id="002ec-106">A **set-AzureRmRelayNamespace** parancsmag a megadott továbbító névtér leírását frissíti az erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="002ec-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="002ec-107">Példák</span><span class="sxs-lookup"><span data-stu-id="002ec-107">EXAMPLES</span></span>

### <span data-ttu-id="002ec-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="002ec-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="002ec-109">Frissíti a továbbítási névteret egy új leírással.</span><span class="sxs-lookup"><span data-stu-id="002ec-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="002ec-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="002ec-110">PARAMETERS</span></span>

### <span data-ttu-id="002ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="002ec-111">-DefaultProfile</span></span>
<span data-ttu-id="002ec-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="002ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="002ec-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="002ec-113">-InputObject</span></span>
<span data-ttu-id="002ec-114">A névtér-objektum továbbítása</span><span class="sxs-lookup"><span data-stu-id="002ec-114">Relay Namespace object</span></span>

```yaml
Type: RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="002ec-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="002ec-115">-Name</span></span>
<span data-ttu-id="002ec-116">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="002ec-116">Relay Namespace Name</span></span>

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

### <span data-ttu-id="002ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="002ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="002ec-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="002ec-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="002ec-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="002ec-119">-Tag</span></span>
<span data-ttu-id="002ec-120">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="002ec-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="002ec-121">Példa:</span><span class="sxs-lookup"><span data-stu-id="002ec-121">For example:</span></span>

<span data-ttu-id="002ec-122">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="002ec-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="002ec-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="002ec-123">-Confirm</span></span>
<span data-ttu-id="002ec-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="002ec-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="002ec-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="002ec-125">-WhatIf</span></span>
<span data-ttu-id="002ec-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="002ec-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="002ec-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="002ec-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="002ec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002ec-128">CommonParameters</span></span>
<span data-ttu-id="002ec-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="002ec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002ec-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="002ec-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002ec-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="002ec-131">INPUTS</span></span>

### <span data-ttu-id="002ec-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="002ec-132">-ResourceGroupName</span></span>
 <span data-ttu-id="002ec-133">System. String</span><span class="sxs-lookup"><span data-stu-id="002ec-133">System.String</span></span>

### <span data-ttu-id="002ec-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="002ec-134">-NamespaceName</span></span>
 <span data-ttu-id="002ec-135">System. String</span><span class="sxs-lookup"><span data-stu-id="002ec-135">System.String</span></span>

### <span data-ttu-id="002ec-136">-Hely</span><span class="sxs-lookup"><span data-stu-id="002ec-136">-Location</span></span>
 <span data-ttu-id="002ec-137">System. String</span><span class="sxs-lookup"><span data-stu-id="002ec-137">System.String</span></span>

### <span data-ttu-id="002ec-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="002ec-138">-Tag</span></span>
 <span data-ttu-id="002ec-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="002ec-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="002ec-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="002ec-140">OUTPUTS</span></span>

### <span data-ttu-id="002ec-141">Microsoft. Azure. Command. Relay. models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="002ec-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="002ec-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="002ec-142">NOTES</span></span>

## <span data-ttu-id="002ec-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="002ec-143">RELATED LINKS</span></span>


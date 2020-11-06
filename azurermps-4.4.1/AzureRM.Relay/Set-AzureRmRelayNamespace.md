---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: c243f31ee549443ad959bde13abc9ff3b68c1560
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494710"
---
# <span data-ttu-id="da682-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="da682-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="da682-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da682-102">SYNOPSIS</span></span>
<span data-ttu-id="da682-103">Frissíti egy meglévő továbbítási névtér leírását.</span><span class="sxs-lookup"><span data-stu-id="da682-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da682-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da682-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da682-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da682-105">DESCRIPTION</span></span>
<span data-ttu-id="da682-106">A **set-AzureRmRelayNamespace** parancsmag a megadott továbbító névtér leírását frissíti az erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="da682-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="da682-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da682-107">EXAMPLES</span></span>

### <span data-ttu-id="da682-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da682-108">Example 1</span></span>
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

<span data-ttu-id="da682-109">Frissíti a továbbítási névteret egy új leírással.</span><span class="sxs-lookup"><span data-stu-id="da682-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="da682-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da682-110">PARAMETERS</span></span>

### <span data-ttu-id="da682-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da682-111">-ResourceGroupName</span></span>
<span data-ttu-id="da682-112">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="da682-112">Resource Group Name.</span></span>

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

### <span data-ttu-id="da682-113">-Címke</span><span class="sxs-lookup"><span data-stu-id="da682-113">-Tag</span></span>
<span data-ttu-id="da682-114">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="da682-114">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="da682-115">Példa:</span><span class="sxs-lookup"><span data-stu-id="da682-115">For example:</span></span>

<span data-ttu-id="da682-116">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="da682-116">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="da682-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da682-117">-Confirm</span></span>
<span data-ttu-id="da682-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da682-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da682-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da682-119">-WhatIf</span></span>
<span data-ttu-id="da682-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da682-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da682-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da682-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da682-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da682-122">-DefaultProfile</span></span>
<span data-ttu-id="da682-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da682-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da682-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da682-124">-InputObject</span></span>
<span data-ttu-id="da682-125">A névtér-objektum továbbítása</span><span class="sxs-lookup"><span data-stu-id="da682-125">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da682-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da682-126">-Name</span></span>
<span data-ttu-id="da682-127">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="da682-127">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da682-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da682-128">CommonParameters</span></span>
<span data-ttu-id="da682-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da682-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da682-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da682-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da682-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da682-131">INPUTS</span></span>

### <span data-ttu-id="da682-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da682-132">-ResourceGroupName</span></span>
 <span data-ttu-id="da682-133">System. String</span><span class="sxs-lookup"><span data-stu-id="da682-133">System.String</span></span>

### <span data-ttu-id="da682-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="da682-134">-NamespaceName</span></span>
 <span data-ttu-id="da682-135">System. String</span><span class="sxs-lookup"><span data-stu-id="da682-135">System.String</span></span>

### <span data-ttu-id="da682-136">-Hely</span><span class="sxs-lookup"><span data-stu-id="da682-136">-Location</span></span>
 <span data-ttu-id="da682-137">System. String</span><span class="sxs-lookup"><span data-stu-id="da682-137">System.String</span></span>

### <span data-ttu-id="da682-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="da682-138">-Tag</span></span>
 <span data-ttu-id="da682-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="da682-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="da682-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da682-140">OUTPUTS</span></span>

### <span data-ttu-id="da682-141">Microsoft. Azure. Command. Relay. models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="da682-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="da682-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da682-142">NOTES</span></span>

## <span data-ttu-id="da682-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da682-143">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 6bb333de426236099bed7402fc4756181415c4ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672292"
---
# <span data-ttu-id="d131f-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="d131f-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="d131f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d131f-102">SYNOPSIS</span></span>
<span data-ttu-id="d131f-103">Frissíti egy meglévő továbbítási névtér leírását.</span><span class="sxs-lookup"><span data-stu-id="d131f-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d131f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d131f-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d131f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d131f-105">DESCRIPTION</span></span>
<span data-ttu-id="d131f-106">A **set-AzureRmRelayNamespace** parancsmag a megadott továbbító névtér leírását frissíti az erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="d131f-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="d131f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d131f-107">EXAMPLES</span></span>

### <span data-ttu-id="d131f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d131f-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="d131f-109">Frissíti a továbbítási névteret egy új leírással.</span><span class="sxs-lookup"><span data-stu-id="d131f-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="d131f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d131f-110">PARAMETERS</span></span>

### <span data-ttu-id="d131f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d131f-111">-DefaultProfile</span></span>
<span data-ttu-id="d131f-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d131f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d131f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d131f-113">-InputObject</span></span>
<span data-ttu-id="d131f-114">A névtér-objektum továbbítása</span><span class="sxs-lookup"><span data-stu-id="d131f-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="d131f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d131f-115">-Name</span></span>
<span data-ttu-id="d131f-116">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="d131f-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="d131f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d131f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d131f-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d131f-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="d131f-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="d131f-119">-Tag</span></span>
<span data-ttu-id="d131f-120">Hashtables, amely az erőforrás címkét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d131f-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="d131f-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d131f-121">-Confirm</span></span>
<span data-ttu-id="d131f-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d131f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d131f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d131f-123">-WhatIf</span></span>
<span data-ttu-id="d131f-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d131f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d131f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d131f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d131f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d131f-126">CommonParameters</span></span>
<span data-ttu-id="d131f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d131f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d131f-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d131f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d131f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d131f-129">INPUTS</span></span>

### <span data-ttu-id="d131f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d131f-130">System.String</span></span>
<span data-ttu-id="d131f-131">System. Collections. Hashtable Microsoft. Azure. Command. Relay. models. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="d131f-131">System.Collections.Hashtable Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>


## <span data-ttu-id="d131f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d131f-132">OUTPUTS</span></span>

### <span data-ttu-id="d131f-133">Microsoft. Azure. Command. Relay. models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d131f-133">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>


## <span data-ttu-id="d131f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d131f-134">NOTES</span></span>

## <span data-ttu-id="d131f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d131f-135">RELATED LINKS</span></span>

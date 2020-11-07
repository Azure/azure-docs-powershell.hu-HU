---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846834"
---
# <span data-ttu-id="bdc0d-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="bdc0d-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="bdc0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bdc0d-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc0d-103">Frissíti egy meglévő továbbítási névtér leírását.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="bdc0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bdc0d-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdc0d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bdc0d-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc0d-106">A **set-AzRelayNamespace** parancsmag a megadott továbbító névtér leírását frissíti az erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="bdc0d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bdc0d-107">EXAMPLES</span></span>

### <span data-ttu-id="bdc0d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bdc0d-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="bdc0d-109">Frissíti a továbbítási névteret egy új leírással.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="bdc0d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bdc0d-110">PARAMETERS</span></span>

### <span data-ttu-id="bdc0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc0d-111">-DefaultProfile</span></span>
<span data-ttu-id="bdc0d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdc0d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdc0d-113">-InputObject</span></span>
<span data-ttu-id="bdc0d-114">A névtér-objektum továbbítása</span><span class="sxs-lookup"><span data-stu-id="bdc0d-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="bdc0d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bdc0d-115">-Name</span></span>
<span data-ttu-id="bdc0d-116">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="bdc0d-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="bdc0d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc0d-117">-ResourceGroupName</span></span>
<span data-ttu-id="bdc0d-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="bdc0d-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="bdc0d-119">-Tag</span></span>
<span data-ttu-id="bdc0d-120">Hashtables, amely az erőforrás címkét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="bdc0d-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bdc0d-121">-Confirm</span></span>
<span data-ttu-id="bdc0d-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc0d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc0d-123">-WhatIf</span></span>
<span data-ttu-id="bdc0d-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdc0d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc0d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc0d-126">CommonParameters</span></span>
<span data-ttu-id="bdc0d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bdc0d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc0d-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc0d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc0d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdc0d-129">INPUTS</span></span>

### <span data-ttu-id="bdc0d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bdc0d-130">System.String</span></span>

### <span data-ttu-id="bdc0d-131">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bdc0d-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bdc0d-132">Microsoft. Azure. Command. Relay. models. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="bdc0d-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="bdc0d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdc0d-133">OUTPUTS</span></span>

### <span data-ttu-id="bdc0d-134">Microsoft. Azure. Command. Relay. models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bdc0d-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="bdc0d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bdc0d-135">NOTES</span></span>

## <span data-ttu-id="bdc0d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdc0d-136">RELATED LINKS</span></span>
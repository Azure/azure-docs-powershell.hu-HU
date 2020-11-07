---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: 37e641516ffc21a0984f97cb84f94d2564033fe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838971"
---
# <span data-ttu-id="9dfb7-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="9dfb7-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="9dfb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9dfb7-102">SYNOPSIS</span></span>
<span data-ttu-id="9dfb7-103">Új továbbító névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="9dfb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9dfb7-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dfb7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9dfb7-105">DESCRIPTION</span></span>
<span data-ttu-id="9dfb7-106">A **New-AzRelayNamespace** parancsmag új továbbítási névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="9dfb7-107">A létrehozás után a névtér-erőforrás jegyzékfájlja nem állandó.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="9dfb7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9dfb7-108">EXAMPLES</span></span>

### <span data-ttu-id="9dfb7-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9dfb7-109">Example 1</span></span>
```
PS C:\> New-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

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

<span data-ttu-id="9dfb7-110">Új továbbítási névteret hoz létre a megadott erőforráscsoport-csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="9dfb7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9dfb7-111">PARAMETERS</span></span>

### <span data-ttu-id="9dfb7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dfb7-112">-DefaultProfile</span></span>
<span data-ttu-id="9dfb7-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dfb7-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="9dfb7-114">-Location</span></span>
<span data-ttu-id="9dfb7-115">A továbbítási névtér helye.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-115">Relay Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dfb7-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9dfb7-116">-Name</span></span>
<span data-ttu-id="9dfb7-117">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="9dfb7-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="9dfb7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dfb7-118">-ResourceGroupName</span></span>
<span data-ttu-id="9dfb7-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="9dfb7-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="9dfb7-120">-Tag</span></span>
<span data-ttu-id="9dfb7-121">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="9dfb7-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9dfb7-122">-Confirm</span></span>
<span data-ttu-id="9dfb7-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dfb7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dfb7-124">-WhatIf</span></span>
<span data-ttu-id="9dfb7-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dfb7-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dfb7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dfb7-127">CommonParameters</span></span>
<span data-ttu-id="9dfb7-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9dfb7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dfb7-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dfb7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dfb7-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dfb7-130">INPUTS</span></span>

### <span data-ttu-id="9dfb7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9dfb7-131">System.String</span></span>

### <span data-ttu-id="9dfb7-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9dfb7-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9dfb7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dfb7-133">OUTPUTS</span></span>

### <span data-ttu-id="9dfb7-134">Microsoft. Azure. Command. Relay. models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9dfb7-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="9dfb7-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9dfb7-135">NOTES</span></span>

## <span data-ttu-id="9dfb7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dfb7-136">RELATED LINKS</span></span>

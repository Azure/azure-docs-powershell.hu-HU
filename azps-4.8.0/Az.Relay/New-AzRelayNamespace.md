---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184693"
---
# <span data-ttu-id="fdb34-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="fdb34-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="fdb34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdb34-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb34-103">Új továbbító névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fdb34-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="fdb34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdb34-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb34-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdb34-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb34-106">A **New-AzRelayNamespace** parancsmag új továbbítási névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fdb34-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="fdb34-107">A létrehozás után a névtér-erőforrás jegyzékfájlja nem állandó.</span><span class="sxs-lookup"><span data-stu-id="fdb34-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="fdb34-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fdb34-108">EXAMPLES</span></span>

### <span data-ttu-id="fdb34-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fdb34-109">Example 1</span></span>
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

<span data-ttu-id="fdb34-110">Új továbbítási névteret hoz létre a megadott erőforráscsoport-csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="fdb34-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="fdb34-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdb34-111">PARAMETERS</span></span>

### <span data-ttu-id="fdb34-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb34-112">-DefaultProfile</span></span>
<span data-ttu-id="fdb34-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdb34-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdb34-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="fdb34-114">-Location</span></span>
<span data-ttu-id="fdb34-115">A továbbítási névtér helye.</span><span class="sxs-lookup"><span data-stu-id="fdb34-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="fdb34-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fdb34-116">-Name</span></span>
<span data-ttu-id="fdb34-117">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="fdb34-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="fdb34-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb34-118">-ResourceGroupName</span></span>
<span data-ttu-id="fdb34-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fdb34-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="fdb34-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="fdb34-120">-Tag</span></span>
<span data-ttu-id="fdb34-121">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="fdb34-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="fdb34-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fdb34-122">-Confirm</span></span>
<span data-ttu-id="fdb34-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fdb34-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb34-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb34-124">-WhatIf</span></span>
<span data-ttu-id="fdb34-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fdb34-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdb34-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fdb34-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb34-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb34-127">CommonParameters</span></span>
<span data-ttu-id="fdb34-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdb34-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb34-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb34-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb34-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdb34-130">INPUTS</span></span>

### <span data-ttu-id="fdb34-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fdb34-131">System.String</span></span>

### <span data-ttu-id="fdb34-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fdb34-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fdb34-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdb34-133">OUTPUTS</span></span>

### <span data-ttu-id="fdb34-134">Microsoft. Azure. Command. Relay. models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="fdb34-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="fdb34-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdb34-135">NOTES</span></span>

## <span data-ttu-id="fdb34-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdb34-136">RELATED LINKS</span></span>

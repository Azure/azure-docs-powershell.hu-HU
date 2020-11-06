---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: a809d563c4fe633669e9b1cf9d3bbb39770bfd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493972"
---
# <span data-ttu-id="aab5c-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="aab5c-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="aab5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aab5c-102">SYNOPSIS</span></span>
<span data-ttu-id="aab5c-103">Új továbbító névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aab5c-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aab5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aab5c-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aab5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aab5c-105">DESCRIPTION</span></span>
<span data-ttu-id="aab5c-106">A **New-AzureRmRelayNamespace** parancsmag új továbbítási névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aab5c-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="aab5c-107">A létrehozás után a névtér-erőforrás jegyzékfájlja nem állandó.</span><span class="sxs-lookup"><span data-stu-id="aab5c-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="aab5c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="aab5c-108">EXAMPLES</span></span>

### <span data-ttu-id="aab5c-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aab5c-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

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

<span data-ttu-id="aab5c-110">Új továbbítási névteret hoz létre a megadott erőforráscsoport-csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="aab5c-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="aab5c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aab5c-111">PARAMETERS</span></span>

### <span data-ttu-id="aab5c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab5c-112">-DefaultProfile</span></span>
<span data-ttu-id="aab5c-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aab5c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aab5c-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="aab5c-114">-Location</span></span>
<span data-ttu-id="aab5c-115">A továbbítási névtér helye.</span><span class="sxs-lookup"><span data-stu-id="aab5c-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="aab5c-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aab5c-116">-Name</span></span>
<span data-ttu-id="aab5c-117">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="aab5c-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="aab5c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aab5c-118">-ResourceGroupName</span></span>
<span data-ttu-id="aab5c-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="aab5c-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="aab5c-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="aab5c-120">-Tag</span></span>
<span data-ttu-id="aab5c-121">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="aab5c-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="aab5c-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aab5c-122">-Confirm</span></span>
<span data-ttu-id="aab5c-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aab5c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aab5c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aab5c-124">-WhatIf</span></span>
<span data-ttu-id="aab5c-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aab5c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aab5c-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aab5c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aab5c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab5c-127">CommonParameters</span></span>
<span data-ttu-id="aab5c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aab5c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="aab5c-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aab5c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab5c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aab5c-130">INPUTS</span></span>

### <span data-ttu-id="aab5c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="aab5c-131">System.String</span></span>
<span data-ttu-id="aab5c-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="aab5c-132">System.Collections.Hashtable</span></span>


## <span data-ttu-id="aab5c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aab5c-133">OUTPUTS</span></span>

### <span data-ttu-id="aab5c-134">Microsoft. Azure. Command. Relay. models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="aab5c-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>


## <span data-ttu-id="aab5c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aab5c-135">NOTES</span></span>

## <span data-ttu-id="aab5c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aab5c-136">RELATED LINKS</span></span>

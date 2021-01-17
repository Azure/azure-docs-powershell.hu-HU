---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467226"
---
# <span data-ttu-id="988d4-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="988d4-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="988d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="988d4-102">SYNOPSIS</span></span>
<span data-ttu-id="988d4-103">Új továbbítási névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="988d4-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="988d4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="988d4-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="988d4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="988d4-105">DESCRIPTION</span></span>
<span data-ttu-id="988d4-106">A **New-AzRelayNamespace** parancsmag létrehoz egy új továbbítási névteret.</span><span class="sxs-lookup"><span data-stu-id="988d4-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="988d4-107">Létrehozás után a névtérerőforrás jegyzékfájlja nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="988d4-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="988d4-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="988d4-108">EXAMPLES</span></span>

### <span data-ttu-id="988d4-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="988d4-109">Example 1</span></span>
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

<span data-ttu-id="988d4-110">Új továbbítási névteret hoz létre a megadott erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="988d4-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="988d4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="988d4-111">PARAMETERS</span></span>

### <span data-ttu-id="988d4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="988d4-112">-DefaultProfile</span></span>
<span data-ttu-id="988d4-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="988d4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="988d4-114">-Location</span><span class="sxs-lookup"><span data-stu-id="988d4-114">-Location</span></span>
<span data-ttu-id="988d4-115">Továbbító névterének helye.</span><span class="sxs-lookup"><span data-stu-id="988d4-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="988d4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="988d4-116">-Name</span></span>
<span data-ttu-id="988d4-117">Relay Namespace Name (Továbbítás neve)</span><span class="sxs-lookup"><span data-stu-id="988d4-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="988d4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="988d4-118">-ResourceGroupName</span></span>
<span data-ttu-id="988d4-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="988d4-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="988d4-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="988d4-120">-Tag</span></span>
<span data-ttu-id="988d4-121">Erőforráscímkéket képviselő hashtables.</span><span class="sxs-lookup"><span data-stu-id="988d4-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="988d4-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="988d4-122">-Confirm</span></span>
<span data-ttu-id="988d4-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="988d4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="988d4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="988d4-124">-WhatIf</span></span>
<span data-ttu-id="988d4-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="988d4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="988d4-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="988d4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="988d4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988d4-127">CommonParameters</span></span>
<span data-ttu-id="988d4-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="988d4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="988d4-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="988d4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988d4-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="988d4-130">INPUTS</span></span>

### <span data-ttu-id="988d4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="988d4-131">System.String</span></span>

### <span data-ttu-id="988d4-132">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="988d4-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="988d4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="988d4-133">OUTPUTS</span></span>

### <span data-ttu-id="988d4-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="988d4-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="988d4-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="988d4-135">NOTES</span></span>

## <span data-ttu-id="988d4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="988d4-136">RELATED LINKS</span></span>

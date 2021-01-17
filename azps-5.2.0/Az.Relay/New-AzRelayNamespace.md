---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368057"
---
# <span data-ttu-id="0b0d8-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="0b0d8-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="0b0d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0b0d8-103">Új továbbítási névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="0b0d8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b0d8-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b0d8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b0d8-105">DESCRIPTION</span></span>
<span data-ttu-id="0b0d8-106">A **New-AzRelayNamespace** parancsmag létrehoz egy új továbbítási névteret.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="0b0d8-107">Létrehozás után a névtérerőforrás jegyzékfájlja nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="0b0d8-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b0d8-108">EXAMPLES</span></span>

### <span data-ttu-id="0b0d8-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="0b0d8-109">Example 1</span></span>
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

<span data-ttu-id="0b0d8-110">Új továbbítási névteret hoz létre a megadott erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="0b0d8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b0d8-111">PARAMETERS</span></span>

### <span data-ttu-id="0b0d8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b0d8-112">-DefaultProfile</span></span>
<span data-ttu-id="0b0d8-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b0d8-114">-Location</span><span class="sxs-lookup"><span data-stu-id="0b0d8-114">-Location</span></span>
<span data-ttu-id="0b0d8-115">Továbbító névterének helye.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="0b0d8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0b0d8-116">-Name</span></span>
<span data-ttu-id="0b0d8-117">Relay Namespace Name (Továbbítás neve)</span><span class="sxs-lookup"><span data-stu-id="0b0d8-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="0b0d8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b0d8-118">-ResourceGroupName</span></span>
<span data-ttu-id="0b0d8-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="0b0d8-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b0d8-120">-Tag</span></span>
<span data-ttu-id="0b0d8-121">Erőforráscímkéket képviselő hashtables.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="0b0d8-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b0d8-122">-Confirm</span></span>
<span data-ttu-id="0b0d8-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b0d8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b0d8-124">-WhatIf</span></span>
<span data-ttu-id="0b0d8-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b0d8-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b0d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b0d8-127">CommonParameters</span></span>
<span data-ttu-id="0b0d8-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b0d8-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b0d8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b0d8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b0d8-130">INPUTS</span></span>

### <span data-ttu-id="0b0d8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0b0d8-131">System.String</span></span>

### <span data-ttu-id="0b0d8-132">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b0d8-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b0d8-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b0d8-133">OUTPUTS</span></span>

### <span data-ttu-id="0b0d8-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="0b0d8-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="0b0d8-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b0d8-135">NOTES</span></span>

## <span data-ttu-id="0b0d8-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b0d8-136">RELATED LINKS</span></span>

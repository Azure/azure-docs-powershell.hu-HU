---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160042"
---
# <span data-ttu-id="24720-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="24720-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="24720-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24720-102">SYNOPSIS</span></span>
<span data-ttu-id="24720-103">Frissíti egy meglévő továbbítási névtér leírását.</span><span class="sxs-lookup"><span data-stu-id="24720-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="24720-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="24720-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24720-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="24720-105">DESCRIPTION</span></span>
<span data-ttu-id="24720-106">A **Set-AzRelayNamespace** parancsmag frissíti a megadott Továbbítás névterének leírását az erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="24720-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="24720-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="24720-107">EXAMPLES</span></span>

### <span data-ttu-id="24720-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="24720-108">Example 1</span></span>
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

<span data-ttu-id="24720-109">Frissíti a Továbbítás névterét egy új leírással.</span><span class="sxs-lookup"><span data-stu-id="24720-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="24720-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24720-110">PARAMETERS</span></span>

### <span data-ttu-id="24720-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24720-111">-DefaultProfile</span></span>
<span data-ttu-id="24720-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24720-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24720-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24720-113">-InputObject</span></span>
<span data-ttu-id="24720-114">Relay Namespace objektum.</span><span class="sxs-lookup"><span data-stu-id="24720-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="24720-115">-Name</span><span class="sxs-lookup"><span data-stu-id="24720-115">-Name</span></span>
<span data-ttu-id="24720-116">Relay Namespace Name (Továbbítás neve)</span><span class="sxs-lookup"><span data-stu-id="24720-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="24720-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24720-117">-ResourceGroupName</span></span>
<span data-ttu-id="24720-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="24720-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="24720-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="24720-119">-Tag</span></span>
<span data-ttu-id="24720-120">Az erőforráscímkéket képviselő hashtables.</span><span class="sxs-lookup"><span data-stu-id="24720-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="24720-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24720-121">-Confirm</span></span>
<span data-ttu-id="24720-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="24720-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24720-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24720-123">-WhatIf</span></span>
<span data-ttu-id="24720-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="24720-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24720-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24720-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24720-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24720-126">CommonParameters</span></span>
<span data-ttu-id="24720-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24720-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24720-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24720-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24720-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24720-129">INPUTS</span></span>

### <span data-ttu-id="24720-130">System.String</span><span class="sxs-lookup"><span data-stu-id="24720-130">System.String</span></span>

### <span data-ttu-id="24720-131">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="24720-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="24720-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="24720-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="24720-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24720-133">OUTPUTS</span></span>

### <span data-ttu-id="24720-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="24720-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="24720-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="24720-135">NOTES</span></span>

## <span data-ttu-id="24720-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24720-136">RELATED LINKS</span></span>

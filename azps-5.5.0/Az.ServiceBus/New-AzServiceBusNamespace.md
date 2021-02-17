---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165090"
---
# <span data-ttu-id="cfd2d-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="cfd2d-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="cfd2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfd2d-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd2d-103">Új Service Bus névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="cfd2d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cfd2d-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfd2d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cfd2d-105">DESCRIPTION</span></span>
<span data-ttu-id="cfd2d-106">A **New-AzServiceBusNamespace** parancsmag létrehoz egy új Service Bus névteret.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="cfd2d-107">Létrehozás után a névtérerőforrás jegyzékfájlja nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="cfd2d-108">Ez a művelet idempotent.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-108">This operation is idempotent.</span></span>

## <span data-ttu-id="cfd2d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cfd2d-109">EXAMPLES</span></span>

### <span data-ttu-id="cfd2d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="cfd2d-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="cfd2d-111">Létrehoz egy új Service Bus névteret a megadott erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="cfd2d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfd2d-112">PARAMETERS</span></span>

### <span data-ttu-id="cfd2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd2d-113">-DefaultProfile</span></span>
<span data-ttu-id="cfd2d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfd2d-115">-Location</span><span class="sxs-lookup"><span data-stu-id="cfd2d-115">-Location</span></span>
<span data-ttu-id="cfd2d-116">A szolgáltatásbusz névterének helye.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="cfd2d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cfd2d-117">-Name</span></span>
<span data-ttu-id="cfd2d-118">ServiceBus Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd2d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd2d-119">-ResourceGroupName</span></span>
<span data-ttu-id="cfd2d-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd2d-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="cfd2d-121">-SkuCapacity</span></span>
<span data-ttu-id="cfd2d-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span><span class="sxs-lookup"><span data-stu-id="cfd2d-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd2d-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cfd2d-123">-SkuName</span></span>
<span data-ttu-id="cfd2d-124">A Szolgáltatásbusz névterének termékváltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-124">The Service Bus namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd2d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="cfd2d-125">-Tag</span></span>
<span data-ttu-id="cfd2d-126">Kulcsérték-párok a kiszolgálón címkékként beállított kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="cfd2d-127">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="cfd2d-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cfd2d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfd2d-128">-Confirm</span></span>
<span data-ttu-id="cfd2d-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfd2d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfd2d-130">-WhatIf</span></span>
<span data-ttu-id="cfd2d-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfd2d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfd2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd2d-133">CommonParameters</span></span>
<span data-ttu-id="cfd2d-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfd2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd2d-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfd2d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd2d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cfd2d-136">INPUTS</span></span>

### <span data-ttu-id="cfd2d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="cfd2d-137">System.String</span></span>

### <span data-ttu-id="cfd2d-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cfd2d-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cfd2d-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cfd2d-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cfd2d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfd2d-140">OUTPUTS</span></span>

### <span data-ttu-id="cfd2d-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="cfd2d-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="cfd2d-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cfd2d-142">NOTES</span></span>

## <span data-ttu-id="cfd2d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfd2d-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: b17fa7309274f261c329eaf896519f8bb70d06fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838803"
---
# <span data-ttu-id="e2764-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="e2764-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="e2764-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2764-102">SYNOPSIS</span></span>
<span data-ttu-id="e2764-103">Eltávolítja a névteret a megadott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="e2764-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="e2764-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2764-104">SYNTAX</span></span>

### <span data-ttu-id="e2764-105">NamespacePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2764-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2764-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e2764-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2764-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2764-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2764-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2764-108">DESCRIPTION</span></span>
<span data-ttu-id="e2764-109">A **Remove-AzServiceBusNamespace** parancsmag eltávolítja a névteret a megadott erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="e2764-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="e2764-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e2764-110">EXAMPLES</span></span>

### <span data-ttu-id="e2764-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e2764-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="e2764-112">Eltávolítja a szervizsor névterét `SB-Example1` a megadott erőforráscsoport közül `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="e2764-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="e2764-113">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="e2764-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="e2764-114">Eltávolítja a $inputobjecton keresztül kapott szolgáltatás busz névterét.</span><span class="sxs-lookup"><span data-stu-id="e2764-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="e2764-115">Példa 2,2-InputObject:</span><span class="sxs-lookup"><span data-stu-id="e2764-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="e2764-116">A szolgáltatás busz-névtérének eltávolítása a csővezetékek használatával.</span><span class="sxs-lookup"><span data-stu-id="e2764-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="e2764-117">Példa: 3 – ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2764-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="e2764-118">A $resourceid ResourceId paraméterben vagy a csővezetéken keresztül az ARM-azonosítóval megadott szolgáltatás busz névterét távolítja el.</span><span class="sxs-lookup"><span data-stu-id="e2764-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="e2764-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2764-119">PARAMETERS</span></span>

### <span data-ttu-id="e2764-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2764-120">-AsJob</span></span>
<span data-ttu-id="e2764-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e2764-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2764-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2764-122">-DefaultProfile</span></span>
<span data-ttu-id="e2764-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2764-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2764-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2764-124">-InputObject</span></span>
<span data-ttu-id="e2764-125">A Service Bus Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="e2764-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2764-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2764-126">-Name</span></span>
<span data-ttu-id="e2764-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="e2764-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2764-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2764-128">-PassThru</span></span>
<span data-ttu-id="e2764-129">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="e2764-129">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2764-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2764-130">-ResourceGroupName</span></span>
<span data-ttu-id="e2764-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e2764-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2764-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2764-132">-ResourceId</span></span>
<span data-ttu-id="e2764-133">A Service Bus névtér erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e2764-133">Service Bus Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2764-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2764-134">-Confirm</span></span>
<span data-ttu-id="e2764-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2764-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2764-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2764-136">-WhatIf</span></span>
<span data-ttu-id="e2764-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2764-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2764-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2764-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2764-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2764-139">CommonParameters</span></span>
<span data-ttu-id="e2764-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2764-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2764-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2764-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2764-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2764-142">INPUTS</span></span>

### <span data-ttu-id="e2764-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e2764-143">System.String</span></span>

### <span data-ttu-id="e2764-144">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e2764-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e2764-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2764-145">OUTPUTS</span></span>

### <span data-ttu-id="e2764-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2764-146">System.Boolean</span></span>

## <span data-ttu-id="e2764-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2764-147">NOTES</span></span>

## <span data-ttu-id="e2764-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2764-148">RELATED LINKS</span></span>

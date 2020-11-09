---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296759"
---
# <span data-ttu-id="d5566-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="d5566-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="d5566-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5566-102">SYNOPSIS</span></span>
<span data-ttu-id="d5566-103">Eltávolítja a névteret a megadott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="d5566-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="d5566-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5566-104">SYNTAX</span></span>

### <span data-ttu-id="d5566-105">NamespacePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5566-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5566-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d5566-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5566-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5566-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5566-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5566-108">DESCRIPTION</span></span>
<span data-ttu-id="d5566-109">A **Remove-AzServiceBusNamespace** parancsmag eltávolítja a névteret a megadott erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="d5566-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="d5566-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d5566-110">EXAMPLES</span></span>

### <span data-ttu-id="d5566-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d5566-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="d5566-112">Eltávolítja a szervizsor névterét `SB-Example1` a megadott erőforráscsoport közül `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="d5566-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="d5566-113">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="d5566-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="d5566-114">Eltávolítja a $inputobjecton keresztül kapott szolgáltatás busz névterét.</span><span class="sxs-lookup"><span data-stu-id="d5566-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="d5566-115">Példa 2,2-InputObject:</span><span class="sxs-lookup"><span data-stu-id="d5566-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="d5566-116">A szolgáltatás busz-névtérének eltávolítása a csővezetékek használatával.</span><span class="sxs-lookup"><span data-stu-id="d5566-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="d5566-117">Példa: 3 – ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5566-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="d5566-118">A $resourceid ResourceId paraméterben vagy a csővezetéken keresztül az ARM-azonosítóval megadott szolgáltatás busz névterét távolítja el.</span><span class="sxs-lookup"><span data-stu-id="d5566-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="d5566-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5566-119">PARAMETERS</span></span>

### <span data-ttu-id="d5566-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5566-120">-AsJob</span></span>
<span data-ttu-id="d5566-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d5566-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5566-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5566-122">-DefaultProfile</span></span>
<span data-ttu-id="d5566-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5566-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5566-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5566-124">-InputObject</span></span>
<span data-ttu-id="d5566-125">A Service Bus Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="d5566-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="d5566-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5566-126">-Name</span></span>
<span data-ttu-id="d5566-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="d5566-127">Namespace Name.</span></span>

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

### <span data-ttu-id="d5566-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5566-128">-PassThru</span></span>
<span data-ttu-id="d5566-129">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="d5566-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d5566-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5566-130">-ResourceGroupName</span></span>
<span data-ttu-id="d5566-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d5566-131">The name of the resource group</span></span>

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

### <span data-ttu-id="d5566-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5566-132">-ResourceId</span></span>
<span data-ttu-id="d5566-133">A Service Bus névtér erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d5566-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="d5566-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d5566-134">-Confirm</span></span>
<span data-ttu-id="d5566-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d5566-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5566-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5566-136">-WhatIf</span></span>
<span data-ttu-id="d5566-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d5566-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5566-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d5566-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5566-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5566-139">CommonParameters</span></span>
<span data-ttu-id="d5566-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5566-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5566-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5566-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5566-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5566-142">INPUTS</span></span>

### <span data-ttu-id="d5566-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d5566-143">System.String</span></span>

### <span data-ttu-id="d5566-144">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d5566-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="d5566-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5566-145">OUTPUTS</span></span>

### <span data-ttu-id="d5566-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5566-146">System.Boolean</span></span>

## <span data-ttu-id="d5566-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5566-147">NOTES</span></span>

## <span data-ttu-id="d5566-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5566-148">RELATED LINKS</span></span>

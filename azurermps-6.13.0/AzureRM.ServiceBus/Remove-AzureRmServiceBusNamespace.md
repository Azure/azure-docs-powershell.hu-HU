---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: c56637b8470e40e6b46984117a764da248684005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672447"
---
# <span data-ttu-id="7ca65-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="7ca65-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="7ca65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ca65-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca65-103">Eltávolítja a névteret a megadott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="7ca65-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ca65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ca65-104">SYNTAX</span></span>

### <span data-ttu-id="7ca65-105">NamespacePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ca65-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca65-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7ca65-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca65-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca65-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ca65-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ca65-108">DESCRIPTION</span></span>
<span data-ttu-id="7ca65-109">A **Remove-AzureRmServiceBusNamespace** parancsmag eltávolítja a névteret a megadott erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="7ca65-109">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="7ca65-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7ca65-110">EXAMPLES</span></span>

### <span data-ttu-id="7ca65-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7ca65-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="7ca65-112">Eltávolítja a szervizsor névterét `SB-Example1` a megadott erőforráscsoport közül `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="7ca65-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="7ca65-113">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="7ca65-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusNamespace <params>
PS C:\> Remove-AzureRmServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="7ca65-114">Eltávolítja a $inputobjecton keresztül kapott szolgáltatás busz névterét.</span><span class="sxs-lookup"><span data-stu-id="7ca65-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="7ca65-115">Példa 2,2-InputObject:</span><span class="sxs-lookup"><span data-stu-id="7ca65-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace <params> | Remove-AzureRmServiceBusNamespace
```

<span data-ttu-id="7ca65-116">A szolgáltatás busz-névtérének eltávolítása a csővezetékek használatával.</span><span class="sxs-lookup"><span data-stu-id="7ca65-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="7ca65-117">Példa: 3 – ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ca65-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzureRmResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="7ca65-118">A $resourceid ResourceId paraméterben vagy a csővezetéken keresztül az ARM-azonosítóval megadott szolgáltatás busz névterét távolítja el.</span><span class="sxs-lookup"><span data-stu-id="7ca65-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="7ca65-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ca65-119">PARAMETERS</span></span>

### <span data-ttu-id="7ca65-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ca65-120">-AsJob</span></span>
<span data-ttu-id="7ca65-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7ca65-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ca65-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca65-122">-DefaultProfile</span></span>
<span data-ttu-id="7ca65-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ca65-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ca65-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ca65-124">-InputObject</span></span>
<span data-ttu-id="7ca65-125">A Service Bus Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="7ca65-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="7ca65-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ca65-126">-Name</span></span>
<span data-ttu-id="7ca65-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="7ca65-127">Namespace Name.</span></span>

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

### <span data-ttu-id="7ca65-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ca65-128">-PassThru</span></span>
<span data-ttu-id="7ca65-129">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="7ca65-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7ca65-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca65-130">-ResourceGroupName</span></span>
<span data-ttu-id="7ca65-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7ca65-131">The name of the resource group</span></span>

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

### <span data-ttu-id="7ca65-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ca65-132">-ResourceId</span></span>
<span data-ttu-id="7ca65-133">A Service Bus névtér erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7ca65-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="7ca65-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7ca65-134">-Confirm</span></span>
<span data-ttu-id="7ca65-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ca65-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca65-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca65-136">-WhatIf</span></span>
<span data-ttu-id="7ca65-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7ca65-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ca65-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ca65-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca65-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca65-139">CommonParameters</span></span>
<span data-ttu-id="7ca65-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ca65-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca65-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ca65-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca65-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ca65-142">INPUTS</span></span>

### <span data-ttu-id="7ca65-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7ca65-143">System.String</span></span>

### <span data-ttu-id="7ca65-144">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7ca65-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="7ca65-145">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7ca65-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7ca65-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ca65-146">OUTPUTS</span></span>

### <span data-ttu-id="7ca65-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ca65-147">System.Boolean</span></span>

## <span data-ttu-id="7ca65-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ca65-148">NOTES</span></span>

## <span data-ttu-id="7ca65-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ca65-149">RELATED LINKS</span></span>

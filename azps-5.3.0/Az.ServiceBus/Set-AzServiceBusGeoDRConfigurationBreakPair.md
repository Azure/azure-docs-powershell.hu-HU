---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f45899b1c2d397245461a10a6e2648f92dc9da40
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479616"
---
# <span data-ttu-id="4de33-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="4de33-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="4de33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4de33-102">SYNOPSIS</span></span>
<span data-ttu-id="4de33-103">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja a módosítások elsődlegesről másodlagos névterekbe való replikálását.</span><span class="sxs-lookup"><span data-stu-id="4de33-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="4de33-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4de33-104">SYNTAX</span></span>

### <span data-ttu-id="4de33-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4de33-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4de33-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4de33-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4de33-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4de33-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4de33-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4de33-108">DESCRIPTION</span></span>
<span data-ttu-id="4de33-109">A **Set-AzServiceBusGeoDRConfigurationBreakPair** parancsmag letiltja a katasztrófa-helyreállítást, és leállítja a módosítások elsődlegesről másodlagos névtérre való replikálását.</span><span class="sxs-lookup"><span data-stu-id="4de33-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="4de33-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4de33-110">EXAMPLES</span></span>

### <span data-ttu-id="4de33-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4de33-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="4de33-112">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja a módosítások elsődlegesről másodlagos névterekbe való replikálását.</span><span class="sxs-lookup"><span data-stu-id="4de33-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="4de33-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4de33-113">PARAMETERS</span></span>

### <span data-ttu-id="4de33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de33-114">-DefaultProfile</span></span>
<span data-ttu-id="4de33-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4de33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4de33-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4de33-116">-InputObject</span></span>
<span data-ttu-id="4de33-117">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="4de33-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4de33-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4de33-118">-Name</span></span>
<span data-ttu-id="4de33-119">DR Configuration Name</span><span class="sxs-lookup"><span data-stu-id="4de33-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de33-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4de33-120">-Namespace</span></span>
<span data-ttu-id="4de33-121">Namespace Name - Primary Namespace</span><span class="sxs-lookup"><span data-stu-id="4de33-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de33-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4de33-122">-PassThru</span></span>
<span data-ttu-id="4de33-123">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="4de33-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4de33-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4de33-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4de33-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de33-125">-ResourceGroupName</span></span>
<span data-ttu-id="4de33-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4de33-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de33-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4de33-127">-ResourceId</span></span>
<span data-ttu-id="4de33-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="4de33-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de33-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4de33-129">-Confirm</span></span>
<span data-ttu-id="4de33-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4de33-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4de33-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de33-131">-WhatIf</span></span>
<span data-ttu-id="4de33-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4de33-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4de33-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4de33-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4de33-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de33-134">CommonParameters</span></span>
<span data-ttu-id="4de33-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de33-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de33-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de33-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de33-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4de33-137">INPUTS</span></span>

### <span data-ttu-id="4de33-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4de33-138">System.String</span></span>

### <span data-ttu-id="4de33-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="4de33-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="4de33-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4de33-140">OUTPUTS</span></span>

### <span data-ttu-id="4de33-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4de33-141">System.Boolean</span></span>

## <span data-ttu-id="4de33-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4de33-142">NOTES</span></span>

## <span data-ttu-id="4de33-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4de33-143">RELATED LINKS</span></span>

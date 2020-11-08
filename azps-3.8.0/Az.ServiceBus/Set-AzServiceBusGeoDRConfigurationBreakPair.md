---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f45899b1c2d397245461a10a6e2648f92dc9da40
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011094"
---
# <span data-ttu-id="57a79-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="57a79-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="57a79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57a79-102">SYNOPSIS</span></span>
<span data-ttu-id="57a79-103">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja az elsődlegestől a másodlagos névtérig történő módosítások replikálását.</span><span class="sxs-lookup"><span data-stu-id="57a79-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="57a79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57a79-104">SYNTAX</span></span>

### <span data-ttu-id="57a79-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57a79-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57a79-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="57a79-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57a79-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57a79-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57a79-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="57a79-108">DESCRIPTION</span></span>
<span data-ttu-id="57a79-109">A **set-AzServiceBusGeoDRConfigurationBreakPair** parancsmag letiltja a katasztrófa-helyreállítást, és leállítja az elsődlegestől a másodlagos névtérbe való replikálást.</span><span class="sxs-lookup"><span data-stu-id="57a79-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="57a79-110">Példák</span><span class="sxs-lookup"><span data-stu-id="57a79-110">EXAMPLES</span></span>

### <span data-ttu-id="57a79-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="57a79-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="57a79-112">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja az elsődlegestől a másodlagos névtérig történő módosítások replikálását.</span><span class="sxs-lookup"><span data-stu-id="57a79-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="57a79-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57a79-113">PARAMETERS</span></span>

### <span data-ttu-id="57a79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a79-114">-DefaultProfile</span></span>
<span data-ttu-id="57a79-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57a79-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57a79-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57a79-116">-InputObject</span></span>
<span data-ttu-id="57a79-117">A Service Bus GeoDR konfigurációs objektuma</span><span class="sxs-lookup"><span data-stu-id="57a79-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="57a79-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="57a79-118">-Name</span></span>
<span data-ttu-id="57a79-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="57a79-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="57a79-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="57a79-120">-Namespace</span></span>
<span data-ttu-id="57a79-121">Névtér neve – elsődleges névtér</span><span class="sxs-lookup"><span data-stu-id="57a79-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="57a79-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57a79-122">-PassThru</span></span>
<span data-ttu-id="57a79-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="57a79-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="57a79-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="57a79-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="57a79-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57a79-125">-ResourceGroupName</span></span>
<span data-ttu-id="57a79-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="57a79-126">Resource Group Name</span></span>

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

### <span data-ttu-id="57a79-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57a79-127">-ResourceId</span></span>
<span data-ttu-id="57a79-128">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="57a79-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="57a79-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="57a79-129">-Confirm</span></span>
<span data-ttu-id="57a79-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="57a79-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57a79-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57a79-131">-WhatIf</span></span>
<span data-ttu-id="57a79-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="57a79-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57a79-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="57a79-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57a79-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a79-134">CommonParameters</span></span>
<span data-ttu-id="57a79-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57a79-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a79-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57a79-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a79-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57a79-137">INPUTS</span></span>

### <span data-ttu-id="57a79-138">System. String</span><span class="sxs-lookup"><span data-stu-id="57a79-138">System.String</span></span>

### <span data-ttu-id="57a79-139">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="57a79-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="57a79-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57a79-140">OUTPUTS</span></span>

### <span data-ttu-id="57a79-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57a79-141">System.Boolean</span></span>

## <span data-ttu-id="57a79-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57a79-142">NOTES</span></span>

## <span data-ttu-id="57a79-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57a79-143">RELATED LINKS</span></span>

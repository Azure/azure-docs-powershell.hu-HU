---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 1bb881d96b0247b4cc6d59171c146d75f6df9de0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195325"
---
# <span data-ttu-id="a877b-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="a877b-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="a877b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a877b-102">SYNOPSIS</span></span>
<span data-ttu-id="a877b-103">Új alias létrehozása (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="a877b-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="a877b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a877b-104">SYNTAX</span></span>

### <span data-ttu-id="a877b-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a877b-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a877b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a877b-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a877b-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a877b-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a877b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a877b-108">DESCRIPTION</span></span>
<span data-ttu-id="a877b-109">A **New-AzServiceBusGeoDRConfiguration** parancsmag új aliast hoz létre (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="a877b-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="a877b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a877b-110">EXAMPLES</span></span>

### <span data-ttu-id="a877b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a877b-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="a877b-112">"SampleDRConfigName" aliast hoz létre "SampleNamespace_Primary" elsődleges névtérrel, "SampleNamespace_Secondary" másodlagos névtérrel</span><span class="sxs-lookup"><span data-stu-id="a877b-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="a877b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a877b-113">PARAMETERS</span></span>

### <span data-ttu-id="a877b-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="a877b-114">-AlternateName</span></span>
<span data-ttu-id="a877b-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="a877b-115">AlternateName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a877b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a877b-116">-AsJob</span></span>
<span data-ttu-id="a877b-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a877b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a877b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a877b-118">-DefaultProfile</span></span>
<span data-ttu-id="a877b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a877b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a877b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a877b-120">-InputObject</span></span>
<span data-ttu-id="a877b-121">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="a877b-121">Namespace Object</span></span>

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

### <span data-ttu-id="a877b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a877b-122">-Name</span></span>
<span data-ttu-id="a877b-123">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="a877b-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="a877b-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a877b-124">-Namespace</span></span>
<span data-ttu-id="a877b-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="a877b-125">Namespace Name</span></span>

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

### <span data-ttu-id="a877b-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="a877b-126">-PartnerNamespace</span></span>
<span data-ttu-id="a877b-127">DR konfigurációs PartnerNamespace (PartnerNamespace [másodlagos névtér])</span><span class="sxs-lookup"><span data-stu-id="a877b-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a877b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a877b-128">-ResourceGroupName</span></span>
<span data-ttu-id="a877b-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a877b-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a877b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a877b-130">-ResourceId</span></span>
<span data-ttu-id="a877b-131">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="a877b-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="a877b-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a877b-132">-Confirm</span></span>
<span data-ttu-id="a877b-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a877b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a877b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a877b-134">-WhatIf</span></span>
<span data-ttu-id="a877b-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a877b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a877b-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a877b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a877b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a877b-137">CommonParameters</span></span>
<span data-ttu-id="a877b-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a877b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a877b-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a877b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a877b-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a877b-140">INPUTS</span></span>

### <span data-ttu-id="a877b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a877b-141">System.String</span></span>

### <span data-ttu-id="a877b-142">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a877b-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a877b-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a877b-143">OUTPUTS</span></span>

### <span data-ttu-id="a877b-144">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a877b-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="a877b-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a877b-145">NOTES</span></span>

## <span data-ttu-id="a877b-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a877b-146">RELATED LINKS</span></span>
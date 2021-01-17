---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 1bb881d96b0247b4cc6d59171c146d75f6df9de0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371249"
---
# <span data-ttu-id="2269d-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2269d-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="2269d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2269d-102">SYNOPSIS</span></span>
<span data-ttu-id="2269d-103">Létrehoz egy új aliast(katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="2269d-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2269d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2269d-104">SYNTAX</span></span>

### <span data-ttu-id="2269d-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2269d-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2269d-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2269d-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2269d-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2269d-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2269d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2269d-108">DESCRIPTION</span></span>
<span data-ttu-id="2269d-109">A **New-AzServiceBusGeoDRConfiguration** parancsmag létrehoz egy új aliast(Katasztrófa-helyreállítás konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="2269d-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2269d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2269d-110">EXAMPLES</span></span>

### <span data-ttu-id="2269d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2269d-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="2269d-112">Létrehozza az "SampleDRConfigName" aliast a "SampleNamespace_Primary" elsődleges névtér "SampleNamespace_Secondary" névterével</span><span class="sxs-lookup"><span data-stu-id="2269d-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="2269d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2269d-113">PARAMETERS</span></span>

### <span data-ttu-id="2269d-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="2269d-114">-AlternateName</span></span>
<span data-ttu-id="2269d-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="2269d-115">AlternateName</span></span>

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

### <span data-ttu-id="2269d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2269d-116">-AsJob</span></span>
<span data-ttu-id="2269d-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2269d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2269d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2269d-118">-DefaultProfile</span></span>
<span data-ttu-id="2269d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2269d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2269d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2269d-120">-InputObject</span></span>
<span data-ttu-id="2269d-121">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="2269d-121">Namespace Object</span></span>

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

### <span data-ttu-id="2269d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2269d-122">-Name</span></span>
<span data-ttu-id="2269d-123">DR Configuration Name</span><span class="sxs-lookup"><span data-stu-id="2269d-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="2269d-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2269d-124">-Namespace</span></span>
<span data-ttu-id="2269d-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="2269d-125">Namespace Name</span></span>

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

### <span data-ttu-id="2269d-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="2269d-126">-PartnerNamespace</span></span>
<span data-ttu-id="2269d-127">DR Configuration PartnerNamespace (ARM PartnerNamespace azonosítója [Secondary namespace])</span><span class="sxs-lookup"><span data-stu-id="2269d-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="2269d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2269d-128">-ResourceGroupName</span></span>
<span data-ttu-id="2269d-129">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2269d-129">Resource Group Name</span></span>

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

### <span data-ttu-id="2269d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2269d-130">-ResourceId</span></span>
<span data-ttu-id="2269d-131">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="2269d-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2269d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2269d-132">-Confirm</span></span>
<span data-ttu-id="2269d-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2269d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2269d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2269d-134">-WhatIf</span></span>
<span data-ttu-id="2269d-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2269d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2269d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2269d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2269d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2269d-137">CommonParameters</span></span>
<span data-ttu-id="2269d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2269d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2269d-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2269d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2269d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2269d-140">INPUTS</span></span>

### <span data-ttu-id="2269d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2269d-141">System.String</span></span>

### <span data-ttu-id="2269d-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2269d-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="2269d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2269d-143">OUTPUTS</span></span>

### <span data-ttu-id="2269d-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2269d-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="2269d-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2269d-145">NOTES</span></span>

## <span data-ttu-id="2269d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2269d-146">RELATED LINKS</span></span>

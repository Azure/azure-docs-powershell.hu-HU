---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 83d1e9edde6e2e792a24e0dc943cf62068938c2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353178"
---
# <span data-ttu-id="166b7-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="166b7-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="166b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="166b7-102">SYNOPSIS</span></span>
<span data-ttu-id="166b7-103">Létrehoz egy új aliast(katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="166b7-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="166b7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="166b7-104">SYNTAX</span></span>

### <span data-ttu-id="166b7-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="166b7-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="166b7-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="166b7-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="166b7-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="166b7-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="166b7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="166b7-108">DESCRIPTION</span></span>
<span data-ttu-id="166b7-109">The **New-AzEventHubGeoDRConfiguration cmdlet** Creates a new Alias(Disaster Recovery configuration)</span><span class="sxs-lookup"><span data-stu-id="166b7-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="166b7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="166b7-110">EXAMPLES</span></span>

### <span data-ttu-id="166b7-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="166b7-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="166b7-112">Létrehozza az "SampleDRConfigName" aliast a "SampleNamespace_Primary" elsődleges névtér "SampleNamespace_Secondary" névterével</span><span class="sxs-lookup"><span data-stu-id="166b7-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="166b7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="166b7-113">PARAMETERS</span></span>

### <span data-ttu-id="166b7-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="166b7-114">-AlternateName</span></span>
<span data-ttu-id="166b7-115">AlternateName required when DR configuration name is same as Primary Namespace</span><span class="sxs-lookup"><span data-stu-id="166b7-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="166b7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="166b7-116">-AsJob</span></span>
<span data-ttu-id="166b7-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="166b7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="166b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166b7-118">-DefaultProfile</span></span>
<span data-ttu-id="166b7-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="166b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="166b7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="166b7-120">-InputObject</span></span>
<span data-ttu-id="166b7-121">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="166b7-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="166b7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="166b7-122">-Name</span></span>
<span data-ttu-id="166b7-123">DR Configuration Name</span><span class="sxs-lookup"><span data-stu-id="166b7-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="166b7-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="166b7-124">-Namespace</span></span>
<span data-ttu-id="166b7-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="166b7-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166b7-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="166b7-126">-PartnerNamespace</span></span>
<span data-ttu-id="166b7-127">DR Configuration PartnerNamespace ARM ID</span><span class="sxs-lookup"><span data-stu-id="166b7-127">DR Configuration PartnerNamespace ARM ID</span></span>

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

### <span data-ttu-id="166b7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="166b7-128">-ResourceGroupName</span></span>
<span data-ttu-id="166b7-129">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="166b7-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166b7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="166b7-130">-ResourceId</span></span>
<span data-ttu-id="166b7-131">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="166b7-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="166b7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="166b7-132">-Confirm</span></span>
<span data-ttu-id="166b7-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="166b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="166b7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="166b7-134">-WhatIf</span></span>
<span data-ttu-id="166b7-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="166b7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="166b7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="166b7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="166b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166b7-137">CommonParameters</span></span>
<span data-ttu-id="166b7-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="166b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166b7-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="166b7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166b7-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="166b7-140">INPUTS</span></span>

### <span data-ttu-id="166b7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="166b7-141">System.String</span></span>

### <span data-ttu-id="166b7-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="166b7-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="166b7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="166b7-143">OUTPUTS</span></span>

### <span data-ttu-id="166b7-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="166b7-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="166b7-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="166b7-145">NOTES</span></span>

## <span data-ttu-id="166b7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="166b7-146">RELATED LINKS</span></span>

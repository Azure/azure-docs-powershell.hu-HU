---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: cb1f3ba75b05fcd6950a8cb9bcff9fe899aaf471
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666478"
---
# <span data-ttu-id="b6bbb-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6bbb-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="b6bbb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bbb-103">Új alias létrehozása (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="b6bbb-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="b6bbb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6bbb-104">SYNTAX</span></span>

### <span data-ttu-id="b6bbb-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6bbb-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6bbb-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b6bbb-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6bbb-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6bbb-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6bbb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6bbb-108">DESCRIPTION</span></span>
<span data-ttu-id="b6bbb-109">A **New-AzEventHubGeoDRConfiguration** parancsmag új aliast hoz létre (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="b6bbb-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="b6bbb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b6bbb-110">EXAMPLES</span></span>

### <span data-ttu-id="b6bbb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b6bbb-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="b6bbb-112">"SampleDRConfigName" aliast hoz létre "SampleNamespace_Primary" elsődleges névtérrel, "SampleNamespace_Secondary" másodlagos névtérrel</span><span class="sxs-lookup"><span data-stu-id="b6bbb-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="b6bbb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6bbb-113">PARAMETERS</span></span>

### <span data-ttu-id="b6bbb-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="b6bbb-114">-AlternateName</span></span>
<span data-ttu-id="b6bbb-115">Az elsődleges névtérként használt DR-AlternateName megadásához szükséges beállítások</span><span class="sxs-lookup"><span data-stu-id="b6bbb-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="b6bbb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6bbb-116">-AsJob</span></span>
<span data-ttu-id="b6bbb-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b6bbb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6bbb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6bbb-118">-DefaultProfile</span></span>
<span data-ttu-id="b6bbb-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6bbb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6bbb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6bbb-120">-InputObject</span></span>
<span data-ttu-id="b6bbb-121">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="b6bbb-121">Namespace Object</span></span>

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

### <span data-ttu-id="b6bbb-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6bbb-122">-Name</span></span>
<span data-ttu-id="b6bbb-123">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="b6bbb-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="b6bbb-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b6bbb-124">-Namespace</span></span>
<span data-ttu-id="b6bbb-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="b6bbb-125">Namespace Name</span></span>

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

### <span data-ttu-id="b6bbb-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="b6bbb-126">-PartnerNamespace</span></span>
<span data-ttu-id="b6bbb-127">DR konfigurációs PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="b6bbb-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="b6bbb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6bbb-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6bbb-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b6bbb-129">Resource Group Name</span></span>

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

### <span data-ttu-id="b6bbb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6bbb-130">-ResourceId</span></span>
<span data-ttu-id="b6bbb-131">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="b6bbb-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="b6bbb-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6bbb-132">-Confirm</span></span>
<span data-ttu-id="b6bbb-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6bbb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6bbb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6bbb-134">-WhatIf</span></span>
<span data-ttu-id="b6bbb-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6bbb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6bbb-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6bbb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6bbb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bbb-137">CommonParameters</span></span>
<span data-ttu-id="b6bbb-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6bbb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bbb-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6bbb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bbb-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6bbb-140">INPUTS</span></span>

### <span data-ttu-id="b6bbb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b6bbb-141">System.String</span></span>

### <span data-ttu-id="b6bbb-142">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b6bbb-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b6bbb-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6bbb-143">OUTPUTS</span></span>

### <span data-ttu-id="b6bbb-144">Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b6bbb-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="b6bbb-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6bbb-145">NOTES</span></span>

## <span data-ttu-id="b6bbb-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6bbb-146">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: bc7ad71c694bc994e621a9b3c9dd0e0f076f6f73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670834"
---
# <span data-ttu-id="2008d-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2008d-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="2008d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2008d-102">SYNOPSIS</span></span>
<span data-ttu-id="2008d-103">Új alias létrehozása (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="2008d-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2008d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2008d-104">SYNTAX</span></span>

### <span data-ttu-id="2008d-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2008d-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2008d-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2008d-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2008d-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2008d-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2008d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2008d-108">DESCRIPTION</span></span>
<span data-ttu-id="2008d-109">A **New-AzEventHubGeoDRConfiguration** parancsmag új aliast hoz létre (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="2008d-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2008d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2008d-110">EXAMPLES</span></span>

### <span data-ttu-id="2008d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2008d-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="2008d-112">"SampleDRCongifName" aliast hoz létre "SampleNamespace_Primary" elsődleges névtérrel, "SampleNamespace_Secondary" másodlagos névtérrel</span><span class="sxs-lookup"><span data-stu-id="2008d-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="2008d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2008d-113">PARAMETERS</span></span>

### <span data-ttu-id="2008d-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="2008d-114">-AlternateName</span></span>
<span data-ttu-id="2008d-115">Az elsődleges névtérként használt DR-AlternateName megadásához szükséges beállítások</span><span class="sxs-lookup"><span data-stu-id="2008d-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="2008d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2008d-116">-AsJob</span></span>
<span data-ttu-id="2008d-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2008d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2008d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2008d-118">-DefaultProfile</span></span>
<span data-ttu-id="2008d-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2008d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2008d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2008d-120">-InputObject</span></span>
<span data-ttu-id="2008d-121">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="2008d-121">Namespace Object</span></span>

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

### <span data-ttu-id="2008d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2008d-122">-Name</span></span>
<span data-ttu-id="2008d-123">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="2008d-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="2008d-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2008d-124">-Namespace</span></span>
<span data-ttu-id="2008d-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="2008d-125">Namespace Name</span></span>

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

### <span data-ttu-id="2008d-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="2008d-126">-PartnerNamespace</span></span>
<span data-ttu-id="2008d-127">DR konfigurációs PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="2008d-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="2008d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2008d-128">-ResourceGroupName</span></span>
<span data-ttu-id="2008d-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2008d-129">Resource Group Name</span></span>

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

### <span data-ttu-id="2008d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2008d-130">-ResourceId</span></span>
<span data-ttu-id="2008d-131">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="2008d-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2008d-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2008d-132">-Confirm</span></span>
<span data-ttu-id="2008d-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2008d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2008d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2008d-134">-WhatIf</span></span>
<span data-ttu-id="2008d-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2008d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2008d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2008d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2008d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2008d-137">CommonParameters</span></span>
<span data-ttu-id="2008d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2008d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2008d-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2008d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2008d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2008d-140">INPUTS</span></span>

### <span data-ttu-id="2008d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2008d-141">System.String</span></span>

### <span data-ttu-id="2008d-142">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2008d-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="2008d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2008d-143">OUTPUTS</span></span>

### <span data-ttu-id="2008d-144">Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2008d-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="2008d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2008d-145">NOTES</span></span>

## <span data-ttu-id="2008d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2008d-146">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e2f1edfa0d1b5fa081754457fa3fc53f310eb345
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672894"
---
# <span data-ttu-id="28bcd-101">New-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="28bcd-101">New-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="28bcd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="28bcd-103">Új alias létrehozása (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="28bcd-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28bcd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28bcd-104">SYNTAX</span></span>

### <span data-ttu-id="28bcd-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28bcd-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28bcd-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="28bcd-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28bcd-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28bcd-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28bcd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="28bcd-108">DESCRIPTION</span></span>
<span data-ttu-id="28bcd-109">A **New-AzureRmServiceBusGeoDRConfiguration** parancsmag új aliast hoz létre (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="28bcd-109">The **New-AzureRmServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="28bcd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="28bcd-110">EXAMPLES</span></span>

### <span data-ttu-id="28bcd-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="28bcd-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="28bcd-112">"SampleDRCongifName" aliast hoz létre "SampleNamespace_Primary" elsődleges névtérrel, "SampleNamespace_Secondary" másodlagos névtérrel</span><span class="sxs-lookup"><span data-stu-id="28bcd-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="28bcd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28bcd-113">PARAMETERS</span></span>

### <span data-ttu-id="28bcd-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="28bcd-114">-AlternateName</span></span>
<span data-ttu-id="28bcd-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="28bcd-115">AlternateName</span></span>

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

### <span data-ttu-id="28bcd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28bcd-116">-AsJob</span></span>
<span data-ttu-id="28bcd-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="28bcd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28bcd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28bcd-118">-DefaultProfile</span></span>
<span data-ttu-id="28bcd-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28bcd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28bcd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28bcd-120">-InputObject</span></span>
<span data-ttu-id="28bcd-121">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="28bcd-121">Namespace Object</span></span>

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

### <span data-ttu-id="28bcd-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="28bcd-122">-Name</span></span>
<span data-ttu-id="28bcd-123">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="28bcd-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="28bcd-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="28bcd-124">-Namespace</span></span>
<span data-ttu-id="28bcd-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="28bcd-125">Namespace Name</span></span>

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

### <span data-ttu-id="28bcd-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="28bcd-126">-PartnerNamespace</span></span>
<span data-ttu-id="28bcd-127">DR konfigurációs PartnerNamespace (PartnerNamespace [másodlagos névtér])</span><span class="sxs-lookup"><span data-stu-id="28bcd-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="28bcd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28bcd-128">-ResourceGroupName</span></span>
<span data-ttu-id="28bcd-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="28bcd-129">Resource Group Name</span></span>

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

### <span data-ttu-id="28bcd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28bcd-130">-ResourceId</span></span>
<span data-ttu-id="28bcd-131">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="28bcd-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="28bcd-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="28bcd-132">-Confirm</span></span>
<span data-ttu-id="28bcd-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28bcd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28bcd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28bcd-134">-WhatIf</span></span>
<span data-ttu-id="28bcd-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="28bcd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28bcd-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28bcd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28bcd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28bcd-137">CommonParameters</span></span>
<span data-ttu-id="28bcd-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28bcd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28bcd-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28bcd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28bcd-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28bcd-140">INPUTS</span></span>

### <span data-ttu-id="28bcd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="28bcd-141">System.String</span></span>

### <span data-ttu-id="28bcd-142">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="28bcd-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="28bcd-143">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28bcd-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="28bcd-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28bcd-144">OUTPUTS</span></span>

### <span data-ttu-id="28bcd-145">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="28bcd-145">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="28bcd-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28bcd-146">NOTES</span></span>

## <span data-ttu-id="28bcd-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28bcd-147">RELATED LINKS</span></span>

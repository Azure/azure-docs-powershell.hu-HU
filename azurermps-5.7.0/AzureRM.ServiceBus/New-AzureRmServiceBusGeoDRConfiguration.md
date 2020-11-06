---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: b90144fb94dcef874ce67168364aa65782084b4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502427"
---
# <span data-ttu-id="184f0-101">New-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="184f0-101">New-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="184f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="184f0-102">SYNOPSIS</span></span>
<span data-ttu-id="184f0-103">Új alias létrehozása (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="184f0-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="184f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="184f0-104">SYNTAX</span></span>

### <span data-ttu-id="184f0-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="184f0-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184f0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="184f0-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184f0-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="184f0-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="184f0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="184f0-108">DESCRIPTION</span></span>
<span data-ttu-id="184f0-109">A **New-AzureRmServiceBusGeoDRConfiguration** parancsmag új aliast hoz létre (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="184f0-109">The **New-AzureRmServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="184f0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="184f0-110">EXAMPLES</span></span>

### <span data-ttu-id="184f0-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="184f0-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="184f0-112">"SampleDRCongifName" aliast hoz létre "SampleNamespace_Primary" elsődleges névtérrel, "SampleNamespace_Secondary" másodlagos névtérrel</span><span class="sxs-lookup"><span data-stu-id="184f0-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="184f0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="184f0-113">PARAMETERS</span></span>

### <span data-ttu-id="184f0-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="184f0-114">-AlternateName</span></span>
<span data-ttu-id="184f0-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="184f0-115">AlternateName</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184f0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="184f0-116">-AsJob</span></span>
<span data-ttu-id="184f0-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="184f0-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184f0-118">-DefaultProfile</span></span>
<span data-ttu-id="184f0-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="184f0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184f0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="184f0-120">-InputObject</span></span>
<span data-ttu-id="184f0-121">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="184f0-121">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="184f0-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="184f0-122">-Name</span></span>
<span data-ttu-id="184f0-123">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="184f0-123">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184f0-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="184f0-124">-Namespace</span></span>
<span data-ttu-id="184f0-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="184f0-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184f0-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="184f0-126">-PartnerNamespace</span></span>
<span data-ttu-id="184f0-127">DR konfigurációs PartnerNamespace (PartnerNamespace [másodlagos névtér])</span><span class="sxs-lookup"><span data-stu-id="184f0-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="184f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="184f0-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="184f0-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184f0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="184f0-130">-ResourceId</span></span>
<span data-ttu-id="184f0-131">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="184f0-131">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184f0-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="184f0-132">-Confirm</span></span>
<span data-ttu-id="184f0-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="184f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="184f0-134">-WhatIf</span></span>
<span data-ttu-id="184f0-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="184f0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="184f0-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="184f0-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184f0-137">CommonParameters</span></span>
<span data-ttu-id="184f0-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="184f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="184f0-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="184f0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184f0-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="184f0-140">INPUTS</span></span>

### <span data-ttu-id="184f0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="184f0-141">System.String</span></span>
<span data-ttu-id="184f0-142">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="184f0-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="184f0-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="184f0-143">OUTPUTS</span></span>

### <span data-ttu-id="184f0-144">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="184f0-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="184f0-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="184f0-145">NOTES</span></span>

## <span data-ttu-id="184f0-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="184f0-146">RELATED LINKS</span></span>

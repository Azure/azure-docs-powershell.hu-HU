---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: feeb47a1db28debfcfeb4e5d61c22e15db66b799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493788"
---
# <span data-ttu-id="f5e71-101">New-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5e71-101">New-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="f5e71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5e71-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e71-103">Új alias létrehozása (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="f5e71-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5e71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5e71-104">SYNTAX</span></span>

### <span data-ttu-id="f5e71-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5e71-105">GeoDRParameterSet (Default)</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5e71-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f5e71-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5e71-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5e71-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5e71-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5e71-108">DESCRIPTION</span></span>
<span data-ttu-id="f5e71-109">A **New-AzureRmEventHubGeoDRConfiguration** parancsmag új aliast hoz létre (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="f5e71-109">The **New-AzureRmEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f5e71-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f5e71-110">EXAMPLES</span></span>

### <span data-ttu-id="f5e71-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f5e71-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="f5e71-112">"SampleDRCongifName" aliast hoz létre "SampleNamespace_Primary" elsődleges névtérrel, "SampleNamespace_Secondary" másodlagos névtérrel</span><span class="sxs-lookup"><span data-stu-id="f5e71-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="f5e71-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5e71-113">PARAMETERS</span></span>

### <span data-ttu-id="f5e71-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="f5e71-114">-AlternateName</span></span>
<span data-ttu-id="f5e71-115">Az elsődleges névtérként használt DR-AlternateName megadásához szükséges beállítások</span><span class="sxs-lookup"><span data-stu-id="f5e71-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e71-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5e71-116">-AsJob</span></span>
<span data-ttu-id="f5e71-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f5e71-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5e71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e71-118">-DefaultProfile</span></span>
<span data-ttu-id="f5e71-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5e71-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5e71-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5e71-120">-InputObject</span></span>
<span data-ttu-id="f5e71-121">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="f5e71-121">Namespace Object</span></span>

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

### <span data-ttu-id="f5e71-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5e71-122">-Name</span></span>
<span data-ttu-id="f5e71-123">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="f5e71-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="f5e71-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5e71-124">-Namespace</span></span>
<span data-ttu-id="f5e71-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f5e71-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e71-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="f5e71-126">-PartnerNamespace</span></span>
<span data-ttu-id="f5e71-127">DR konfigurációs PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="f5e71-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="f5e71-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e71-128">-ResourceGroupName</span></span>
<span data-ttu-id="f5e71-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f5e71-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e71-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5e71-130">-ResourceId</span></span>
<span data-ttu-id="f5e71-131">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="f5e71-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="f5e71-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5e71-132">-Confirm</span></span>
<span data-ttu-id="f5e71-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5e71-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5e71-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5e71-134">-WhatIf</span></span>
<span data-ttu-id="f5e71-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5e71-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5e71-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5e71-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5e71-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e71-137">CommonParameters</span></span>
<span data-ttu-id="f5e71-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5e71-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f5e71-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e71-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e71-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5e71-140">INPUTS</span></span>

### <span data-ttu-id="f5e71-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f5e71-141">System.String</span></span>
<span data-ttu-id="f5e71-142">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f5e71-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="f5e71-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5e71-143">OUTPUTS</span></span>

### <span data-ttu-id="f5e71-144">Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f5e71-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="f5e71-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5e71-145">NOTES</span></span>

## <span data-ttu-id="f5e71-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5e71-146">RELATED LINKS</span></span>

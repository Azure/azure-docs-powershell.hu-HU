---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e5623ed840b9b1d2a7f75150fa686d6f488dc2ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494344"
---
# <span data-ttu-id="e4325-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4325-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="e4325-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4325-102">SYNOPSIS</span></span>
<span data-ttu-id="e4325-103">Az elsődleges vagy másodlagos névtérhez tartozó alias (katasztrófa-helyreállítási konfiguráció) beolvasása</span><span class="sxs-lookup"><span data-stu-id="e4325-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4325-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4325-104">SYNTAX</span></span>

### <span data-ttu-id="e4325-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4325-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4325-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e4325-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4325-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4325-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4325-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4325-108">DESCRIPTION</span></span>
<span data-ttu-id="e4325-109">A **Get-AzureRmServiceBusGeoDRConfiguration** lekéri az aliast (katasztrófa-helyreállítási konfiguráció) az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="e4325-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="e4325-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e4325-110">EXAMPLES</span></span>

### <span data-ttu-id="e4325-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e4325-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="e4325-112">Az elsődleges névtér "SampleDRCongifName" konfigurációjának lekérése "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="e4325-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="e4325-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4325-113">PARAMETERS</span></span>

### <span data-ttu-id="e4325-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4325-114">-DefaultProfile</span></span>
<span data-ttu-id="e4325-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4325-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4325-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4325-116">-InputObject</span></span>
<span data-ttu-id="e4325-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="e4325-117">Namespace Object</span></span>

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

### <span data-ttu-id="e4325-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4325-118">-Name</span></span>
<span data-ttu-id="e4325-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="e4325-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4325-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e4325-120">-Namespace</span></span>
<span data-ttu-id="e4325-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="e4325-121">Namespace Name</span></span>

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

### <span data-ttu-id="e4325-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4325-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4325-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e4325-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e4325-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4325-124">-ResourceId</span></span>
<span data-ttu-id="e4325-125">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="e4325-125">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4325-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4325-126">CommonParameters</span></span>
<span data-ttu-id="e4325-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4325-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e4325-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4325-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4325-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4325-129">INPUTS</span></span>

### <span data-ttu-id="e4325-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e4325-130">System.String</span></span>
<span data-ttu-id="e4325-131">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e4325-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="e4325-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4325-132">OUTPUTS</span></span>

### <span data-ttu-id="e4325-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.5.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e4325-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="e4325-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4325-134">NOTES</span></span>

## <span data-ttu-id="e4325-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4325-135">RELATED LINKS</span></span>

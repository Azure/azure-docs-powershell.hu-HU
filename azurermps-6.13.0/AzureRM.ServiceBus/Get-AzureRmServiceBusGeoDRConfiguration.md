---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 7d3635b33e96052c42ca77384d2f138af5cc0d5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501067"
---
# <span data-ttu-id="88e85-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="88e85-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="88e85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88e85-102">SYNOPSIS</span></span>
<span data-ttu-id="88e85-103">Az elsődleges vagy másodlagos névtérhez tartozó alias (katasztrófa-helyreállítási konfiguráció) beolvasása</span><span class="sxs-lookup"><span data-stu-id="88e85-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88e85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88e85-104">SYNTAX</span></span>

### <span data-ttu-id="88e85-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88e85-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88e85-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="88e85-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88e85-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88e85-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88e85-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="88e85-108">DESCRIPTION</span></span>
<span data-ttu-id="88e85-109">A **Get-AzureRmServiceBusGeoDRConfiguration** lekéri az aliast (katasztrófa-helyreállítási konfiguráció) az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="88e85-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="88e85-110">Példák</span><span class="sxs-lookup"><span data-stu-id="88e85-110">EXAMPLES</span></span>

### <span data-ttu-id="88e85-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="88e85-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="88e85-112">Az elsődleges névtér "SampleDRCongifName" konfigurációjának lekérése "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="88e85-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="88e85-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88e85-113">PARAMETERS</span></span>

### <span data-ttu-id="88e85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e85-114">-DefaultProfile</span></span>
<span data-ttu-id="88e85-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88e85-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e85-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88e85-116">-InputObject</span></span>
<span data-ttu-id="88e85-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="88e85-117">Namespace Object</span></span>

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

### <span data-ttu-id="88e85-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88e85-118">-Name</span></span>
<span data-ttu-id="88e85-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="88e85-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="88e85-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="88e85-120">-Namespace</span></span>
<span data-ttu-id="88e85-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="88e85-121">Namespace Name</span></span>

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

### <span data-ttu-id="88e85-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e85-122">-ResourceGroupName</span></span>
<span data-ttu-id="88e85-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="88e85-123">Resource Group Name</span></span>

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

### <span data-ttu-id="88e85-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88e85-124">-ResourceId</span></span>
<span data-ttu-id="88e85-125">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="88e85-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88e85-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e85-126">CommonParameters</span></span>
<span data-ttu-id="88e85-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88e85-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e85-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e85-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e85-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88e85-129">INPUTS</span></span>

### <span data-ttu-id="88e85-130">System. String</span><span class="sxs-lookup"><span data-stu-id="88e85-130">System.String</span></span>

### <span data-ttu-id="88e85-131">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="88e85-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="88e85-132">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="88e85-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="88e85-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88e85-133">OUTPUTS</span></span>

### <span data-ttu-id="88e85-134">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="88e85-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="88e85-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88e85-135">NOTES</span></span>

## <span data-ttu-id="88e85-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88e85-136">RELATED LINKS</span></span>

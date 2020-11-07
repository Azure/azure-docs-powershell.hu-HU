---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: fd87311c59c0889a57cb22eb08aba855e5c3b49c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669210"
---
# <span data-ttu-id="80956-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="80956-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="80956-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80956-102">SYNOPSIS</span></span>
<span data-ttu-id="80956-103">Az elsődleges vagy másodlagos névtérhez tartozó alias (katasztrófa-helyreállítási konfiguráció) beolvasása</span><span class="sxs-lookup"><span data-stu-id="80956-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="80956-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80956-104">SYNTAX</span></span>

### <span data-ttu-id="80956-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80956-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80956-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="80956-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80956-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80956-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80956-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="80956-108">DESCRIPTION</span></span>
<span data-ttu-id="80956-109">A **Get-AzServiceBusGeoDRConfiguration** lekéri az aliast (katasztrófa-helyreállítási konfiguráció) az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="80956-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="80956-110">Példák</span><span class="sxs-lookup"><span data-stu-id="80956-110">EXAMPLES</span></span>

### <span data-ttu-id="80956-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="80956-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="80956-112">Az elsődleges névtér "SampleDRCongifName" konfigurációjának lekérése "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="80956-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="80956-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80956-113">PARAMETERS</span></span>

### <span data-ttu-id="80956-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80956-114">-DefaultProfile</span></span>
<span data-ttu-id="80956-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80956-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80956-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80956-116">-InputObject</span></span>
<span data-ttu-id="80956-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="80956-117">Namespace Object</span></span>

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

### <span data-ttu-id="80956-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="80956-118">-Name</span></span>
<span data-ttu-id="80956-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="80956-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="80956-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="80956-120">-Namespace</span></span>
<span data-ttu-id="80956-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="80956-121">Namespace Name</span></span>

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

### <span data-ttu-id="80956-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80956-122">-ResourceGroupName</span></span>
<span data-ttu-id="80956-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="80956-123">Resource Group Name</span></span>

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

### <span data-ttu-id="80956-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80956-124">-ResourceId</span></span>
<span data-ttu-id="80956-125">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="80956-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="80956-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80956-126">CommonParameters</span></span>
<span data-ttu-id="80956-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80956-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80956-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80956-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80956-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80956-129">INPUTS</span></span>

### <span data-ttu-id="80956-130">System. String</span><span class="sxs-lookup"><span data-stu-id="80956-130">System.String</span></span>

### <span data-ttu-id="80956-131">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="80956-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="80956-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80956-132">OUTPUTS</span></span>

### <span data-ttu-id="80956-133">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="80956-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="80956-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80956-134">NOTES</span></span>

## <span data-ttu-id="80956-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80956-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195655"
---
# <span data-ttu-id="48671-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="48671-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="48671-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48671-102">SYNOPSIS</span></span>
<span data-ttu-id="48671-103">Az elsődleges vagy másodlagos névtérhez tartozó alias (katasztrófa-helyreállítási konfiguráció) beolvasása</span><span class="sxs-lookup"><span data-stu-id="48671-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="48671-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48671-104">SYNTAX</span></span>

### <span data-ttu-id="48671-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48671-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48671-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="48671-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48671-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48671-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48671-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="48671-108">DESCRIPTION</span></span>
<span data-ttu-id="48671-109">A **Get-AzServiceBusGeoDRConfiguration** lekéri az aliast (katasztrófa-helyreállítási konfiguráció) az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="48671-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="48671-110">Példák</span><span class="sxs-lookup"><span data-stu-id="48671-110">EXAMPLES</span></span>

### <span data-ttu-id="48671-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="48671-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="48671-112">Az elsődleges névtér "SampleDRConfigName" konfigurációjának lekérése "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="48671-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="48671-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48671-113">PARAMETERS</span></span>

### <span data-ttu-id="48671-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48671-114">-DefaultProfile</span></span>
<span data-ttu-id="48671-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48671-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48671-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48671-116">-InputObject</span></span>
<span data-ttu-id="48671-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="48671-117">Namespace Object</span></span>

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

### <span data-ttu-id="48671-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48671-118">-Name</span></span>
<span data-ttu-id="48671-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="48671-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="48671-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="48671-120">-Namespace</span></span>
<span data-ttu-id="48671-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="48671-121">Namespace Name</span></span>

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

### <span data-ttu-id="48671-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48671-122">-ResourceGroupName</span></span>
<span data-ttu-id="48671-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="48671-123">Resource Group Name</span></span>

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

### <span data-ttu-id="48671-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48671-124">-ResourceId</span></span>
<span data-ttu-id="48671-125">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="48671-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="48671-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48671-126">CommonParameters</span></span>
<span data-ttu-id="48671-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48671-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48671-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48671-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48671-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48671-129">INPUTS</span></span>

### <span data-ttu-id="48671-130">System. String</span><span class="sxs-lookup"><span data-stu-id="48671-130">System.String</span></span>

### <span data-ttu-id="48671-131">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="48671-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="48671-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48671-132">OUTPUTS</span></span>

### <span data-ttu-id="48671-133">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="48671-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="48671-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48671-134">NOTES</span></span>

## <span data-ttu-id="48671-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48671-135">RELATED LINKS</span></span>
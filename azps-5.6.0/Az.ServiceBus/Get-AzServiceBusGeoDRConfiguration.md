---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 21ccb8a16ff3622e6661bd5548721d6d1227e7e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942209"
---
# <span data-ttu-id="6ccbb-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ccbb-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="6ccbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ccbb-102">SYNOPSIS</span></span>
<span data-ttu-id="6ccbb-103">Beolvassa az alias(katasztrófa-helyreállítási konfiguráció) beállítást az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="6ccbb-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="6ccbb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6ccbb-104">SYNTAX</span></span>

### <span data-ttu-id="6ccbb-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ccbb-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ccbb-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6ccbb-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ccbb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ccbb-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ccbb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6ccbb-108">DESCRIPTION</span></span>
<span data-ttu-id="6ccbb-109">A **Get-AzServiceBusGeoDRConfiguration** beolvassa az alias(Katasztrófa-helyreállítási konfiguráció) beállítást az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="6ccbb-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="6ccbb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6ccbb-110">EXAMPLES</span></span>

### <span data-ttu-id="6ccbb-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6ccbb-111">Example 1</span></span>
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

<span data-ttu-id="6ccbb-112">A "SampleDRConfigName" alias-konfiguráció lekérése az elsődleges névtér "SampleNamespace_Primary" esetén</span><span class="sxs-lookup"><span data-stu-id="6ccbb-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="6ccbb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ccbb-113">PARAMETERS</span></span>

### <span data-ttu-id="6ccbb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ccbb-114">-DefaultProfile</span></span>
<span data-ttu-id="6ccbb-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ccbb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ccbb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ccbb-116">-InputObject</span></span>
<span data-ttu-id="6ccbb-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="6ccbb-117">Namespace Object</span></span>

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

### <span data-ttu-id="6ccbb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6ccbb-118">-Name</span></span>
<span data-ttu-id="6ccbb-119">DR Configuration Name</span><span class="sxs-lookup"><span data-stu-id="6ccbb-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="6ccbb-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6ccbb-120">-Namespace</span></span>
<span data-ttu-id="6ccbb-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="6ccbb-121">Namespace Name</span></span>

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

### <span data-ttu-id="6ccbb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ccbb-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ccbb-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6ccbb-123">Resource Group Name</span></span>

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

### <span data-ttu-id="6ccbb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ccbb-124">-ResourceId</span></span>
<span data-ttu-id="6ccbb-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="6ccbb-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="6ccbb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ccbb-126">CommonParameters</span></span>
<span data-ttu-id="6ccbb-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ccbb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ccbb-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ccbb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ccbb-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ccbb-129">INPUTS</span></span>

### <span data-ttu-id="6ccbb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6ccbb-130">System.String</span></span>

### <span data-ttu-id="6ccbb-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="6ccbb-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="6ccbb-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ccbb-132">OUTPUTS</span></span>

### <span data-ttu-id="6ccbb-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="6ccbb-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="6ccbb-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6ccbb-134">NOTES</span></span>

## <span data-ttu-id="6ccbb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ccbb-135">RELATED LINKS</span></span>

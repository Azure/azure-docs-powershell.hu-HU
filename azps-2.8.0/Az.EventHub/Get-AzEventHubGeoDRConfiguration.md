---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 4c9d4d1a4ec79da0677bc44d53a3843aa9a6d102
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666494"
---
# <span data-ttu-id="9e6f4-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e6f4-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="9e6f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e6f4-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6f4-103">Az elsődleges vagy másodlagos névtérhez tartozó alias (katasztrófa-helyreállítási konfiguráció) beolvasása</span><span class="sxs-lookup"><span data-stu-id="9e6f4-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="9e6f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e6f4-104">SYNTAX</span></span>

### <span data-ttu-id="9e6f4-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e6f4-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e6f4-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9e6f4-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e6f4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e6f4-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e6f4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e6f4-108">DESCRIPTION</span></span>
<span data-ttu-id="9e6f4-109">A **Get-AzEventHubGeoDRConfiguration** lekéri az aliast (katasztrófa-helyreállítási konfiguráció) az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="9e6f4-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="9e6f4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9e6f4-110">EXAMPLES</span></span>

### <span data-ttu-id="9e6f4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9e6f4-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="9e6f4-112">Az elsődleges névtér "SampleDRConfigName" konfigurációjának lekérése "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="9e6f4-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="9e6f4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e6f4-113">PARAMETERS</span></span>

### <span data-ttu-id="9e6f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6f4-114">-DefaultProfile</span></span>
<span data-ttu-id="9e6f4-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e6f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e6f4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e6f4-116">-InputObject</span></span>
<span data-ttu-id="9e6f4-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="9e6f4-117">Namespace Object</span></span>

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

### <span data-ttu-id="9e6f4-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e6f4-118">-Name</span></span>
<span data-ttu-id="9e6f4-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="9e6f4-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="9e6f4-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9e6f4-120">-Namespace</span></span>
<span data-ttu-id="9e6f4-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="9e6f4-121">Namespace Name</span></span>

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

### <span data-ttu-id="9e6f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e6f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="9e6f4-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9e6f4-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9e6f4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e6f4-124">-ResourceId</span></span>
<span data-ttu-id="9e6f4-125">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="9e6f4-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="9e6f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6f4-126">CommonParameters</span></span>
<span data-ttu-id="9e6f4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e6f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6f4-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6f4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6f4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e6f4-129">INPUTS</span></span>

### <span data-ttu-id="9e6f4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9e6f4-130">System.String</span></span>

### <span data-ttu-id="9e6f4-131">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9e6f4-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="9e6f4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e6f4-132">OUTPUTS</span></span>

### <span data-ttu-id="9e6f4-133">Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9e6f4-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="9e6f4-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e6f4-134">NOTES</span></span>

## <span data-ttu-id="9e6f4-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e6f4-135">RELATED LINKS</span></span>

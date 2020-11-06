---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 40a80a975de56a867f0dcbc34aea0e46d42a155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495120"
---
# <span data-ttu-id="643ba-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="643ba-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="643ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="643ba-102">SYNOPSIS</span></span>
<span data-ttu-id="643ba-103">Az elsődleges vagy másodlagos névtérhez tartozó alias (katasztrófa-helyreállítási konfiguráció) beolvasása</span><span class="sxs-lookup"><span data-stu-id="643ba-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="643ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="643ba-104">SYNTAX</span></span>

### <span data-ttu-id="643ba-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="643ba-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="643ba-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="643ba-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="643ba-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="643ba-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="643ba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="643ba-108">DESCRIPTION</span></span>
<span data-ttu-id="643ba-109">A **Get-AzureRmEventHubGeoDRConfiguration** lekéri az aliast (katasztrófa-helyreállítási konfiguráció) az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="643ba-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="643ba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="643ba-110">EXAMPLES</span></span>

### <span data-ttu-id="643ba-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="643ba-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="643ba-112">Az elsődleges névtér "SampleDRCongifName" konfigurációjának lekérése "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="643ba-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="643ba-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="643ba-113">PARAMETERS</span></span>

### <span data-ttu-id="643ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643ba-114">-DefaultProfile</span></span>
<span data-ttu-id="643ba-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="643ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="643ba-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="643ba-116">-InputObject</span></span>
<span data-ttu-id="643ba-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="643ba-117">Namespace Object</span></span>

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

### <span data-ttu-id="643ba-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="643ba-118">-Name</span></span>
<span data-ttu-id="643ba-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="643ba-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="643ba-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="643ba-120">-Namespace</span></span>
<span data-ttu-id="643ba-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="643ba-121">Namespace Name</span></span>

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

### <span data-ttu-id="643ba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="643ba-122">-ResourceGroupName</span></span>
<span data-ttu-id="643ba-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="643ba-123">Resource Group Name</span></span>

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

### <span data-ttu-id="643ba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="643ba-124">-ResourceId</span></span>
<span data-ttu-id="643ba-125">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="643ba-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="643ba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643ba-126">CommonParameters</span></span>
<span data-ttu-id="643ba-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="643ba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643ba-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="643ba-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643ba-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="643ba-129">INPUTS</span></span>

### <span data-ttu-id="643ba-130">System. String</span><span class="sxs-lookup"><span data-stu-id="643ba-130">System.String</span></span>

### <span data-ttu-id="643ba-131">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="643ba-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="643ba-132">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="643ba-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="643ba-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="643ba-133">OUTPUTS</span></span>

### <span data-ttu-id="643ba-134">Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="643ba-134">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="643ba-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="643ba-135">NOTES</span></span>

## <span data-ttu-id="643ba-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="643ba-136">RELATED LINKS</span></span>

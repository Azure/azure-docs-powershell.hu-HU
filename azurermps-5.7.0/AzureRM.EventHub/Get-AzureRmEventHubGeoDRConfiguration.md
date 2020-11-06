---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 8c48e6dc8fb095258953a57498b76219dec4ef42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502587"
---
# <span data-ttu-id="a81b5-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="a81b5-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="a81b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a81b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a81b5-103">Az elsődleges vagy másodlagos névtérhez tartozó alias (katasztrófa-helyreállítási konfiguráció) beolvasása</span><span class="sxs-lookup"><span data-stu-id="a81b5-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a81b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a81b5-104">SYNTAX</span></span>

### <span data-ttu-id="a81b5-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a81b5-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a81b5-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a81b5-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a81b5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a81b5-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a81b5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a81b5-108">DESCRIPTION</span></span>
<span data-ttu-id="a81b5-109">A **Get-AzureRmEventHubGeoDRConfiguration** lekéri az aliast (katasztrófa-helyreállítási konfiguráció) az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="a81b5-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="a81b5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a81b5-110">EXAMPLES</span></span>

### <span data-ttu-id="a81b5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a81b5-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="a81b5-112">Az elsődleges névtér "SampleDRCongifName" konfigurációjának lekérése "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="a81b5-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="a81b5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a81b5-113">PARAMETERS</span></span>

### <span data-ttu-id="a81b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a81b5-114">-DefaultProfile</span></span>
<span data-ttu-id="a81b5-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a81b5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a81b5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a81b5-116">-InputObject</span></span>
<span data-ttu-id="a81b5-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="a81b5-117">Namespace Object</span></span>

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

### <span data-ttu-id="a81b5-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a81b5-118">-Name</span></span>
<span data-ttu-id="a81b5-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="a81b5-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="a81b5-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a81b5-120">-Namespace</span></span>
<span data-ttu-id="a81b5-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="a81b5-121">Namespace Name</span></span>

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

### <span data-ttu-id="a81b5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a81b5-122">-ResourceGroupName</span></span>
<span data-ttu-id="a81b5-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a81b5-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a81b5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a81b5-124">-ResourceId</span></span>
<span data-ttu-id="a81b5-125">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="a81b5-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="a81b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a81b5-126">CommonParameters</span></span>
<span data-ttu-id="a81b5-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a81b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a81b5-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a81b5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a81b5-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a81b5-129">INPUTS</span></span>

### <span data-ttu-id="a81b5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a81b5-130">System.String</span></span>
<span data-ttu-id="a81b5-131">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a81b5-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a81b5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a81b5-132">OUTPUTS</span></span>

### <span data-ttu-id="a81b5-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes, Microsoft. Azure. commands. EventHub, Version = 0.5.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a81b5-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a81b5-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a81b5-134">NOTES</span></span>

## <span data-ttu-id="a81b5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a81b5-135">RELATED LINKS</span></span>

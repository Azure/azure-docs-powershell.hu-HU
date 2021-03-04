---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: b2003821178875777240cb43bcdc1e9e53784fc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921241"
---
# <span data-ttu-id="c1bbf-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1bbf-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="c1bbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="c1bbf-103">Beolvassa az alias(katasztrófa-helyreállítási konfiguráció) beállítást az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="c1bbf-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c1bbf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c1bbf-104">SYNTAX</span></span>

### <span data-ttu-id="c1bbf-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1bbf-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1bbf-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c1bbf-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1bbf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1bbf-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1bbf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c1bbf-108">DESCRIPTION</span></span>
<span data-ttu-id="c1bbf-109">A **Get-AzEventHubGeoDRConfiguration** beolvassa az Alias(Katasztrófa-helyreállítás konfiguráció) beállítást az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="c1bbf-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c1bbf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c1bbf-110">EXAMPLES</span></span>

### <span data-ttu-id="c1bbf-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c1bbf-111">Example 1</span></span>
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

<span data-ttu-id="c1bbf-112">A "SampleDRConfigName" alias-konfiguráció lekérése az elsődleges névtér "SampleNamespace_Primary" esetén</span><span class="sxs-lookup"><span data-stu-id="c1bbf-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="c1bbf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1bbf-113">PARAMETERS</span></span>

### <span data-ttu-id="c1bbf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1bbf-114">-DefaultProfile</span></span>
<span data-ttu-id="c1bbf-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1bbf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1bbf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1bbf-116">-InputObject</span></span>
<span data-ttu-id="c1bbf-117">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="c1bbf-117">Namespace Object</span></span>

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

### <span data-ttu-id="c1bbf-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c1bbf-118">-Name</span></span>
<span data-ttu-id="c1bbf-119">DR Configuration Name</span><span class="sxs-lookup"><span data-stu-id="c1bbf-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="c1bbf-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c1bbf-120">-Namespace</span></span>
<span data-ttu-id="c1bbf-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="c1bbf-121">Namespace Name</span></span>

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

### <span data-ttu-id="c1bbf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1bbf-122">-ResourceGroupName</span></span>
<span data-ttu-id="c1bbf-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c1bbf-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c1bbf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1bbf-124">-ResourceId</span></span>
<span data-ttu-id="c1bbf-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="c1bbf-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="c1bbf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1bbf-126">CommonParameters</span></span>
<span data-ttu-id="c1bbf-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1bbf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1bbf-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1bbf-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1bbf-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1bbf-129">INPUTS</span></span>

### <span data-ttu-id="c1bbf-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c1bbf-130">System.String</span></span>

### <span data-ttu-id="c1bbf-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c1bbf-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c1bbf-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1bbf-132">OUTPUTS</span></span>

### <span data-ttu-id="c1bbf-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c1bbf-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="c1bbf-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c1bbf-134">NOTES</span></span>

## <span data-ttu-id="c1bbf-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1bbf-135">RELATED LINKS</span></span>

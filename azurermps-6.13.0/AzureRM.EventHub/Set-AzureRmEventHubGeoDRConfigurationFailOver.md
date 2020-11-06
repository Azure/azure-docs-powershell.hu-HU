---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 84a101a427fc5541d4888a0b4deb4c5e3880b1d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496184"
---
# <span data-ttu-id="e5ca9-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="e5ca9-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="e5ca9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ca9-103">A GEO DR feladatátvételt hívja meg, és a másodlagos névtérre irányítja át az aliast.</span><span class="sxs-lookup"><span data-stu-id="e5ca9-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5ca9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5ca9-104">SYNTAX</span></span>

### <span data-ttu-id="e5ca9-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5ca9-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ca9-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e5ca9-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5ca9-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5ca9-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5ca9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5ca9-108">DESCRIPTION</span></span>
<span data-ttu-id="e5ca9-109">A **set-AzureRmEventHubGeoDRConfigurationFailOver** PARANCSMAG ENVOKES geo Dr feladatátvételi lehetőséget, és átállíthatja az aliast, hogy a másodlagos névtérre mutasson</span><span class="sxs-lookup"><span data-stu-id="e5ca9-109">The **Set-AzureRmEventHubGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="e5ca9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e5ca9-110">EXAMPLES</span></span>

### <span data-ttu-id="e5ca9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e5ca9-111">Example 1</span></span>
```
PS C:\>Set-AzureRmEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="e5ca9-112">A feladatátvételt a "SampleDRCongifName" aliasra hívja, átirányítja, majd a másodlagos névtér "SampleNamespace_Secondary" elemre mutat.</span><span class="sxs-lookup"><span data-stu-id="e5ca9-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="e5ca9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5ca9-113">PARAMETERS</span></span>

### <span data-ttu-id="e5ca9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ca9-114">-DefaultProfile</span></span>
<span data-ttu-id="e5ca9-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5ca9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5ca9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5ca9-116">-InputObject</span></span>
<span data-ttu-id="e5ca9-117">Eventhub GeoDR konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="e5ca9-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5ca9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5ca9-118">-Name</span></span>
<span data-ttu-id="e5ca9-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="e5ca9-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5ca9-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e5ca9-120">-Namespace</span></span>
<span data-ttu-id="e5ca9-121">Névtér neve – másodlagos névtér</span><span class="sxs-lookup"><span data-stu-id="e5ca9-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="e5ca9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5ca9-122">-PassThru</span></span>
<span data-ttu-id="e5ca9-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e5ca9-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5ca9-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e5ca9-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ca9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5ca9-125">-ResourceGroupName</span></span>
<span data-ttu-id="e5ca9-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e5ca9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e5ca9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5ca9-127">-ResourceId</span></span>
<span data-ttu-id="e5ca9-128">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="e5ca9-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5ca9-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5ca9-129">-Confirm</span></span>
<span data-ttu-id="e5ca9-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5ca9-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ca9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5ca9-131">-WhatIf</span></span>
<span data-ttu-id="e5ca9-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5ca9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5ca9-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5ca9-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ca9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ca9-134">CommonParameters</span></span>
<span data-ttu-id="e5ca9-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5ca9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ca9-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5ca9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ca9-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5ca9-137">INPUTS</span></span>

### <span data-ttu-id="e5ca9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e5ca9-138">System.String</span></span>

### <span data-ttu-id="e5ca9-139">Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e5ca9-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="e5ca9-140">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e5ca9-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e5ca9-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5ca9-141">OUTPUTS</span></span>

### <span data-ttu-id="e5ca9-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5ca9-142">System.Boolean</span></span>

## <span data-ttu-id="e5ca9-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5ca9-143">NOTES</span></span>

## <span data-ttu-id="e5ca9-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5ca9-144">RELATED LINKS</span></span>

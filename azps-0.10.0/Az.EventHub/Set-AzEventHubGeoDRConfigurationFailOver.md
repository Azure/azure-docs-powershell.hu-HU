---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 6569c5081ec92e20682edf63c09f1b4319d4c038
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842257"
---
# <span data-ttu-id="8cf77-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="8cf77-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="8cf77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cf77-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf77-103">A GEO DR feladatátvételt hívja meg, és a másodlagos névtérre irányítja át az aliast.</span><span class="sxs-lookup"><span data-stu-id="8cf77-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="8cf77-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cf77-104">SYNTAX</span></span>

### <span data-ttu-id="8cf77-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8cf77-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf77-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8cf77-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf77-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cf77-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf77-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cf77-108">DESCRIPTION</span></span>
<span data-ttu-id="8cf77-109">A **set-AzEventHubGeoDRConfigurationFailOver** PARANCSMAG a Geo Dr feladatátvételt hívja meg, és átadja a másodlagos névtérre mutató aliast.</span><span class="sxs-lookup"><span data-stu-id="8cf77-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="8cf77-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8cf77-110">EXAMPLES</span></span>

### <span data-ttu-id="8cf77-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8cf77-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="8cf77-112">A feladatátvételt a "SampleDRConfigName" aliasra hívja, átirányítja, majd a másodlagos névtér "SampleNamespace_Secondary" elemre mutat.</span><span class="sxs-lookup"><span data-stu-id="8cf77-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="8cf77-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cf77-113">PARAMETERS</span></span>

### <span data-ttu-id="8cf77-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf77-114">-DefaultProfile</span></span>
<span data-ttu-id="8cf77-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8cf77-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cf77-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cf77-116">-InputObject</span></span>
<span data-ttu-id="8cf77-117">Eventhub GeoDR konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="8cf77-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="8cf77-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8cf77-118">-Name</span></span>
<span data-ttu-id="8cf77-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="8cf77-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="8cf77-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8cf77-120">-Namespace</span></span>
<span data-ttu-id="8cf77-121">Névtér neve – másodlagos névtér</span><span class="sxs-lookup"><span data-stu-id="8cf77-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="8cf77-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cf77-122">-PassThru</span></span>
<span data-ttu-id="8cf77-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="8cf77-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8cf77-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8cf77-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8cf77-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf77-125">-ResourceGroupName</span></span>
<span data-ttu-id="8cf77-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="8cf77-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8cf77-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cf77-127">-ResourceId</span></span>
<span data-ttu-id="8cf77-128">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="8cf77-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="8cf77-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8cf77-129">-Confirm</span></span>
<span data-ttu-id="8cf77-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8cf77-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf77-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf77-131">-WhatIf</span></span>
<span data-ttu-id="8cf77-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8cf77-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf77-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8cf77-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf77-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf77-134">CommonParameters</span></span>
<span data-ttu-id="8cf77-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cf77-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf77-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf77-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf77-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cf77-137">INPUTS</span></span>

### <span data-ttu-id="8cf77-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8cf77-138">System.String</span></span>

### <span data-ttu-id="8cf77-139">Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="8cf77-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="8cf77-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cf77-140">OUTPUTS</span></span>

### <span data-ttu-id="8cf77-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8cf77-141">System.Boolean</span></span>

## <span data-ttu-id="8cf77-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cf77-142">NOTES</span></span>

## <span data-ttu-id="8cf77-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cf77-143">RELATED LINKS</span></span>

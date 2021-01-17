---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4ee96fbe20fca3f0af1f0bb9604f178b912d0ea2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466136"
---
# <span data-ttu-id="25e23-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="25e23-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="25e23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e23-102">SYNOPSIS</span></span>
<span data-ttu-id="25e23-103">A GEO DR feladatátvételének meghívása és az alias újrakonfigurálása a másodlagos névtérre</span><span class="sxs-lookup"><span data-stu-id="25e23-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="25e23-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25e23-104">SYNTAX</span></span>

### <span data-ttu-id="25e23-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25e23-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e23-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="25e23-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e23-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25e23-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25e23-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25e23-108">DESCRIPTION</span></span>
<span data-ttu-id="25e23-109">A **Set-AzEventHubGeoDRConfigurationFailOver** parancsmag meghívja a GEO DR feladatátvételt, és újrakonfigurálja az aliast úgy, hogy a másodlagos névtérre mutasson.</span><span class="sxs-lookup"><span data-stu-id="25e23-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="25e23-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25e23-110">EXAMPLES</span></span>

### <span data-ttu-id="25e23-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="25e23-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="25e23-112">A "SampleDRConfigName" alias felett meghívja a feladatátvételi rekordot, újrakonfigurál, és a Másodlagos névtér "SampleNamespace_Secondary" névre mutat</span><span class="sxs-lookup"><span data-stu-id="25e23-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="25e23-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25e23-113">PARAMETERS</span></span>

### <span data-ttu-id="25e23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e23-114">-DefaultProfile</span></span>
<span data-ttu-id="25e23-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25e23-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e23-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25e23-116">-InputObject</span></span>
<span data-ttu-id="25e23-117">Eventhub GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="25e23-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="25e23-118">-Name</span><span class="sxs-lookup"><span data-stu-id="25e23-118">-Name</span></span>
<span data-ttu-id="25e23-119">DR Configuration Name</span><span class="sxs-lookup"><span data-stu-id="25e23-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="25e23-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="25e23-120">-Namespace</span></span>
<span data-ttu-id="25e23-121">Namespace Name - Secondary Namespace</span><span class="sxs-lookup"><span data-stu-id="25e23-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="25e23-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25e23-122">-PassThru</span></span>
<span data-ttu-id="25e23-123">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="25e23-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25e23-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="25e23-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25e23-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e23-125">-ResourceGroupName</span></span>
<span data-ttu-id="25e23-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="25e23-126">Resource Group Name</span></span>

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

### <span data-ttu-id="25e23-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25e23-127">-ResourceId</span></span>
<span data-ttu-id="25e23-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="25e23-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="25e23-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25e23-129">-Confirm</span></span>
<span data-ttu-id="25e23-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="25e23-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e23-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25e23-131">-WhatIf</span></span>
<span data-ttu-id="25e23-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="25e23-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25e23-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25e23-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e23-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e23-134">CommonParameters</span></span>
<span data-ttu-id="25e23-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e23-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e23-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25e23-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e23-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25e23-137">INPUTS</span></span>

### <span data-ttu-id="25e23-138">System.String</span><span class="sxs-lookup"><span data-stu-id="25e23-138">System.String</span></span>

### <span data-ttu-id="25e23-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="25e23-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="25e23-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25e23-140">OUTPUTS</span></span>

### <span data-ttu-id="25e23-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25e23-141">System.Boolean</span></span>

## <span data-ttu-id="25e23-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25e23-142">NOTES</span></span>

## <span data-ttu-id="25e23-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25e23-143">RELATED LINKS</span></span>

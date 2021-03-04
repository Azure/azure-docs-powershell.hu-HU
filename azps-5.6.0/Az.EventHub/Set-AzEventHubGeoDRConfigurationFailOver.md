---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: d68fe2005f827d55b57ecedb7e21fd11b0cc9978
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935761"
---
# <span data-ttu-id="d0798-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="d0798-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="d0798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0798-102">SYNOPSIS</span></span>
<span data-ttu-id="d0798-103">A GEO DR feladatátvételének meghívása és az alias újrakonfigurálása a másodlagos névtérre</span><span class="sxs-lookup"><span data-stu-id="d0798-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="d0798-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0798-104">SYNTAX</span></span>

### <span data-ttu-id="d0798-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0798-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0798-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0798-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0798-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0798-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0798-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0798-108">DESCRIPTION</span></span>
<span data-ttu-id="d0798-109">A **Set-AzEventHubGeoDRConfigurationFailOver** parancsmag meghívja a GEO DR feladatátvételt, és újrakonfigurálja az aliast úgy, hogy a másodlagos névtérre mutasson.</span><span class="sxs-lookup"><span data-stu-id="d0798-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="d0798-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0798-110">EXAMPLES</span></span>

### <span data-ttu-id="d0798-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d0798-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="d0798-112">A "SampleDRConfigName" alias felett meghívja a feladatátvételi rekordot, újrakonfigurál, és a Másodlagos névtér "SampleNamespace_Secondary" névre mutat</span><span class="sxs-lookup"><span data-stu-id="d0798-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="d0798-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0798-113">PARAMETERS</span></span>

### <span data-ttu-id="d0798-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0798-114">-DefaultProfile</span></span>
<span data-ttu-id="d0798-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0798-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0798-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0798-116">-InputObject</span></span>
<span data-ttu-id="d0798-117">Eventhub GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="d0798-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="d0798-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d0798-118">-Name</span></span>
<span data-ttu-id="d0798-119">DR Configuration Name</span><span class="sxs-lookup"><span data-stu-id="d0798-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="d0798-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d0798-120">-Namespace</span></span>
<span data-ttu-id="d0798-121">Namespace Name - Secondary Namespace</span><span class="sxs-lookup"><span data-stu-id="d0798-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="d0798-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0798-122">-PassThru</span></span>
<span data-ttu-id="d0798-123">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="d0798-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d0798-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d0798-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d0798-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0798-125">-ResourceGroupName</span></span>
<span data-ttu-id="d0798-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d0798-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d0798-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0798-127">-ResourceId</span></span>
<span data-ttu-id="d0798-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="d0798-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="d0798-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0798-129">-Confirm</span></span>
<span data-ttu-id="d0798-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d0798-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0798-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0798-131">-WhatIf</span></span>
<span data-ttu-id="d0798-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d0798-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0798-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0798-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0798-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0798-134">CommonParameters</span></span>
<span data-ttu-id="d0798-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0798-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0798-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0798-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0798-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0798-137">INPUTS</span></span>

### <span data-ttu-id="d0798-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d0798-138">System.String</span></span>

### <span data-ttu-id="d0798-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="d0798-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="d0798-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0798-140">OUTPUTS</span></span>

### <span data-ttu-id="d0798-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d0798-141">System.Boolean</span></span>

## <span data-ttu-id="d0798-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0798-142">NOTES</span></span>

## <span data-ttu-id="d0798-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0798-143">RELATED LINKS</span></span>

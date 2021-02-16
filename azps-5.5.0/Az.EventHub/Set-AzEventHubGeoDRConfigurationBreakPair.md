---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167587"
---
# <span data-ttu-id="5f9e5-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="5f9e5-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="5f9e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9e5-103">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja a módosítások elsődlegesről másodlagos névterekbe való replikálását.</span><span class="sxs-lookup"><span data-stu-id="5f9e5-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="5f9e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5f9e5-104">SYNTAX</span></span>

### <span data-ttu-id="5f9e5-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f9e5-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f9e5-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5f9e5-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f9e5-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f9e5-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f9e5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5f9e5-108">DESCRIPTION</span></span>
<span data-ttu-id="5f9e5-109">A **Set-AzEventHubGeoDRConfigurationBreakPair** parancsmag letiltja a katasztrófa-helyreállítást, és leállítja a módosítások elsődlegesről másodlagos névterekbe való replikálását.</span><span class="sxs-lookup"><span data-stu-id="5f9e5-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="5f9e5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5f9e5-110">EXAMPLES</span></span>

### <span data-ttu-id="5f9e5-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5f9e5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="5f9e5-112">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja a módosítások elsődlegesről másodlagos névterekbe való replikálását.</span><span class="sxs-lookup"><span data-stu-id="5f9e5-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="5f9e5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f9e5-113">PARAMETERS</span></span>

### <span data-ttu-id="5f9e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f9e5-114">-DefaultProfile</span></span>
<span data-ttu-id="5f9e5-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f9e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f9e5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f9e5-116">-InputObject</span></span>
<span data-ttu-id="5f9e5-117">Eventhub GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="5f9e5-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="5f9e5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5f9e5-118">-Name</span></span>
<span data-ttu-id="5f9e5-119">DR Configuration Name</span><span class="sxs-lookup"><span data-stu-id="5f9e5-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="5f9e5-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5f9e5-120">-Namespace</span></span>
<span data-ttu-id="5f9e5-121">Namespace Name - Primary Namespace</span><span class="sxs-lookup"><span data-stu-id="5f9e5-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="5f9e5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f9e5-122">-PassThru</span></span>
<span data-ttu-id="5f9e5-123">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="5f9e5-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5f9e5-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5f9e5-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5f9e5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f9e5-125">-ResourceGroupName</span></span>
<span data-ttu-id="5f9e5-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5f9e5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="5f9e5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f9e5-127">-ResourceId</span></span>
<span data-ttu-id="5f9e5-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="5f9e5-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="5f9e5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f9e5-129">-Confirm</span></span>
<span data-ttu-id="5f9e5-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5f9e5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f9e5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f9e5-131">-WhatIf</span></span>
<span data-ttu-id="5f9e5-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5f9e5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f9e5-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f9e5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f9e5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9e5-134">CommonParameters</span></span>
<span data-ttu-id="5f9e5-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f9e5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9e5-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f9e5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9e5-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f9e5-137">INPUTS</span></span>

### <span data-ttu-id="5f9e5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5f9e5-138">System.String</span></span>

### <span data-ttu-id="5f9e5-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5f9e5-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="5f9e5-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f9e5-140">OUTPUTS</span></span>

### <span data-ttu-id="5f9e5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5f9e5-141">System.Boolean</span></span>

## <span data-ttu-id="5f9e5-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5f9e5-142">NOTES</span></span>

## <span data-ttu-id="5f9e5-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f9e5-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017767"
---
# <span data-ttu-id="dd1b0-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="dd1b0-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="dd1b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1b0-103">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja az elsődlegestől a másodlagos névtérig történő módosítások replikálását.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="dd1b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd1b0-104">SYNTAX</span></span>

### <span data-ttu-id="dd1b0-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd1b0-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd1b0-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd1b0-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd1b0-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd1b0-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd1b0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd1b0-108">DESCRIPTION</span></span>
<span data-ttu-id="dd1b0-109">A **set-AzEventHubGeoDRConfigurationBreakPair** parancsmag letiltja a katasztrófa-helyreállítást, és leállítja az elsődlegestől a másodlagos névtérbe való replikálást.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="dd1b0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dd1b0-110">EXAMPLES</span></span>

### <span data-ttu-id="dd1b0-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dd1b0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="dd1b0-112">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja az elsődlegestől a másodlagos névtérig történő módosítások replikálását.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="dd1b0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd1b0-113">PARAMETERS</span></span>

### <span data-ttu-id="dd1b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd1b0-114">-DefaultProfile</span></span>
<span data-ttu-id="dd1b0-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd1b0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd1b0-116">-InputObject</span></span>
<span data-ttu-id="dd1b0-117">Eventhub GeoDR konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="dd1b0-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="dd1b0-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd1b0-118">-Name</span></span>
<span data-ttu-id="dd1b0-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="dd1b0-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="dd1b0-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd1b0-120">-Namespace</span></span>
<span data-ttu-id="dd1b0-121">Névtér neve – elsődleges névtér</span><span class="sxs-lookup"><span data-stu-id="dd1b0-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="dd1b0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd1b0-122">-PassThru</span></span>
<span data-ttu-id="dd1b0-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dd1b0-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dd1b0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd1b0-125">-ResourceGroupName</span></span>
<span data-ttu-id="dd1b0-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="dd1b0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="dd1b0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd1b0-127">-ResourceId</span></span>
<span data-ttu-id="dd1b0-128">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="dd1b0-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="dd1b0-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd1b0-129">-Confirm</span></span>
<span data-ttu-id="dd1b0-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd1b0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd1b0-131">-WhatIf</span></span>
<span data-ttu-id="dd1b0-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd1b0-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd1b0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd1b0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1b0-134">CommonParameters</span></span>
<span data-ttu-id="dd1b0-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd1b0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1b0-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd1b0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1b0-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd1b0-137">INPUTS</span></span>

### <span data-ttu-id="dd1b0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dd1b0-138">System.String</span></span>

### <span data-ttu-id="dd1b0-139">Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="dd1b0-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="dd1b0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd1b0-140">OUTPUTS</span></span>

### <span data-ttu-id="dd1b0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd1b0-141">System.Boolean</span></span>

## <span data-ttu-id="dd1b0-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd1b0-142">NOTES</span></span>

## <span data-ttu-id="dd1b0-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd1b0-143">RELATED LINKS</span></span>

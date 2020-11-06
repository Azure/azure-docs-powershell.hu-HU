---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 3ee0e251f4dd92b087343edc03e829e8032ee5c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496188"
---
# <span data-ttu-id="903c2-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="903c2-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="903c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="903c2-102">SYNOPSIS</span></span>
<span data-ttu-id="903c2-103">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja az elsődlegestől a másodlagos névtérig történő módosítások replikálását.</span><span class="sxs-lookup"><span data-stu-id="903c2-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="903c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="903c2-104">SYNTAX</span></span>

### <span data-ttu-id="903c2-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="903c2-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="903c2-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="903c2-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="903c2-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="903c2-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="903c2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="903c2-108">DESCRIPTION</span></span>
<span data-ttu-id="903c2-109">A **set-AzureRmEventHubGeoDRConfigurationBreakPair** parancsmag letiltja a katasztrófa-helyreállítást, és leállítja az elsődlegestől a másodlagos névtérbe való replikálást.</span><span class="sxs-lookup"><span data-stu-id="903c2-109">The **Set-AzureRmEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="903c2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="903c2-110">EXAMPLES</span></span>

### <span data-ttu-id="903c2-111">Például</span><span class="sxs-lookup"><span data-stu-id="903c2-111">Example</span></span>
```
PS C:\> Set-AzureRmEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="903c2-112">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja az elsődlegestől a másodlagos névtérig történő módosítások replikálását.</span><span class="sxs-lookup"><span data-stu-id="903c2-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="903c2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="903c2-113">PARAMETERS</span></span>

### <span data-ttu-id="903c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903c2-114">-DefaultProfile</span></span>
<span data-ttu-id="903c2-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="903c2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="903c2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="903c2-116">-InputObject</span></span>
<span data-ttu-id="903c2-117">Eventhub GeoDR konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="903c2-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="903c2-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="903c2-118">-Name</span></span>
<span data-ttu-id="903c2-119">DR konfigurációs név</span><span class="sxs-lookup"><span data-stu-id="903c2-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="903c2-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="903c2-120">-Namespace</span></span>
<span data-ttu-id="903c2-121">Névtér neve – elsődleges névtér</span><span class="sxs-lookup"><span data-stu-id="903c2-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="903c2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="903c2-122">-PassThru</span></span>
<span data-ttu-id="903c2-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="903c2-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="903c2-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="903c2-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="903c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="903c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="903c2-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="903c2-126">Resource Group Name</span></span>

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

### <span data-ttu-id="903c2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="903c2-127">-ResourceId</span></span>
<span data-ttu-id="903c2-128">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="903c2-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="903c2-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="903c2-129">-Confirm</span></span>
<span data-ttu-id="903c2-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="903c2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="903c2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="903c2-131">-WhatIf</span></span>
<span data-ttu-id="903c2-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="903c2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="903c2-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="903c2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="903c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903c2-134">CommonParameters</span></span>
<span data-ttu-id="903c2-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="903c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903c2-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="903c2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903c2-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="903c2-137">INPUTS</span></span>

### <span data-ttu-id="903c2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="903c2-138">System.String</span></span>

### <span data-ttu-id="903c2-139">Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="903c2-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="903c2-140">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="903c2-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="903c2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="903c2-141">OUTPUTS</span></span>

### <span data-ttu-id="903c2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="903c2-142">System.Boolean</span></span>

## <span data-ttu-id="903c2-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="903c2-143">NOTES</span></span>

## <span data-ttu-id="903c2-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="903c2-144">RELATED LINKS</span></span>

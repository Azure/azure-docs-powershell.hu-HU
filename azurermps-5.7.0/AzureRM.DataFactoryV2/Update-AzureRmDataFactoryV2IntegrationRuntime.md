---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a66ed7e910b5b9fbd1057d50e2fa3e5058400855
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495406"
---
# <span data-ttu-id="c9f40-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c9f40-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="c9f40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9f40-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f40-103">Az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="c9f40-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9f40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9f40-104">SYNTAX</span></span>

### <span data-ttu-id="c9f40-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9f40-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f40-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c9f40-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f40-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c9f40-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9f40-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9f40-108">DESCRIPTION</span></span>
<span data-ttu-id="c9f40-109">Az **Update-AzureRmDataFactoryV2IntegrationRuntime** parancsmag frissíti az integrációs futtatókörnyezet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="c9f40-109">The **Update-AzureRmDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="c9f40-110">Jelenleg a parancsmag csak az "AutoUpdate" és a "AutoUpdateDelayOffset" frissítést támogatja az önálló integrációs futtatókörnyezethez.</span><span class="sxs-lookup"><span data-stu-id="c9f40-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="c9f40-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c9f40-111">EXAMPLES</span></span>

### <span data-ttu-id="c9f40-112">1. példa: az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="c9f40-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntime `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -Name 'test-selfhost-ir' `
    -AutoUpdate Off `
    -AutoUpdateDelayOffset $ts

Nodes                     : {Node_1}
CreateTime                : 11/18/2017 2:45:38 PM
InternalChannelEncryption : 
Version                   : 3.2.6519.3
Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
ScheduledUpdateDate       : 
UpdateDelayOffset         : 
LocalTimeZoneOffset       : 
AutoUpdate                : Off
ServiceUrls               : {wu.frontend.int.clouddatahub-int.net, *.servicebus.windows.net}
State                     : Online
Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
Type                      : SelfHosted
ResourceGroupName         : rg-test-dfv2
DataFactoryName           : test-df-eu2
Name                      : test-selfhost-ir
Description               : New 2 description
```

<span data-ttu-id="c9f40-113">A parancsmag a "teszt-selfhost-IR" nevű önálló integrációs futtatókörnyezetet frissíti.</span><span class="sxs-lookup"><span data-stu-id="c9f40-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="c9f40-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9f40-114">PARAMETERS</span></span>

### <span data-ttu-id="c9f40-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="c9f40-115">-AutoUpdate</span></span>
<span data-ttu-id="c9f40-116">Engedélyezze vagy tiltsa le az önkiszolgáló integrációs futtatókörnyezet automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="c9f40-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f40-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="c9f40-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="c9f40-118">Az önkiszolgáló integrációs futtatókörnyezet automatikus frissítésének időpontja a nap órájában.</span><span class="sxs-lookup"><span data-stu-id="c9f40-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f40-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c9f40-119">-DataFactoryName</span></span>
<span data-ttu-id="c9f40-120">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="c9f40-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9f40-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f40-121">-DefaultProfile</span></span>
<span data-ttu-id="c9f40-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9f40-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9f40-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9f40-123">-InputObject</span></span>
<span data-ttu-id="c9f40-124">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="c9f40-124">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9f40-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c9f40-125">-Name</span></span>
<span data-ttu-id="c9f40-126">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="c9f40-126">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9f40-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f40-127">-ResourceGroupName</span></span>
<span data-ttu-id="c9f40-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c9f40-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9f40-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9f40-129">-ResourceId</span></span>
<span data-ttu-id="c9f40-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="c9f40-130">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9f40-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9f40-131">-Confirm</span></span>
<span data-ttu-id="c9f40-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9f40-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f40-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f40-133">-WhatIf</span></span>
<span data-ttu-id="c9f40-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9f40-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9f40-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9f40-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f40-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f40-136">CommonParameters</span></span>
<span data-ttu-id="c9f40-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9f40-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f40-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9f40-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f40-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9f40-139">INPUTS</span></span>

### <span data-ttu-id="c9f40-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c9f40-140">System.String</span></span>
<span data-ttu-id="c9f40-141">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c9f40-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c9f40-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9f40-142">OUTPUTS</span></span>

### <span data-ttu-id="c9f40-143">Microsoft. Azure. Command. DataFactoryV2. models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="c9f40-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="c9f40-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9f40-144">NOTES</span></span>
<span data-ttu-id="c9f40-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="c9f40-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="c9f40-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9f40-146">RELATED LINKS</span></span>

<span data-ttu-id="c9f40-147">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="c9f40-147">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>


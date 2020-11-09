---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298202"
---
# <span data-ttu-id="83370-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="83370-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="83370-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83370-102">SYNOPSIS</span></span>
<span data-ttu-id="83370-103">Adatfolyam-hibakeresési munkamenet leállítása az Azure Data Factory-ban</span><span class="sxs-lookup"><span data-stu-id="83370-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="83370-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83370-104">SYNTAX</span></span>

### <span data-ttu-id="83370-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83370-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83370-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="83370-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83370-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="83370-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83370-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="83370-108">DESCRIPTION</span></span>
<span data-ttu-id="83370-109">Ez a parancs leállítja a Debug munkamenetet, ha nem, akkor a munkamenet automatikusan kikapcsol a Debug munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="83370-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="83370-110">Példák</span><span class="sxs-lookup"><span data-stu-id="83370-110">EXAMPLES</span></span>

### <span data-ttu-id="83370-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="83370-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="83370-112">Az adatáramlás hibakeresési munkamenetének leállítása "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" adatkapcsolatú "WikiADF" adatforgalomban</span><span class="sxs-lookup"><span data-stu-id="83370-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="83370-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83370-113">PARAMETERS</span></span>

### <span data-ttu-id="83370-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="83370-114">-DataFactory</span></span>
<span data-ttu-id="83370-115">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="83370-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83370-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="83370-116">-DataFactoryName</span></span>
<span data-ttu-id="83370-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="83370-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83370-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83370-118">-DefaultProfile</span></span>
<span data-ttu-id="83370-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83370-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83370-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83370-120">-PassThru</span></span>
<span data-ttu-id="83370-121">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="83370-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="83370-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="83370-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="83370-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83370-123">-ResourceGroupName</span></span>
<span data-ttu-id="83370-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="83370-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83370-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83370-125">-ResourceId</span></span>
<span data-ttu-id="83370-126">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="83370-126">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83370-127">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="83370-127">-SessionId</span></span>
<span data-ttu-id="83370-128">Az adatfolyam-debug munkamenet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="83370-128">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83370-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83370-129">-Confirm</span></span>
<span data-ttu-id="83370-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83370-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83370-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83370-131">-WhatIf</span></span>
<span data-ttu-id="83370-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83370-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83370-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83370-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83370-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83370-134">CommonParameters</span></span>
<span data-ttu-id="83370-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83370-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83370-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="83370-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83370-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83370-137">INPUTS</span></span>

### <span data-ttu-id="83370-138">System. String</span><span class="sxs-lookup"><span data-stu-id="83370-138">System.String</span></span>

### <span data-ttu-id="83370-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="83370-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="83370-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83370-140">OUTPUTS</span></span>

### <span data-ttu-id="83370-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="83370-141">System.Void</span></span>

### <span data-ttu-id="83370-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83370-142">System.Boolean</span></span>

## <span data-ttu-id="83370-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83370-143">NOTES</span></span>
<span data-ttu-id="83370-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="83370-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="83370-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83370-145">RELATED LINKS</span></span>

[<span data-ttu-id="83370-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="83370-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="83370-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="83370-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="83370-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="83370-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="83370-149">Meghívó-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="83370-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)
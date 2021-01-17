---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477057"
---
# <span data-ttu-id="283d9-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="283d9-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="283d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="283d9-102">SYNOPSIS</span></span>
<span data-ttu-id="283d9-103">Adatfolyam-hibakeresési munkamenet leállítja az Azure Data Factoryban</span><span class="sxs-lookup"><span data-stu-id="283d9-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="283d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="283d9-104">SYNTAX</span></span>

### <span data-ttu-id="283d9-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="283d9-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="283d9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="283d9-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="283d9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="283d9-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="283d9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="283d9-108">DESCRIPTION</span></span>
<span data-ttu-id="283d9-109">Ez a parancs leállítja a hibakeresési munkamenetet, ha nem, akkor a rendszer automatikusan kikapcsolja a munkamenetet a hibakeresési munkamenet Time To Live beállításának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="283d9-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="283d9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="283d9-110">EXAMPLES</span></span>

### <span data-ttu-id="283d9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="283d9-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="283d9-112">Leállítja az "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" adatfolyam-hibakeresési munkamenetet a "WikiADF" adat factoryban</span><span class="sxs-lookup"><span data-stu-id="283d9-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="283d9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="283d9-113">PARAMETERS</span></span>

### <span data-ttu-id="283d9-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="283d9-114">-DataFactory</span></span>
<span data-ttu-id="283d9-115">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="283d9-115">The data factory object.</span></span>

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

### <span data-ttu-id="283d9-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="283d9-116">-DataFactoryName</span></span>
<span data-ttu-id="283d9-117">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="283d9-117">The data factory name.</span></span>

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

### <span data-ttu-id="283d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="283d9-118">-DefaultProfile</span></span>
<span data-ttu-id="283d9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="283d9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="283d9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="283d9-120">-PassThru</span></span>
<span data-ttu-id="283d9-121">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="283d9-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="283d9-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="283d9-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="283d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="283d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="283d9-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="283d9-124">The resource group name.</span></span>

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

### <span data-ttu-id="283d9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="283d9-125">-ResourceId</span></span>
<span data-ttu-id="283d9-126">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="283d9-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="283d9-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="283d9-127">-SessionId</span></span>
<span data-ttu-id="283d9-128">Az adatfolyam hibakeresési munkamenet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="283d9-128">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="283d9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="283d9-129">-Confirm</span></span>
<span data-ttu-id="283d9-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="283d9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="283d9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="283d9-131">-WhatIf</span></span>
<span data-ttu-id="283d9-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="283d9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="283d9-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="283d9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="283d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="283d9-134">CommonParameters</span></span>
<span data-ttu-id="283d9-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="283d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="283d9-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="283d9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="283d9-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="283d9-137">INPUTS</span></span>

### <span data-ttu-id="283d9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="283d9-138">System.String</span></span>

### <span data-ttu-id="283d9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="283d9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="283d9-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="283d9-140">OUTPUTS</span></span>

### <span data-ttu-id="283d9-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="283d9-141">System.Void</span></span>

### <span data-ttu-id="283d9-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="283d9-142">System.Boolean</span></span>

## <span data-ttu-id="283d9-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="283d9-143">NOTES</span></span>
<span data-ttu-id="283d9-144">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="283d9-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="283d9-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="283d9-145">RELATED LINKS</span></span>

[<span data-ttu-id="283d9-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="283d9-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="283d9-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="283d9-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="283d9-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="283d9-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="283d9-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="283d9-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)
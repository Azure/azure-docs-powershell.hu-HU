---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209823"
---
# <span data-ttu-id="370e4-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="370e4-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="370e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="370e4-102">SYNOPSIS</span></span>
<span data-ttu-id="370e4-103">Adatfolyam-hibakeresési munkamenet leállítja az Azure Data Factoryban</span><span class="sxs-lookup"><span data-stu-id="370e4-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="370e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="370e4-104">SYNTAX</span></span>

### <span data-ttu-id="370e4-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="370e4-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="370e4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="370e4-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="370e4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="370e4-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="370e4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="370e4-108">DESCRIPTION</span></span>
<span data-ttu-id="370e4-109">Ez a parancs leállítja a hibakeresési munkamenetet, ha nem, akkor a rendszer automatikusan kikapcsolja a munkamenetet a hibakeresési munkamenet Time To Live beállításának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="370e4-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="370e4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="370e4-110">EXAMPLES</span></span>

### <span data-ttu-id="370e4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="370e4-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="370e4-112">Leállítja az "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" adatfolyam-hibakeresési munkamenetet a "WikiADF" adat factoryban</span><span class="sxs-lookup"><span data-stu-id="370e4-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="370e4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="370e4-113">PARAMETERS</span></span>

### <span data-ttu-id="370e4-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="370e4-114">-DataFactory</span></span>
<span data-ttu-id="370e4-115">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="370e4-115">The data factory object.</span></span>

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

### <span data-ttu-id="370e4-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="370e4-116">-DataFactoryName</span></span>
<span data-ttu-id="370e4-117">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="370e4-117">The data factory name.</span></span>

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

### <span data-ttu-id="370e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="370e4-118">-DefaultProfile</span></span>
<span data-ttu-id="370e4-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="370e4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="370e4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="370e4-120">-PassThru</span></span>
<span data-ttu-id="370e4-121">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="370e4-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="370e4-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="370e4-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="370e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="370e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="370e4-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="370e4-124">The resource group name.</span></span>

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

### <span data-ttu-id="370e4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="370e4-125">-ResourceId</span></span>
<span data-ttu-id="370e4-126">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="370e4-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="370e4-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="370e4-127">-SessionId</span></span>
<span data-ttu-id="370e4-128">Az adatfolyam hibakeresési munkamenet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="370e4-128">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="370e4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="370e4-129">-Confirm</span></span>
<span data-ttu-id="370e4-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="370e4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="370e4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="370e4-131">-WhatIf</span></span>
<span data-ttu-id="370e4-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="370e4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="370e4-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="370e4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="370e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="370e4-134">CommonParameters</span></span>
<span data-ttu-id="370e4-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="370e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="370e4-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="370e4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="370e4-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="370e4-137">INPUTS</span></span>

### <span data-ttu-id="370e4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="370e4-138">System.String</span></span>

### <span data-ttu-id="370e4-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="370e4-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="370e4-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="370e4-140">OUTPUTS</span></span>

### <span data-ttu-id="370e4-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="370e4-141">System.Void</span></span>

### <span data-ttu-id="370e4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="370e4-142">System.Boolean</span></span>

## <span data-ttu-id="370e4-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="370e4-143">NOTES</span></span>
<span data-ttu-id="370e4-144">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="370e4-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="370e4-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="370e4-145">RELATED LINKS</span></span>

[<span data-ttu-id="370e4-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="370e4-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="370e4-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="370e4-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="370e4-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="370e4-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="370e4-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="370e4-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)
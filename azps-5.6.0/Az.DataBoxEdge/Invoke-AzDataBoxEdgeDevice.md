---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 27dc757d3a59a5ab65e30335408f38ffc19aed5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001653"
---
# <span data-ttu-id="43895-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="43895-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="43895-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43895-102">SYNOPSIS</span></span>
<span data-ttu-id="43895-103">Adott műveleteket hív meg az eszközön.</span><span class="sxs-lookup"><span data-stu-id="43895-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="43895-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43895-104">SYNTAX</span></span>

### <span data-ttu-id="43895-105">InvokeScanForUpdateParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43895-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43895-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43895-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43895-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43895-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43895-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43895-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43895-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="43895-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43895-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="43895-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43895-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43895-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43895-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43895-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43895-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43895-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43895-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43895-114">DESCRIPTION</span></span>
<span data-ttu-id="43895-115">Az **Invoke-AzDataBoxEdgeDevice** parancsmag műveleteket hív meg a frissítések kereséséhez, letöltéséhez és telepítéséhez az Data Box Edge eszközén.</span><span class="sxs-lookup"><span data-stu-id="43895-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="43895-116">Az automatikus vizsgálat naponta fut az eszközön, ezt a parancsmagot futtatva explicit módon elindíthatja a beolvasást.</span><span class="sxs-lookup"><span data-stu-id="43895-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="43895-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43895-117">EXAMPLES</span></span>

### <span data-ttu-id="43895-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="43895-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="43895-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="43895-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="43895-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="43895-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="43895-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43895-121">PARAMETERS</span></span>

### <span data-ttu-id="43895-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43895-122">-AsJob</span></span>
<span data-ttu-id="43895-123">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43895-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43895-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43895-124">-DefaultProfile</span></span>
<span data-ttu-id="43895-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43895-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43895-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="43895-126">-DeviceObject</span></span>
<span data-ttu-id="43895-127">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="43895-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43895-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="43895-128">-FetchUpdate</span></span>
<span data-ttu-id="43895-129">A frissítések letöltése egy adatmező szélén/átjáróeszközén</span><span class="sxs-lookup"><span data-stu-id="43895-129">Downloads the updates on a data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeFetchUpdateParameterSet, InvokeFetchUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43895-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="43895-130">-InstallUpdate</span></span>
<span data-ttu-id="43895-131">A frissítések telepítése az adatmező szélére/átjáróeszközére</span><span class="sxs-lookup"><span data-stu-id="43895-131">Installs the updates on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeInstallUpdatesByResourceIdParameterSet, InvokeInstallUpdateParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43895-132">-Name</span><span class="sxs-lookup"><span data-stu-id="43895-132">-Name</span></span>
<span data-ttu-id="43895-133">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="43895-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43895-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43895-134">-PassThru</span></span>
<span data-ttu-id="43895-135">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="43895-135">returns true if successful</span></span>

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

### <span data-ttu-id="43895-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43895-136">-ResourceGroupName</span></span>
<span data-ttu-id="43895-137">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="43895-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43895-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43895-138">-ResourceId</span></span>
<span data-ttu-id="43895-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="43895-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43895-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="43895-140">-ScanForUpdate</span></span>
<span data-ttu-id="43895-141">Frissítéseket keres egy adatmező szélén/átjáróeszközén.</span><span class="sxs-lookup"><span data-stu-id="43895-141">Scans for updates on a data box edge/gateway device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeScanForUpdateByResourceIdParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43895-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43895-142">-Confirm</span></span>
<span data-ttu-id="43895-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="43895-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43895-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43895-144">-WhatIf</span></span>
<span data-ttu-id="43895-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="43895-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43895-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43895-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43895-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43895-147">CommonParameters</span></span>
<span data-ttu-id="43895-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43895-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43895-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43895-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43895-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43895-150">INPUTS</span></span>

### <span data-ttu-id="43895-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="43895-151">None</span></span>

## <span data-ttu-id="43895-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43895-152">OUTPUTS</span></span>

### <span data-ttu-id="43895-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43895-153">System.Boolean</span></span>

## <span data-ttu-id="43895-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43895-154">NOTES</span></span>

## <span data-ttu-id="43895-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43895-155">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355973"
---
# <span data-ttu-id="e1b27-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e1b27-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="e1b27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1b27-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b27-103">Adott műveleteket hív meg az eszközön.</span><span class="sxs-lookup"><span data-stu-id="e1b27-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="e1b27-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e1b27-104">SYNTAX</span></span>

### <span data-ttu-id="e1b27-105">InvokeScanForUpdateParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1b27-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1b27-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1b27-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1b27-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1b27-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1b27-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1b27-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1b27-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1b27-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1b27-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1b27-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1b27-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1b27-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1b27-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1b27-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1b27-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1b27-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1b27-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e1b27-114">DESCRIPTION</span></span>
<span data-ttu-id="e1b27-115">Az **Invoke-AzDataBoxEdgeDevice** parancsmag műveleteket hív meg a frissítések kereséséhez, letöltéséhez és telepítéséhez az Data Box Edge eszközén.</span><span class="sxs-lookup"><span data-stu-id="e1b27-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="e1b27-116">Az automatikus vizsgálat naponta fut az eszközön, ezt a parancsmagot futtatva explicit módon elindíthatja a beolvasást.</span><span class="sxs-lookup"><span data-stu-id="e1b27-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="e1b27-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e1b27-117">EXAMPLES</span></span>

### <span data-ttu-id="e1b27-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="e1b27-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="e1b27-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="e1b27-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="e1b27-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="e1b27-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="e1b27-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1b27-121">PARAMETERS</span></span>

### <span data-ttu-id="e1b27-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1b27-122">-AsJob</span></span>
<span data-ttu-id="e1b27-123">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e1b27-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1b27-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b27-124">-DefaultProfile</span></span>
<span data-ttu-id="e1b27-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1b27-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1b27-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e1b27-126">-DeviceObject</span></span>
<span data-ttu-id="e1b27-127">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="e1b27-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="e1b27-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b27-128">-FetchUpdate</span></span>
<span data-ttu-id="e1b27-129">A frissítések letöltése egy adatmező szélén/átjáróeszközén</span><span class="sxs-lookup"><span data-stu-id="e1b27-129">Downloads the updates on a data box edge/gateway device</span></span>

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

### <span data-ttu-id="e1b27-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b27-130">-InstallUpdate</span></span>
<span data-ttu-id="e1b27-131">A frissítések telepítése az adatmező szélére/átjáróeszközére</span><span class="sxs-lookup"><span data-stu-id="e1b27-131">Installs the updates on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="e1b27-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e1b27-132">-Name</span></span>
<span data-ttu-id="e1b27-133">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="e1b27-133">Device Name</span></span>

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

### <span data-ttu-id="e1b27-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1b27-134">-PassThru</span></span>
<span data-ttu-id="e1b27-135">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="e1b27-135">returns true if successful</span></span>

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

### <span data-ttu-id="e1b27-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1b27-136">-ResourceGroupName</span></span>
<span data-ttu-id="e1b27-137">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e1b27-137">Resource Group Name</span></span>

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

### <span data-ttu-id="e1b27-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1b27-138">-ResourceId</span></span>
<span data-ttu-id="e1b27-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1b27-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="e1b27-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b27-140">-ScanForUpdate</span></span>
<span data-ttu-id="e1b27-141">Frissítéseket keres egy adatmező szélén/átjáróeszközén.</span><span class="sxs-lookup"><span data-stu-id="e1b27-141">Scans for updates on a data box edge/gateway device.</span></span>

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

### <span data-ttu-id="e1b27-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1b27-142">-Confirm</span></span>
<span data-ttu-id="e1b27-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e1b27-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1b27-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1b27-144">-WhatIf</span></span>
<span data-ttu-id="e1b27-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e1b27-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1b27-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1b27-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1b27-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b27-147">CommonParameters</span></span>
<span data-ttu-id="e1b27-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1b27-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b27-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1b27-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b27-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1b27-150">INPUTS</span></span>

### <span data-ttu-id="e1b27-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="e1b27-151">None</span></span>

## <span data-ttu-id="e1b27-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1b27-152">OUTPUTS</span></span>

### <span data-ttu-id="e1b27-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e1b27-153">System.Boolean</span></span>

## <span data-ttu-id="e1b27-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e1b27-154">NOTES</span></span>

## <span data-ttu-id="e1b27-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1b27-155">RELATED LINKS</span></span>

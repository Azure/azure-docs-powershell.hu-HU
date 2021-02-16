---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209127"
---
# <span data-ttu-id="d2823-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d2823-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="d2823-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2823-102">SYNOPSIS</span></span>
<span data-ttu-id="d2823-103">Adott műveleteket hív meg az eszközön.</span><span class="sxs-lookup"><span data-stu-id="d2823-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="d2823-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d2823-104">SYNTAX</span></span>

### <span data-ttu-id="d2823-105">InvokeScanForUpdateParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2823-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2823-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2823-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2823-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2823-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2823-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2823-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2823-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2823-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2823-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2823-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2823-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2823-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2823-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2823-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2823-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2823-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2823-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d2823-114">DESCRIPTION</span></span>
<span data-ttu-id="d2823-115">Az **Invoke-AzStackEdgeDevice** parancsmag műveleteket hív meg a frissítések stack edge eszközön való beolvasása, letöltése és telepítése során.</span><span class="sxs-lookup"><span data-stu-id="d2823-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="d2823-116">Az automatikus vizsgálat naponta fut az eszközön, ezt a parancsmagot futtatva explicit módon elindíthatja a beolvasást.</span><span class="sxs-lookup"><span data-stu-id="d2823-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="d2823-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d2823-117">EXAMPLES</span></span>

### <span data-ttu-id="d2823-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="d2823-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="d2823-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="d2823-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="d2823-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="d2823-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="d2823-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2823-121">PARAMETERS</span></span>

### <span data-ttu-id="d2823-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2823-122">-AsJob</span></span>
<span data-ttu-id="d2823-123">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d2823-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2823-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2823-124">-DefaultProfile</span></span>
<span data-ttu-id="d2823-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2823-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2823-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d2823-126">-DeviceObject</span></span>
<span data-ttu-id="d2823-127">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="d2823-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2823-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="d2823-128">-FetchUpdate</span></span>
<span data-ttu-id="d2823-129">Frissítések letöltése Stack edge/gateway eszközre</span><span class="sxs-lookup"><span data-stu-id="d2823-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="d2823-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="d2823-130">-InstallUpdate</span></span>
<span data-ttu-id="d2823-131">A frissítések telepítése a Stack edge/gateway eszközre</span><span class="sxs-lookup"><span data-stu-id="d2823-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="d2823-132">-Name</span><span class="sxs-lookup"><span data-stu-id="d2823-132">-Name</span></span>
<span data-ttu-id="d2823-133">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="d2823-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2823-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2823-134">-PassThru</span></span>
<span data-ttu-id="d2823-135">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="d2823-135">returns true if successful</span></span>

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

### <span data-ttu-id="d2823-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2823-136">-ResourceGroupName</span></span>
<span data-ttu-id="d2823-137">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d2823-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2823-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2823-138">-ResourceId</span></span>
<span data-ttu-id="d2823-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2823-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2823-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="d2823-140">-ScanForUpdate</span></span>
<span data-ttu-id="d2823-141">Frissítéseket keres stack edge/gateway eszközön.</span><span class="sxs-lookup"><span data-stu-id="d2823-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="d2823-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2823-142">-Confirm</span></span>
<span data-ttu-id="d2823-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d2823-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2823-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2823-144">-WhatIf</span></span>
<span data-ttu-id="d2823-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d2823-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2823-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2823-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2823-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2823-147">CommonParameters</span></span>
<span data-ttu-id="d2823-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2823-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2823-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2823-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2823-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2823-150">INPUTS</span></span>

### <span data-ttu-id="d2823-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="d2823-151">None</span></span>

## <span data-ttu-id="d2823-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2823-152">OUTPUTS</span></span>

### <span data-ttu-id="d2823-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2823-153">System.Boolean</span></span>

## <span data-ttu-id="d2823-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d2823-154">NOTES</span></span>

## <span data-ttu-id="d2823-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2823-155">RELATED LINKS</span></span>

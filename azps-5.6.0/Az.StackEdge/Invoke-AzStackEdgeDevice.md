---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: 63d364ac12d47f5bb15e877e5076550a0cbd3f16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005270"
---
# <span data-ttu-id="8ef4d-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8ef4d-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="8ef4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ef4d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef4d-103">Adott műveleteket hív meg az eszközön.</span><span class="sxs-lookup"><span data-stu-id="8ef4d-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="8ef4d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ef4d-104">SYNTAX</span></span>

### <span data-ttu-id="8ef4d-105">InvokeScanForUpdateParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ef4d-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef4d-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef4d-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef4d-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef4d-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef4d-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef4d-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef4d-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef4d-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef4d-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef4d-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef4d-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef4d-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef4d-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef4d-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef4d-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef4d-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ef4d-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ef4d-114">DESCRIPTION</span></span>
<span data-ttu-id="8ef4d-115">Az **Invoke-AzStackEdgeDevice** parancsmag műveleteket hív meg a frissítések stack edge-es eszközre való átolvasása, letöltése és telepítése során.</span><span class="sxs-lookup"><span data-stu-id="8ef4d-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="8ef4d-116">Az automatikus vizsgálat naponta fut az eszközön, ezt a parancsmagot futtatva explicit módon elindíthatja a beolvasást.</span><span class="sxs-lookup"><span data-stu-id="8ef4d-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="8ef4d-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ef4d-117">EXAMPLES</span></span>

### <span data-ttu-id="8ef4d-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="8ef4d-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="8ef4d-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="8ef4d-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="8ef4d-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="8ef4d-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="8ef4d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ef4d-121">PARAMETERS</span></span>

### <span data-ttu-id="8ef4d-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ef4d-122">-AsJob</span></span>
<span data-ttu-id="8ef4d-123">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8ef4d-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ef4d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef4d-124">-DefaultProfile</span></span>
<span data-ttu-id="8ef4d-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ef4d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ef4d-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8ef4d-126">-DeviceObject</span></span>
<span data-ttu-id="8ef4d-127">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="8ef4d-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="8ef4d-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="8ef4d-128">-FetchUpdate</span></span>
<span data-ttu-id="8ef4d-129">Frissítések letöltése Stack edge/gateway eszközre</span><span class="sxs-lookup"><span data-stu-id="8ef4d-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="8ef4d-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="8ef4d-130">-InstallUpdate</span></span>
<span data-ttu-id="8ef4d-131">A frissítések telepítése a Stack edge/gateway eszközre</span><span class="sxs-lookup"><span data-stu-id="8ef4d-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="8ef4d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="8ef4d-132">-Name</span></span>
<span data-ttu-id="8ef4d-133">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="8ef4d-133">Device Name</span></span>

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

### <span data-ttu-id="8ef4d-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ef4d-134">-PassThru</span></span>
<span data-ttu-id="8ef4d-135">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="8ef4d-135">returns true if successful</span></span>

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

### <span data-ttu-id="8ef4d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ef4d-136">-ResourceGroupName</span></span>
<span data-ttu-id="8ef4d-137">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8ef4d-137">Resource Group Name</span></span>

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

### <span data-ttu-id="8ef4d-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ef4d-138">-ResourceId</span></span>
<span data-ttu-id="8ef4d-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ef4d-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="8ef4d-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="8ef4d-140">-ScanForUpdate</span></span>
<span data-ttu-id="8ef4d-141">Frissítéseket keres stack edge/gateway eszközön.</span><span class="sxs-lookup"><span data-stu-id="8ef4d-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="8ef4d-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ef4d-142">-Confirm</span></span>
<span data-ttu-id="8ef4d-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8ef4d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ef4d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ef4d-144">-WhatIf</span></span>
<span data-ttu-id="8ef4d-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8ef4d-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ef4d-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ef4d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ef4d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef4d-147">CommonParameters</span></span>
<span data-ttu-id="8ef4d-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ef4d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef4d-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ef4d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef4d-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ef4d-150">INPUTS</span></span>

### <span data-ttu-id="8ef4d-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="8ef4d-151">None</span></span>

## <span data-ttu-id="8ef4d-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ef4d-152">OUTPUTS</span></span>

### <span data-ttu-id="8ef4d-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ef4d-153">System.Boolean</span></span>

## <span data-ttu-id="8ef4d-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ef4d-154">NOTES</span></span>

## <span data-ttu-id="8ef4d-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ef4d-155">RELATED LINKS</span></span>

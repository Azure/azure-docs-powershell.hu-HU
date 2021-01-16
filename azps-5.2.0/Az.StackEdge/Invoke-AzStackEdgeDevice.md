---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344406"
---
# <span data-ttu-id="c24bb-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c24bb-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="c24bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c24bb-102">SYNOPSIS</span></span>
<span data-ttu-id="c24bb-103">Adott műveleteket hív meg az eszközön.</span><span class="sxs-lookup"><span data-stu-id="c24bb-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="c24bb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c24bb-104">SYNTAX</span></span>

### <span data-ttu-id="c24bb-105">InvokeScanForUpdateParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c24bb-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24bb-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c24bb-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24bb-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c24bb-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24bb-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c24bb-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24bb-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c24bb-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24bb-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c24bb-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24bb-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c24bb-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24bb-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c24bb-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24bb-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c24bb-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c24bb-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c24bb-114">DESCRIPTION</span></span>
<span data-ttu-id="c24bb-115">Az **Invoke-AzStackEdgeDevice** parancsmag műveleteket hív meg a frissítések stack edge-es eszközre való átolvasása, letöltése és telepítése során.</span><span class="sxs-lookup"><span data-stu-id="c24bb-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="c24bb-116">Az automatikus vizsgálat naponta fut az eszközön, ezt a parancsmagot futtatva explicit módon elindíthatja a beolvasást.</span><span class="sxs-lookup"><span data-stu-id="c24bb-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="c24bb-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c24bb-117">EXAMPLES</span></span>

### <span data-ttu-id="c24bb-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="c24bb-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="c24bb-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="c24bb-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="c24bb-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="c24bb-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="c24bb-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c24bb-121">PARAMETERS</span></span>

### <span data-ttu-id="c24bb-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c24bb-122">-AsJob</span></span>
<span data-ttu-id="c24bb-123">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c24bb-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c24bb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24bb-124">-DefaultProfile</span></span>
<span data-ttu-id="c24bb-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c24bb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c24bb-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c24bb-126">-DeviceObject</span></span>
<span data-ttu-id="c24bb-127">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="c24bb-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c24bb-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="c24bb-128">-FetchUpdate</span></span>
<span data-ttu-id="c24bb-129">Frissítések letöltése Stack edge/gateway eszközre</span><span class="sxs-lookup"><span data-stu-id="c24bb-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="c24bb-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="c24bb-130">-InstallUpdate</span></span>
<span data-ttu-id="c24bb-131">A frissítések telepítése a Stack edge/gateway eszközre</span><span class="sxs-lookup"><span data-stu-id="c24bb-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="c24bb-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c24bb-132">-Name</span></span>
<span data-ttu-id="c24bb-133">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="c24bb-133">Device Name</span></span>

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

### <span data-ttu-id="c24bb-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c24bb-134">-PassThru</span></span>
<span data-ttu-id="c24bb-135">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="c24bb-135">returns true if successful</span></span>

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

### <span data-ttu-id="c24bb-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c24bb-136">-ResourceGroupName</span></span>
<span data-ttu-id="c24bb-137">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c24bb-137">Resource Group Name</span></span>

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

### <span data-ttu-id="c24bb-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c24bb-138">-ResourceId</span></span>
<span data-ttu-id="c24bb-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c24bb-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="c24bb-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="c24bb-140">-ScanForUpdate</span></span>
<span data-ttu-id="c24bb-141">Frissítéseket keres stack edge/gateway eszközön.</span><span class="sxs-lookup"><span data-stu-id="c24bb-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="c24bb-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c24bb-142">-Confirm</span></span>
<span data-ttu-id="c24bb-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c24bb-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c24bb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c24bb-144">-WhatIf</span></span>
<span data-ttu-id="c24bb-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c24bb-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c24bb-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c24bb-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c24bb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24bb-147">CommonParameters</span></span>
<span data-ttu-id="c24bb-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c24bb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24bb-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c24bb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24bb-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c24bb-150">INPUTS</span></span>

### <span data-ttu-id="c24bb-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="c24bb-151">None</span></span>

## <span data-ttu-id="c24bb-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c24bb-152">OUTPUTS</span></span>

### <span data-ttu-id="c24bb-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c24bb-153">System.Boolean</span></span>

## <span data-ttu-id="c24bb-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c24bb-154">NOTES</span></span>

## <span data-ttu-id="c24bb-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c24bb-155">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182089"
---
# <span data-ttu-id="80a39-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="80a39-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="80a39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80a39-102">SYNOPSIS</span></span>
<span data-ttu-id="80a39-103">Meghívja az eszköz adott műveleteit.</span><span class="sxs-lookup"><span data-stu-id="80a39-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="80a39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80a39-104">SYNTAX</span></span>

### <span data-ttu-id="80a39-105">InvokeScanForUpdateParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80a39-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a39-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a39-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a39-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a39-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a39-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a39-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a39-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a39-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a39-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a39-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a39-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a39-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a39-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a39-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a39-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a39-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80a39-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="80a39-114">DESCRIPTION</span></span>
<span data-ttu-id="80a39-115">Az AzStackEdgeDevice parancsmag az átvizsgálandó műveleteket **kezdeményezi** , letöltheti és telepítheti a frissítéseket a halom szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="80a39-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="80a39-116">Az automatikus vizsgálat naponta fut, a következő parancsmag futtatásával explicit módon aktiválhatja a vizsgálatot.</span><span class="sxs-lookup"><span data-stu-id="80a39-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="80a39-117">Példák</span><span class="sxs-lookup"><span data-stu-id="80a39-117">EXAMPLES</span></span>

### <span data-ttu-id="80a39-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="80a39-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="80a39-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="80a39-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="80a39-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="80a39-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="80a39-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80a39-121">PARAMETERS</span></span>

### <span data-ttu-id="80a39-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80a39-122">-AsJob</span></span>
<span data-ttu-id="80a39-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="80a39-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80a39-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a39-124">-DefaultProfile</span></span>
<span data-ttu-id="80a39-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80a39-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80a39-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="80a39-126">-DeviceObject</span></span>
<span data-ttu-id="80a39-127">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="80a39-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="80a39-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="80a39-128">-FetchUpdate</span></span>
<span data-ttu-id="80a39-129">A frissítések letöltése a halom szélén/átjáró eszközön</span><span class="sxs-lookup"><span data-stu-id="80a39-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="80a39-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="80a39-130">-InstallUpdate</span></span>
<span data-ttu-id="80a39-131">A frissítések telepítése a halom Edge/Gateway eszközön</span><span class="sxs-lookup"><span data-stu-id="80a39-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="80a39-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="80a39-132">-Name</span></span>
<span data-ttu-id="80a39-133">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="80a39-133">Device Name</span></span>

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

### <span data-ttu-id="80a39-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80a39-134">-PassThru</span></span>
<span data-ttu-id="80a39-135">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="80a39-135">returns true if successful</span></span>

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

### <span data-ttu-id="80a39-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80a39-136">-ResourceGroupName</span></span>
<span data-ttu-id="80a39-137">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="80a39-137">Resource Group Name</span></span>

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

### <span data-ttu-id="80a39-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80a39-138">-ResourceId</span></span>
<span data-ttu-id="80a39-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="80a39-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="80a39-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="80a39-140">-ScanForUpdate</span></span>
<span data-ttu-id="80a39-141">Frissítéseket keres a halom szélén/átjáró eszközön.</span><span class="sxs-lookup"><span data-stu-id="80a39-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="80a39-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="80a39-142">-Confirm</span></span>
<span data-ttu-id="80a39-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="80a39-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80a39-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a39-144">-WhatIf</span></span>
<span data-ttu-id="80a39-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="80a39-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80a39-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="80a39-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80a39-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a39-147">CommonParameters</span></span>
<span data-ttu-id="80a39-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80a39-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a39-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="80a39-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a39-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80a39-150">INPUTS</span></span>

### <span data-ttu-id="80a39-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="80a39-151">None</span></span>

## <span data-ttu-id="80a39-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80a39-152">OUTPUTS</span></span>

### <span data-ttu-id="80a39-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80a39-153">System.Boolean</span></span>

## <span data-ttu-id="80a39-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80a39-154">NOTES</span></span>

## <span data-ttu-id="80a39-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80a39-155">RELATED LINKS</span></span>

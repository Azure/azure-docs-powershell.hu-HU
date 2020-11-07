---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 07cfcacb30dd855447ab7f568cb2c1f2a61c1d75
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844114"
---
# <span data-ttu-id="c895c-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c895c-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="c895c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c895c-102">SYNOPSIS</span></span>
<span data-ttu-id="c895c-103">Meghívja az eszköz adott műveleteit.</span><span class="sxs-lookup"><span data-stu-id="c895c-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="c895c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c895c-104">SYNTAX</span></span>

### <span data-ttu-id="c895c-105">InvokeScanForUpdateParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c895c-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c895c-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c895c-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c895c-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c895c-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c895c-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c895c-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c895c-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c895c-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c895c-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c895c-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c895c-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c895c-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c895c-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c895c-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c895c-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c895c-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c895c-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="c895c-114">DESCRIPTION</span></span>
<span data-ttu-id="c895c-115">A **meghívó AzDataBoxEdgeDevice** parancsmag az adatmező szélén lévő eszközön elindítja a frissítéseket, letölti és telepíti a frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="c895c-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="c895c-116">Az automatikus vizsgálat naponta fut, a következő parancsmag futtatásával explicit módon aktiválhatja a vizsgálatot.</span><span class="sxs-lookup"><span data-stu-id="c895c-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="c895c-117">Példák</span><span class="sxs-lookup"><span data-stu-id="c895c-117">EXAMPLES</span></span>

### <span data-ttu-id="c895c-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c895c-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="c895c-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="c895c-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="c895c-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="c895c-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="c895c-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c895c-121">PARAMETERS</span></span>

### <span data-ttu-id="c895c-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c895c-122">-AsJob</span></span>
<span data-ttu-id="c895c-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c895c-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c895c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c895c-124">-DefaultProfile</span></span>
<span data-ttu-id="c895c-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c895c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c895c-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c895c-126">-DeviceObject</span></span>
<span data-ttu-id="c895c-127">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="c895c-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c895c-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="c895c-128">-FetchUpdate</span></span>
<span data-ttu-id="c895c-129">Az adatmező szélén vagy átjáró eszközön lévő frissítések letöltése</span><span class="sxs-lookup"><span data-stu-id="c895c-129">Downloads the updates on a data box edge/gateway device</span></span>

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

### <span data-ttu-id="c895c-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="c895c-130">-InstallUpdate</span></span>
<span data-ttu-id="c895c-131">A frissítések telepítése az adatmező szélén/átjáró eszközön</span><span class="sxs-lookup"><span data-stu-id="c895c-131">Installs the updates on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="c895c-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c895c-132">-Name</span></span>
<span data-ttu-id="c895c-133">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="c895c-133">Device Name</span></span>

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

### <span data-ttu-id="c895c-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c895c-134">-PassThru</span></span>
<span data-ttu-id="c895c-135">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="c895c-135">returns true if successful</span></span>

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

### <span data-ttu-id="c895c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c895c-136">-ResourceGroupName</span></span>
<span data-ttu-id="c895c-137">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c895c-137">Resource Group Name</span></span>

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

### <span data-ttu-id="c895c-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c895c-138">-ResourceId</span></span>
<span data-ttu-id="c895c-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c895c-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="c895c-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="c895c-140">-ScanForUpdate</span></span>
<span data-ttu-id="c895c-141">Frissítéseket keres az adatmező szélén/átjáró eszközön.</span><span class="sxs-lookup"><span data-stu-id="c895c-141">Scans for updates on a data box edge/gateway device.</span></span>

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

### <span data-ttu-id="c895c-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c895c-142">-Confirm</span></span>
<span data-ttu-id="c895c-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c895c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c895c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c895c-144">-WhatIf</span></span>
<span data-ttu-id="c895c-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c895c-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c895c-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c895c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c895c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c895c-147">CommonParameters</span></span>
<span data-ttu-id="c895c-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c895c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c895c-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c895c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c895c-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c895c-150">INPUTS</span></span>

### <span data-ttu-id="c895c-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="c895c-151">None</span></span>

## <span data-ttu-id="c895c-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c895c-152">OUTPUTS</span></span>

### <span data-ttu-id="c895c-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c895c-153">System.Boolean</span></span>

## <span data-ttu-id="c895c-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c895c-154">NOTES</span></span>

## <span data-ttu-id="c895c-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c895c-155">RELATED LINKS</span></span>

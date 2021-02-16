---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207399"
---
# <span data-ttu-id="e0360-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="e0360-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="e0360-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0360-102">SYNOPSIS</span></span>
<span data-ttu-id="e0360-103">Windows IoT-eszközszolgáltatás törlése</span><span class="sxs-lookup"><span data-stu-id="e0360-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="e0360-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0360-104">SYNTAX</span></span>

### <span data-ttu-id="e0360-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0360-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0360-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e0360-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0360-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0360-107">DESCRIPTION</span></span>
<span data-ttu-id="e0360-108">Windows IoT-eszközszolgáltatás törlése</span><span class="sxs-lookup"><span data-stu-id="e0360-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="e0360-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0360-109">EXAMPLES</span></span>

### <span data-ttu-id="e0360-110">1. példa: Windows IoT-szolgáltatások eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="e0360-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="e0360-111">Ez a parancs név szerint eltávolítja a Windows IoT-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="e0360-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="e0360-112">2. példa: Windows IoT-szolgáltatások eltávolítása folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="e0360-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="e0360-113">Ez a parancs folyamat szerint eltávolítja a Windows IoT-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="e0360-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="e0360-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0360-114">PARAMETERS</span></span>

### <span data-ttu-id="e0360-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0360-115">-DefaultProfile</span></span>
<span data-ttu-id="e0360-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0360-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0360-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0360-117">-InputObject</span></span>
<span data-ttu-id="e0360-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e0360-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0360-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e0360-119">-Name</span></span>
<span data-ttu-id="e0360-120">A Windows IoT-eszközszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="e0360-120">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0360-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0360-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0360-122">A Windows IoT eszközszolgáltatást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0360-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0360-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0360-123">-SubscriptionId</span></span>
<span data-ttu-id="e0360-124">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e0360-124">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0360-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0360-125">-Confirm</span></span>
<span data-ttu-id="e0360-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e0360-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0360-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0360-127">-WhatIf</span></span>
<span data-ttu-id="e0360-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e0360-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0360-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0360-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0360-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0360-130">CommonParameters</span></span>
<span data-ttu-id="e0360-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0360-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0360-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0360-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0360-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0360-133">INPUTS</span></span>

### <span data-ttu-id="e0360-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="e0360-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="e0360-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0360-135">OUTPUTS</span></span>

### <span data-ttu-id="e0360-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="e0360-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="e0360-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0360-137">NOTES</span></span>

<span data-ttu-id="e0360-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e0360-138">ALIASES</span></span>

<span data-ttu-id="e0360-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e0360-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0360-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e0360-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0360-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0360-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0360-142">INPUTOBJECT: <IWindowsIotServicesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e0360-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0360-143">`[DeviceName <String>]`: A Windows IoT-eszközszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="e0360-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="e0360-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e0360-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0360-145">`[ResourceGroupName <String>]`: A Windows IoT eszközszolgáltatást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0360-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="e0360-146">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e0360-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="e0360-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0360-147">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: e0012bab0679a49e0ad5a117845ca9e0e5d5a6db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928410"
---
# <span data-ttu-id="a28d8-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="a28d8-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="a28d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a28d8-102">SYNOPSIS</span></span>
<span data-ttu-id="a28d8-103">Windows IoT-eszközszolgáltatás törlése</span><span class="sxs-lookup"><span data-stu-id="a28d8-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="a28d8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a28d8-104">SYNTAX</span></span>

### <span data-ttu-id="a28d8-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a28d8-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a28d8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a28d8-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a28d8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a28d8-107">DESCRIPTION</span></span>
<span data-ttu-id="a28d8-108">Windows IoT-eszközszolgáltatás törlése</span><span class="sxs-lookup"><span data-stu-id="a28d8-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="a28d8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a28d8-109">EXAMPLES</span></span>

### <span data-ttu-id="a28d8-110">1. példa: Windows IoT-szolgáltatások eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="a28d8-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="a28d8-111">Ez a parancs név szerint eltávolítja a Windows IoT-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="a28d8-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="a28d8-112">2. példa: Windows IoT-szolgáltatások eltávolítása folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="a28d8-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="a28d8-113">Ez a parancs folyamat szerint eltávolítja a Windows IoT-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="a28d8-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="a28d8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a28d8-114">PARAMETERS</span></span>

### <span data-ttu-id="a28d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28d8-115">-DefaultProfile</span></span>
<span data-ttu-id="a28d8-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a28d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a28d8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a28d8-117">-InputObject</span></span>
<span data-ttu-id="a28d8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a28d8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a28d8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a28d8-119">-Name</span></span>
<span data-ttu-id="a28d8-120">A Windows IoT-eszközszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="a28d8-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="a28d8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a28d8-121">-ResourceGroupName</span></span>
<span data-ttu-id="a28d8-122">A Windows IoT eszközszolgáltatást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a28d8-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="a28d8-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a28d8-123">-SubscriptionId</span></span>
<span data-ttu-id="a28d8-124">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a28d8-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="a28d8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a28d8-125">-Confirm</span></span>
<span data-ttu-id="a28d8-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a28d8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a28d8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a28d8-127">-WhatIf</span></span>
<span data-ttu-id="a28d8-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a28d8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a28d8-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a28d8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a28d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28d8-130">CommonParameters</span></span>
<span data-ttu-id="a28d8-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a28d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28d8-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a28d8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28d8-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a28d8-133">INPUTS</span></span>

### <span data-ttu-id="a28d8-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="a28d8-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="a28d8-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a28d8-135">OUTPUTS</span></span>

### <span data-ttu-id="a28d8-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="a28d8-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="a28d8-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a28d8-137">NOTES</span></span>

<span data-ttu-id="a28d8-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a28d8-138">ALIASES</span></span>

<span data-ttu-id="a28d8-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a28d8-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a28d8-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a28d8-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a28d8-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a28d8-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a28d8-142">INPUTOBJECT: <IWindowsIotServicesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a28d8-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a28d8-143">`[DeviceName <String>]`: A Windows IoT-eszközszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="a28d8-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="a28d8-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a28d8-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a28d8-145">`[ResourceGroupName <String>]`: A Windows IoT eszközszolgáltatást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a28d8-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="a28d8-146">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a28d8-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="a28d8-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a28d8-147">RELATED LINKS</span></span>


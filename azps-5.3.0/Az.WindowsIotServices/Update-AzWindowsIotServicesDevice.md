---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 5e50ad3dc1ce2396dfb7a2b498efc82c4e95e430
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466939"
---
# <span data-ttu-id="5b2bb-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="5b2bb-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="5b2bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5b2bb-103">Frissíti egy Windows IoT-eszközszolgáltatás metaadatait.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="5b2bb-104">A tulajdonság módosításának szokásos sémája az, hogy beolvassa a Windows IoT eszközszolgáltatás metaadatait és biztonsági metaadatait, majd kombinálja őket a módosított értékekkel egy új törzsben a Windows IoT eszközszolgáltatás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="5b2bb-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b2bb-105">SYNTAX</span></span>

### <span data-ttu-id="5b2bb-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b2bb-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5b2bb-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5b2bb-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5b2bb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b2bb-108">DESCRIPTION</span></span>
<span data-ttu-id="5b2bb-109">Frissíti egy Windows IoT-eszközszolgáltatás metaadatait.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="5b2bb-110">A tulajdonság módosításának szokásos sémája az, hogy beolvassa a Windows IoT eszközszolgáltatás metaadatait és biztonsági metaadatait, majd kombinálja őket a módosított értékekkel egy új törzsben a Windows IoT eszközszolgáltatás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="5b2bb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b2bb-111">EXAMPLES</span></span>

### <span data-ttu-id="5b2bb-112">1. példa: Windows IoT-szolgáltatások frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="5b2bb-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="5b2bb-113">Ez a parancs név szerint frissíti a Windows IoT-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="5b2bb-114">2. példa: Windows IoT-szolgáltatások frissítése folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="5b2bb-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="5b2bb-115">Ez a parancs folyamat szerint frissíti a Windows IoT-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="5b2bb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b2bb-116">PARAMETERS</span></span>

### <span data-ttu-id="5b2bb-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="5b2bb-117">-AdminDomainName</span></span>
<span data-ttu-id="5b2bb-118">Windows IoT eszközszolgáltatás OEM AAD-tartomány</span><span class="sxs-lookup"><span data-stu-id="5b2bb-118">Windows IoT Device Service OEM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="5b2bb-119">-BillingDomainName</span></span>
<span data-ttu-id="5b2bb-120">Windows IoT-eszközszolgáltatás – ODM AAD-tartomány</span><span class="sxs-lookup"><span data-stu-id="5b2bb-120">Windows IoT Device Service ODM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b2bb-121">-DefaultProfile</span></span>
<span data-ttu-id="5b2bb-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b2bb-123">-Etag</span><span class="sxs-lookup"><span data-stu-id="5b2bb-123">-Etag</span></span>
<span data-ttu-id="5b2bb-124">Az Etag mező nem *kötelező.*</span><span class="sxs-lookup"><span data-stu-id="5b2bb-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="5b2bb-125">Ha a válasz törzsében meg van biztosítanak, a normál ETag-konvenciónak megfelelő fejlécként is meg kell azt adni.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="5b2bb-126">-IfMatch</span></span>
<span data-ttu-id="5b2bb-127">A Windows IoT eszközszolgáltatás Etagja.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="5b2bb-128">Ne adjon meg teljesen új Windows IoT-eszközszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="5b2bb-129">Egy meglévő Windows IoT-eszközszolgáltatás frissítéséhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-129">Required to update an existing Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b2bb-130">-InputObject</span></span>
<span data-ttu-id="5b2bb-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-132">-Location</span><span class="sxs-lookup"><span data-stu-id="5b2bb-132">-Location</span></span>
<span data-ttu-id="5b2bb-133">Az azure-régió, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="5b2bb-133">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-134">-Name</span><span class="sxs-lookup"><span data-stu-id="5b2bb-134">-Name</span></span>
<span data-ttu-id="5b2bb-135">A Windows IoT-eszközszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-135">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-136">-Note</span><span class="sxs-lookup"><span data-stu-id="5b2bb-136">-Note</span></span>
<span data-ttu-id="5b2bb-137">A Windows IoT-eszközszolgáltatás megjegyzései.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-137">Windows IoT Device Service notes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-138">-Mennyiség</span><span class="sxs-lookup"><span data-stu-id="5b2bb-138">-Quantity</span></span>
<span data-ttu-id="5b2bb-139">Windows IoT-eszközszolgáltatás eszközfoglalása,</span><span class="sxs-lookup"><span data-stu-id="5b2bb-139">Windows IoT Device Service device allocation,</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b2bb-140">-ResourceGroupName</span></span>
<span data-ttu-id="5b2bb-141">A Windows IoT eszközszolgáltatást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b2bb-142">-SubscriptionId</span></span>
<span data-ttu-id="5b2bb-143">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-143">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b2bb-144">-Tag</span></span>
<span data-ttu-id="5b2bb-145">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-145">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2bb-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b2bb-146">-Confirm</span></span>
<span data-ttu-id="5b2bb-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b2bb-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b2bb-148">-WhatIf</span></span>
<span data-ttu-id="5b2bb-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b2bb-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b2bb-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b2bb-151">CommonParameters</span></span>
<span data-ttu-id="5b2bb-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b2bb-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b2bb-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b2bb-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b2bb-154">INPUTS</span></span>

### <span data-ttu-id="5b2bb-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="5b2bb-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="5b2bb-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b2bb-156">OUTPUTS</span></span>

### <span data-ttu-id="5b2bb-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="5b2bb-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="5b2bb-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b2bb-158">NOTES</span></span>

<span data-ttu-id="5b2bb-159">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5b2bb-159">ALIASES</span></span>

<span data-ttu-id="5b2bb-160">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="5b2bb-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5b2bb-161">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b2bb-162">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5b2bb-163">INPUTOBJECT: <IWindowsIotServicesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="5b2bb-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b2bb-164">`[DeviceName <String>]`: A Windows IoT-eszközszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="5b2bb-165">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5b2bb-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b2bb-166">`[ResourceGroupName <String>]`: A Windows IoT eszközszolgáltatást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="5b2bb-167">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5b2bb-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="5b2bb-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b2bb-168">RELATED LINKS</span></span>


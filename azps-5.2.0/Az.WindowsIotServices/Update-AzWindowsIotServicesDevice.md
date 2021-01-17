---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 5e50ad3dc1ce2396dfb7a2b498efc82c4e95e430
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371460"
---
# <span data-ttu-id="46964-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="46964-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="46964-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46964-102">SYNOPSIS</span></span>
<span data-ttu-id="46964-103">Frissíti egy Windows IoT-eszközszolgáltatás metaadatait.</span><span class="sxs-lookup"><span data-stu-id="46964-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="46964-104">A tulajdonság módosításának szokásos sémája az, hogy beolvassa a Windows IoT-eszközszolgáltatás metaadatait és biztonsági metaadatait, majd kombinálja őket a módosított értékekkel egy új törzsben a Windows IoT eszközszolgáltatás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="46964-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="46964-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="46964-105">SYNTAX</span></span>

### <span data-ttu-id="46964-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46964-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="46964-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="46964-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="46964-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="46964-108">DESCRIPTION</span></span>
<span data-ttu-id="46964-109">Frissíti egy Windows IoT-eszközszolgáltatás metaadatait.</span><span class="sxs-lookup"><span data-stu-id="46964-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="46964-110">A tulajdonság módosításának szokásos sémája az, hogy beolvassa a Windows IoT-eszközszolgáltatás metaadatait és biztonsági metaadatait, majd kombinálja őket a módosított értékekkel egy új törzsben a Windows IoT eszközszolgáltatás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="46964-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="46964-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="46964-111">EXAMPLES</span></span>

### <span data-ttu-id="46964-112">1. példa: Windows IoT-szolgáltatások frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="46964-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="46964-113">Ez a parancs név szerint frissíti a Windows IoT-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="46964-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="46964-114">2. példa: Windows IoT-szolgáltatások frissítése folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="46964-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="46964-115">Ez a parancs folyamat szerint frissíti a Windows IoT-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="46964-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="46964-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46964-116">PARAMETERS</span></span>

### <span data-ttu-id="46964-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="46964-117">-AdminDomainName</span></span>
<span data-ttu-id="46964-118">Windows IoT eszközszolgáltatás OEM AAD-tartomány</span><span class="sxs-lookup"><span data-stu-id="46964-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="46964-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="46964-119">-BillingDomainName</span></span>
<span data-ttu-id="46964-120">Windows IoT-eszközszolgáltatás , ODM AAD-tartomány</span><span class="sxs-lookup"><span data-stu-id="46964-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="46964-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46964-121">-DefaultProfile</span></span>
<span data-ttu-id="46964-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46964-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46964-123">-Etag</span><span class="sxs-lookup"><span data-stu-id="46964-123">-Etag</span></span>
<span data-ttu-id="46964-124">Az Etag mező nem *kötelező.*</span><span class="sxs-lookup"><span data-stu-id="46964-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="46964-125">Ha a válasz törzsében meg van biztosítanak, a normál ETag-konvenciónak megfelelő fejlécként is meg kell azt adni.</span><span class="sxs-lookup"><span data-stu-id="46964-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="46964-126">-HaMatch</span><span class="sxs-lookup"><span data-stu-id="46964-126">-IfMatch</span></span>
<span data-ttu-id="46964-127">A Windows IoT eszközszolgáltatás Etagja.</span><span class="sxs-lookup"><span data-stu-id="46964-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="46964-128">Ne adjon meg teljesen új Windows IoT-eszközszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="46964-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="46964-129">Egy meglévő Windows IoT-eszközszolgáltatás frissítéséhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="46964-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="46964-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46964-130">-InputObject</span></span>
<span data-ttu-id="46964-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="46964-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="46964-132">-Location</span><span class="sxs-lookup"><span data-stu-id="46964-132">-Location</span></span>
<span data-ttu-id="46964-133">Az azure-régió, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="46964-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="46964-134">-Name</span><span class="sxs-lookup"><span data-stu-id="46964-134">-Name</span></span>
<span data-ttu-id="46964-135">A Windows IoT-eszközszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="46964-135">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="46964-136">-Note</span><span class="sxs-lookup"><span data-stu-id="46964-136">-Note</span></span>
<span data-ttu-id="46964-137">A Windows IoT-eszközszolgáltatás megjegyzései.</span><span class="sxs-lookup"><span data-stu-id="46964-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="46964-138">-Mennyiség</span><span class="sxs-lookup"><span data-stu-id="46964-138">-Quantity</span></span>
<span data-ttu-id="46964-139">Windows IoT-eszközszolgáltatás eszközfoglalása</span><span class="sxs-lookup"><span data-stu-id="46964-139">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="46964-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46964-140">-ResourceGroupName</span></span>
<span data-ttu-id="46964-141">A Windows IoT eszközszolgáltatást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="46964-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="46964-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46964-142">-SubscriptionId</span></span>
<span data-ttu-id="46964-143">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="46964-143">The subscription identifier.</span></span>

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

### <span data-ttu-id="46964-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="46964-144">-Tag</span></span>
<span data-ttu-id="46964-145">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="46964-145">Resource tags.</span></span>

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

### <span data-ttu-id="46964-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46964-146">-Confirm</span></span>
<span data-ttu-id="46964-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="46964-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46964-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46964-148">-WhatIf</span></span>
<span data-ttu-id="46964-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="46964-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46964-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46964-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46964-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46964-151">CommonParameters</span></span>
<span data-ttu-id="46964-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46964-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46964-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46964-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46964-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46964-154">INPUTS</span></span>

### <span data-ttu-id="46964-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="46964-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="46964-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46964-156">OUTPUTS</span></span>

### <span data-ttu-id="46964-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="46964-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="46964-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="46964-158">NOTES</span></span>

<span data-ttu-id="46964-159">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="46964-159">ALIASES</span></span>

<span data-ttu-id="46964-160">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="46964-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="46964-161">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="46964-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46964-162">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="46964-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="46964-163">INPUTOBJECT: <IWindowsIotServicesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="46964-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="46964-164">`[DeviceName <String>]`: A Windows IoT-eszközszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="46964-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="46964-165">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="46964-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="46964-166">`[ResourceGroupName <String>]`: A Windows IoT eszközszolgáltatást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="46964-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="46964-167">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="46964-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="46964-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46964-168">RELATED LINKS</span></span>


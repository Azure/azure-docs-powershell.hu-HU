---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934585"
---
# <span data-ttu-id="36585-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="36585-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="36585-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36585-102">SYNOPSIS</span></span>
<span data-ttu-id="36585-103">Access-restiction szabályt ad hozzá egy Azure Web Apphoz.</span><span class="sxs-lookup"><span data-stu-id="36585-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="36585-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36585-104">SYNTAX</span></span>

### <span data-ttu-id="36585-105">IpAddressParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36585-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36585-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="36585-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36585-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="36585-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36585-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36585-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36585-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36585-109">DESCRIPTION</span></span>
<span data-ttu-id="36585-110">Az **Add-AzWebAppAccessRestrictionRule** parancsmag access-korlátozási szabályt ad az Azure Web Apphoz.</span><span class="sxs-lookup"><span data-stu-id="36585-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="36585-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36585-111">EXAMPLES</span></span>

### <span data-ttu-id="36585-112">1. példa: IpAddress Access-korlátozási szabály hozzáadása webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="36585-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="36585-113">Ez a parancs hozzáad egy 200-as prioritású hozzáférési korlátozási szabályt és ip-tartományt egy ContosoSite nevű webalkalmazáshoz, amely a Default-Web-WestUS erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="36585-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="36585-114">2. példa: Alhálózati végpont hozzáférési korlátozási szabály hozzáadása webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="36585-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="36585-115">Ez a parancs hozzáad egy 300-as prioritású hozzáférési korlátozási szabályt és a corp-vnet alhálózati appgw-alhálózatát a Default-Web-WestUS erőforráscsoporthoz tartozó ContosoSite nevű webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="36585-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="36585-116">3. példa: Szolgáltatáscímke-hozzáférési korlátozási szabály hozzáadása webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="36585-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="36585-117">Ez a parancs hozzáad egy 200-as prioritású hozzáférési korlátozási szabályt, valamint egy, az Azure Front Door IP-hatókörét képviselő szolgáltatáscímkét egy ContosoSite nevű webalkalmazáshoz, amely a Default-Web-WestUS erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="36585-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="36585-118">4. példa: Több cím elérésére vonatkozó korlátozási szabály hozzáadása webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="36585-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="36585-119">Ez a parancs hozzáad egy 200-as prioritású hozzáférési korlátozási szabályt és két IP-tartományt egy ContosoSite nevű webalkalmazáshoz, amely a Default-Web-WestUS erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="36585-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="36585-120">5. példa: Hozzáférési korlátozási szabály hozzáadása http-fejléccel webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="36585-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="36585-121">Ez a parancs hozzáad egy 400-as prioritású hozzáférési korlátozási szabályt az AzureFrontDoor.Backend szolgáltatáshoz, és további korlátozza a hozzáférést bizonyos értékek http fejlécéhez a Default-Web-WestUS erőforráscsoporthoz tartozó ContosoSite nevű webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="36585-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="36585-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36585-122">PARAMETERS</span></span>

### <span data-ttu-id="36585-123">-Művelet</span><span class="sxs-lookup"><span data-stu-id="36585-123">-Action</span></span>
<span data-ttu-id="36585-124">Szabály engedélyezése vagy elutasítása.</span><span class="sxs-lookup"><span data-stu-id="36585-124">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36585-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36585-125">-DefaultProfile</span></span>
<span data-ttu-id="36585-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36585-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36585-127">-Leírás</span><span class="sxs-lookup"><span data-stu-id="36585-127">-Description</span></span>
<span data-ttu-id="36585-128">A hozzáférés korlátozásának leírása.</span><span class="sxs-lookup"><span data-stu-id="36585-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="36585-129">-HttpHeader</span><span class="sxs-lookup"><span data-stu-id="36585-129">-HttpHeader</span></span>
<span data-ttu-id="36585-130">Http fejlécre vonatkozó korlátozások.</span><span class="sxs-lookup"><span data-stu-id="36585-130">Http header restrictions.</span></span> <span data-ttu-id="36585-131">Például: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span><span class="sxs-lookup"><span data-stu-id="36585-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

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

### <span data-ttu-id="36585-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="36585-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="36585-133">Adja meg, hogy az alhálózati szolgáltatás végpontjának regisztrációját ellenőrizni kell-e.</span><span class="sxs-lookup"><span data-stu-id="36585-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubnetNameParameterSet, SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36585-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="36585-134">-IpAddress</span></span>
<span data-ttu-id="36585-135">Ip Address v4 or v6 CIDR range.</span><span class="sxs-lookup"><span data-stu-id="36585-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="36585-136">Pl.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="36585-136">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: IpAddressParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36585-137">-Name</span><span class="sxs-lookup"><span data-stu-id="36585-137">-Name</span></span>
<span data-ttu-id="36585-138">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="36585-138">Rule Name</span></span>

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

### <span data-ttu-id="36585-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36585-139">-PassThru</span></span>
<span data-ttu-id="36585-140">Adja vissza a hozzáférési korlátozás konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="36585-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="36585-141">-Priority</span><span class="sxs-lookup"><span data-stu-id="36585-141">-Priority</span></span>
<span data-ttu-id="36585-142">Hozzáférési korlátozás prioritása.</span><span class="sxs-lookup"><span data-stu-id="36585-142">Access Restriction priority.</span></span> <span data-ttu-id="36585-143">Például: 500.</span><span class="sxs-lookup"><span data-stu-id="36585-143">E.g.: 500.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36585-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36585-144">-ResourceGroupName</span></span>
<span data-ttu-id="36585-145">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="36585-145">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36585-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="36585-146">-ServiceTag</span></span>
<span data-ttu-id="36585-147">A szolgáltatáscímke neve</span><span class="sxs-lookup"><span data-stu-id="36585-147">Name of Service Tag</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36585-148">-SlotName</span><span class="sxs-lookup"><span data-stu-id="36585-148">-SlotName</span></span>
<span data-ttu-id="36585-149">Az üzembe helyezési hely neve.</span><span class="sxs-lookup"><span data-stu-id="36585-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="36585-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="36585-150">-SubnetId</span></span>
<span data-ttu-id="36585-151">Az alhálózat Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="36585-151">ResourceId of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36585-152">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="36585-152">-SubnetName</span></span>
<span data-ttu-id="36585-153">Az alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="36585-153">Name of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36585-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="36585-154">-TargetScmSite</span></span>
<span data-ttu-id="36585-155">A szabály fő webhelyre vagy Scm-webhelyre vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="36585-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="36585-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="36585-156">-VirtualNetworkName</span></span>
<span data-ttu-id="36585-157">A virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="36585-157">Name of Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36585-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="36585-158">-WebAppName</span></span>
<span data-ttu-id="36585-159">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="36585-159">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36585-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36585-160">-Confirm</span></span>
<span data-ttu-id="36585-161">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="36585-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36585-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36585-162">-WhatIf</span></span>
<span data-ttu-id="36585-163">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="36585-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36585-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36585-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36585-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36585-165">CommonParameters</span></span>
<span data-ttu-id="36585-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36585-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36585-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36585-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36585-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36585-168">INPUTS</span></span>

### <span data-ttu-id="36585-169">System.String</span><span class="sxs-lookup"><span data-stu-id="36585-169">System.String</span></span>

## <span data-ttu-id="36585-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36585-170">OUTPUTS</span></span>

### <span data-ttu-id="36585-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="36585-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="36585-172">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36585-172">NOTES</span></span>

## <span data-ttu-id="36585-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36585-173">RELATED LINKS</span></span>

[<span data-ttu-id="36585-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="36585-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="36585-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="36585-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="36585-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="36585-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)

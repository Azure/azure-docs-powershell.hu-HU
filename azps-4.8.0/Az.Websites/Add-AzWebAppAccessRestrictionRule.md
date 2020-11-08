---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0abad2b3d38a5f614222a8eda7e3c27b9fda9556
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182455"
---
# <span data-ttu-id="0c69f-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="0c69f-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="0c69f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c69f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c69f-103">Access-restiction-szabályt ad hozzá az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="0c69f-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="0c69f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c69f-104">SYNTAX</span></span>

### <span data-ttu-id="0c69f-105">IpAddressParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c69f-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c69f-106">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c69f-106">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c69f-107">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c69f-107">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c69f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c69f-108">DESCRIPTION</span></span>
<span data-ttu-id="0c69f-109">Az **Add-AzWebAppAccessRestrictionRule** parancsmag hozzáférési korlátozási szabályt ad az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="0c69f-109">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="0c69f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0c69f-110">EXAMPLES</span></span>

### <span data-ttu-id="0c69f-111">Példa 1: IP-hozzáférés korlátozási szabályának hozzáadása egy webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="0c69f-111">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="0c69f-112">Ez a parancs egy olyan hozzáférési korlátozási szabályt ad hozzá, amelyben a 200 és az IP-címtartomány a ContosoSite nevű webalkalmazáshoz tartozik, amely az erőforráscsoport alapértelmezett – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="0c69f-112">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="0c69f-113">2. példa: alhálózati szolgáltatás végpontjának hozzáférési korlátozási szabályának hozzáadása egy webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="0c69f-113">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="0c69f-114">Ez a parancs egy Access-korlátozási szabályt ad hozzá a 300 prioritással és a Corp-vnet egy ContosoSite nevű appgw-alhálózattal egy nevű webalkalmazáshoz, amely az erőforráscsoport alapértelmezett webWestUS-tartozik.</span><span class="sxs-lookup"><span data-stu-id="0c69f-114">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0c69f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c69f-115">PARAMETERS</span></span>

### <span data-ttu-id="0c69f-116">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="0c69f-116">-Action</span></span>
<span data-ttu-id="0c69f-117">Szabály engedélyezése vagy elutasítása.</span><span class="sxs-lookup"><span data-stu-id="0c69f-117">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="0c69f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c69f-118">-DefaultProfile</span></span>
<span data-ttu-id="0c69f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c69f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c69f-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0c69f-120">-Description</span></span>
<span data-ttu-id="0c69f-121">Hozzáférés korlátozásának leírása.</span><span class="sxs-lookup"><span data-stu-id="0c69f-121">Access Restriction description.</span></span>

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

### <span data-ttu-id="0c69f-122">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c69f-122">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="0c69f-123">Adja meg, hogy a szolgáltatás végpontjának az alhálózatra való regisztrálását ellenőrizni kell-e.</span><span class="sxs-lookup"><span data-stu-id="0c69f-123">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="0c69f-124">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="0c69f-124">-IpAddress</span></span>
<span data-ttu-id="0c69f-125">IP-cím v4 vagy v6 CIDR-os tartománnyal.</span><span class="sxs-lookup"><span data-stu-id="0c69f-125">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="0c69f-126">Például: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="0c69f-126">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="0c69f-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c69f-127">-Name</span></span>
<span data-ttu-id="0c69f-128">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="0c69f-128">Rule Name</span></span>

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

### <span data-ttu-id="0c69f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c69f-129">-PassThru</span></span>
<span data-ttu-id="0c69f-130">Adja vissza a hozzáférési korlátozás config objektumát.</span><span class="sxs-lookup"><span data-stu-id="0c69f-130">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="0c69f-131">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="0c69f-131">-Priority</span></span>
<span data-ttu-id="0c69f-132">Hozzáférés korlátozásának prioritása</span><span class="sxs-lookup"><span data-stu-id="0c69f-132">Access Restriction priority.</span></span> <span data-ttu-id="0c69f-133">Például: 500.</span><span class="sxs-lookup"><span data-stu-id="0c69f-133">E.g.: 500.</span></span>

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

### <span data-ttu-id="0c69f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c69f-134">-ResourceGroupName</span></span>
<span data-ttu-id="0c69f-135">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0c69f-135">Resource Group Name</span></span>

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

### <span data-ttu-id="0c69f-136">-SlotName</span><span class="sxs-lookup"><span data-stu-id="0c69f-136">-SlotName</span></span>
<span data-ttu-id="0c69f-137">A telepítő tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="0c69f-137">Deployment Slot name.</span></span>

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

### <span data-ttu-id="0c69f-138">– NetI</span><span class="sxs-lookup"><span data-stu-id="0c69f-138">-SubnetId</span></span>
<span data-ttu-id="0c69f-139">Az alhálózat ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c69f-139">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="0c69f-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="0c69f-140">-SubnetName</span></span>
<span data-ttu-id="0c69f-141">Az alhálózat neve</span><span class="sxs-lookup"><span data-stu-id="0c69f-141">Name of Subnet.</span></span>

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

### <span data-ttu-id="0c69f-142">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="0c69f-142">-TargetScmSite</span></span>
<span data-ttu-id="0c69f-143">A szabály a fő webhelyre vagy az SCM-webhelyre irányul.</span><span class="sxs-lookup"><span data-stu-id="0c69f-143">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="0c69f-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0c69f-144">-VirtualNetworkName</span></span>
<span data-ttu-id="0c69f-145">A virtuális hálózat neve</span><span class="sxs-lookup"><span data-stu-id="0c69f-145">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="0c69f-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="0c69f-146">-WebAppName</span></span>
<span data-ttu-id="0c69f-147">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="0c69f-147">The name of the web app.</span></span>

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

### <span data-ttu-id="0c69f-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0c69f-148">-Confirm</span></span>
<span data-ttu-id="0c69f-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c69f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c69f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c69f-150">-WhatIf</span></span>
<span data-ttu-id="0c69f-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0c69f-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c69f-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c69f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c69f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c69f-153">CommonParameters</span></span>
<span data-ttu-id="0c69f-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c69f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c69f-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0c69f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c69f-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c69f-156">INPUTS</span></span>

### <span data-ttu-id="0c69f-157">System. String</span><span class="sxs-lookup"><span data-stu-id="0c69f-157">System.String</span></span>

## <span data-ttu-id="0c69f-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c69f-158">OUTPUTS</span></span>

### <span data-ttu-id="0c69f-159">Microsoft. Azure. Command. WebApps. models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="0c69f-159">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="0c69f-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c69f-160">NOTES</span></span>

## <span data-ttu-id="0c69f-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c69f-161">RELATED LINKS</span></span>

[<span data-ttu-id="0c69f-162">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="0c69f-162">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="0c69f-163">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="0c69f-163">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="0c69f-164">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="0c69f-164">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)

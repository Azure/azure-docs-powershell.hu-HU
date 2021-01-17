---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466994"
---
# <span data-ttu-id="27178-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="27178-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="27178-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27178-102">SYNOPSIS</span></span>
<span data-ttu-id="27178-103">Eltávolít egy hozzáférési korlátozási szabályt egy Azure Web Appból.</span><span class="sxs-lookup"><span data-stu-id="27178-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="27178-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="27178-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27178-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="27178-105">DESCRIPTION</span></span>
<span data-ttu-id="27178-106">A **Remove-AzWebAppAccessRestrictionRule** parancsmag eltávolítja az Access-korlátozási szabályokat az Azure Web Appból</span><span class="sxs-lookup"><span data-stu-id="27178-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="27178-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="27178-107">EXAMPLES</span></span>

### <span data-ttu-id="27178-108">1. példa: Web App-hozzáférés korlátozási szabályának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="27178-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="27178-109">Ez a parancs eltávolítja az IpRule-hozzáférés korlátozási szabályát a Default-Web-WestUS nevű erőforráscsoporthoz tartozó ContosoSite nevű Azure Web Appból.</span><span class="sxs-lookup"><span data-stu-id="27178-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="27178-110">2. példa: Szolgáltatáscímke webalkalmazás hozzáférési korlátozási szabályának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="27178-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="27178-111">Ez a parancs eltávolítja a hozzáférés-korlátozási szabályt úgy, hogy a ServiceTag egyenlő az AzureFrontDoor.Backend értékekkel a ContosoSite nevű Azure Web Appból, amely a Default-Web-WestUS nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="27178-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="27178-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27178-112">PARAMETERS</span></span>

### <span data-ttu-id="27178-113">-Művelet</span><span class="sxs-lookup"><span data-stu-id="27178-113">-Action</span></span>
<span data-ttu-id="27178-114">Szabály engedélyezése vagy elutasítása.</span><span class="sxs-lookup"><span data-stu-id="27178-114">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27178-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27178-115">-DefaultProfile</span></span>
<span data-ttu-id="27178-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27178-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27178-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="27178-117">-IpAddress</span></span>
<span data-ttu-id="27178-118">Ip Address v4 or v6 CIDR range.</span><span class="sxs-lookup"><span data-stu-id="27178-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="27178-119">Pl.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="27178-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="27178-120">-Name</span><span class="sxs-lookup"><span data-stu-id="27178-120">-Name</span></span>
<span data-ttu-id="27178-121">Hozzáférés-korlátozási szabály neve</span><span class="sxs-lookup"><span data-stu-id="27178-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="27178-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27178-122">-PassThru</span></span>
<span data-ttu-id="27178-123">Adja vissza a hozzáférési korlátozás konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="27178-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="27178-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27178-124">-ResourceGroupName</span></span>
<span data-ttu-id="27178-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="27178-125">Resource Group Name</span></span>

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

### <span data-ttu-id="27178-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="27178-126">-ServiceTag</span></span>
<span data-ttu-id="27178-127">A szolgáltatáscímke neve</span><span class="sxs-lookup"><span data-stu-id="27178-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="27178-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="27178-128">-SlotName</span></span>
<span data-ttu-id="27178-129">Deployment Slot Name (Telepítési hely neve).</span><span class="sxs-lookup"><span data-stu-id="27178-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="27178-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="27178-130">-SubnetId</span></span>
<span data-ttu-id="27178-131">Az alhálózat Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="27178-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="27178-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="27178-132">-SubnetName</span></span>
<span data-ttu-id="27178-133">Az alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="27178-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="27178-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="27178-134">-TargetScmSite</span></span>
<span data-ttu-id="27178-135">A szabály fő webhelyre vagy Scm-webhelyre vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="27178-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="27178-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="27178-136">-VirtualNetworkName</span></span>
<span data-ttu-id="27178-137">A virtuális hálózat neve (a Web Apptal azonos erőforráscsoportban kell lennie).</span><span class="sxs-lookup"><span data-stu-id="27178-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="27178-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="27178-138">-WebAppName</span></span>
<span data-ttu-id="27178-139">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="27178-139">The name of the web app.</span></span>

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

### <span data-ttu-id="27178-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27178-140">-Confirm</span></span>
<span data-ttu-id="27178-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="27178-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27178-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27178-142">-WhatIf</span></span>
<span data-ttu-id="27178-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="27178-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27178-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27178-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27178-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27178-145">CommonParameters</span></span>
<span data-ttu-id="27178-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27178-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27178-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27178-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27178-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27178-148">INPUTS</span></span>

### <span data-ttu-id="27178-149">System.String</span><span class="sxs-lookup"><span data-stu-id="27178-149">System.String</span></span>

## <span data-ttu-id="27178-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27178-150">OUTPUTS</span></span>

### <span data-ttu-id="27178-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="27178-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="27178-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="27178-152">NOTES</span></span>

## <span data-ttu-id="27178-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27178-153">RELATED LINKS</span></span>

[<span data-ttu-id="27178-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="27178-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="27178-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="27178-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="27178-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="27178-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

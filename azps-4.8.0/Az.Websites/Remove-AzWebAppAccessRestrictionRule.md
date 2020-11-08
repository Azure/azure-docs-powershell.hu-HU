---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: ad0bdc95ea3d582a2f8b6b6b1f8bc772c795352c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025023"
---
# <span data-ttu-id="a2e02-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="a2e02-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="a2e02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2e02-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e02-103">Hozzáférés-korlátozási szabály eltávolítása az Azure Web App alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="a2e02-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="a2e02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2e02-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-TargetScmSite] [-SlotName <String>] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2e02-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2e02-105">DESCRIPTION</span></span>
<span data-ttu-id="a2e02-106">A **Remove-AzWebAppAccessRestrictionRule** parancsmag eltávolítja a hozzáférési korlátozási szabályt egy Azure Web App alkalmazásból</span><span class="sxs-lookup"><span data-stu-id="a2e02-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="a2e02-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a2e02-107">EXAMPLES</span></span>

### <span data-ttu-id="a2e02-108">Példa 1: webalkalmazás-hozzáférési korlátozási szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a2e02-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="a2e02-109">Ez a parancs eltávolítja a IpRule hozzáférés korlátozási szabályát a ContosoSite nevű Azure Web App alkalmazásból, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="a2e02-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a2e02-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2e02-110">PARAMETERS</span></span>

### <span data-ttu-id="a2e02-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="a2e02-111">-Action</span></span>
<span data-ttu-id="a2e02-112">Szabály engedélyezése vagy elutasítása.</span><span class="sxs-lookup"><span data-stu-id="a2e02-112">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="a2e02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e02-113">-DefaultProfile</span></span>
<span data-ttu-id="a2e02-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2e02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2e02-115">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="a2e02-115">-IpAddress</span></span>
<span data-ttu-id="a2e02-116">IP-cím v4 vagy v6 CIDR-os tartománnyal.</span><span class="sxs-lookup"><span data-stu-id="a2e02-116">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="a2e02-117">Például: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="a2e02-117">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="a2e02-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2e02-118">-Name</span></span>
<span data-ttu-id="a2e02-119">Hozzáférés korlátozási szabály neve</span><span class="sxs-lookup"><span data-stu-id="a2e02-119">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="a2e02-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2e02-120">-PassThru</span></span>
<span data-ttu-id="a2e02-121">Adja vissza a hozzáférési korlátozás config objektumát.</span><span class="sxs-lookup"><span data-stu-id="a2e02-121">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="a2e02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2e02-122">-ResourceGroupName</span></span>
<span data-ttu-id="a2e02-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a2e02-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a2e02-124">-SlotName</span><span class="sxs-lookup"><span data-stu-id="a2e02-124">-SlotName</span></span>
<span data-ttu-id="a2e02-125">A telepítő tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="a2e02-125">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="a2e02-126">– NetI</span><span class="sxs-lookup"><span data-stu-id="a2e02-126">-SubnetId</span></span>
<span data-ttu-id="a2e02-127">Az alhálózat ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2e02-127">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="a2e02-128">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a2e02-128">-SubnetName</span></span>
<span data-ttu-id="a2e02-129">Az alhálózat neve</span><span class="sxs-lookup"><span data-stu-id="a2e02-129">Name of Subnet.</span></span>

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

### <span data-ttu-id="a2e02-130">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="a2e02-130">-TargetScmSite</span></span>
<span data-ttu-id="a2e02-131">A szabály a fő webhelyre vagy az SCM-webhelyre irányul.</span><span class="sxs-lookup"><span data-stu-id="a2e02-131">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="a2e02-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a2e02-132">-VirtualNetworkName</span></span>
<span data-ttu-id="a2e02-133">A virtuális hálózat neve (ugyanazon az erőforrás-csoportban kell lennie, mint a Web App).</span><span class="sxs-lookup"><span data-stu-id="a2e02-133">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="a2e02-134">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a2e02-134">-WebAppName</span></span>
<span data-ttu-id="a2e02-135">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="a2e02-135">The name of the web app.</span></span>

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

### <span data-ttu-id="a2e02-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2e02-136">-Confirm</span></span>
<span data-ttu-id="a2e02-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2e02-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2e02-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2e02-138">-WhatIf</span></span>
<span data-ttu-id="a2e02-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2e02-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2e02-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2e02-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2e02-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e02-141">CommonParameters</span></span>
<span data-ttu-id="a2e02-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2e02-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e02-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a2e02-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e02-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2e02-144">INPUTS</span></span>

### <span data-ttu-id="a2e02-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a2e02-145">System.String</span></span>

## <span data-ttu-id="a2e02-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2e02-146">OUTPUTS</span></span>

### <span data-ttu-id="a2e02-147">Microsoft. Azure. Command. WebApps. models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a2e02-147">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="a2e02-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2e02-148">NOTES</span></span>

## <span data-ttu-id="a2e02-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2e02-149">RELATED LINKS</span></span>

[<span data-ttu-id="a2e02-150">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a2e02-150">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="a2e02-151">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a2e02-151">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="a2e02-152">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="a2e02-152">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

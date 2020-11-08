---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: 9069dd055fd3cccdbd1efe520fc560c385d15cc3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012582"
---
# <span data-ttu-id="8c717-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8c717-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="8c717-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c717-102">SYNOPSIS</span></span>
<span data-ttu-id="8c717-103">Itt frissítheti az Azure-alapú webalkalmazások restiction-konfigurációjának az SCM-webhelyre való öröklését.</span><span class="sxs-lookup"><span data-stu-id="8c717-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="8c717-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c717-104">SYNTAX</span></span>

### <span data-ttu-id="8c717-105">InputValuesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c717-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c717-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c717-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c717-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c717-107">DESCRIPTION</span></span>
<span data-ttu-id="8c717-108">Az **Update-AzWebAppAccessRestrictionConfig** parancsmag az Azure-alapú webalkalmazások hozzáférés-korlátozási konfigurációját frissíti.</span><span class="sxs-lookup"><span data-stu-id="8c717-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="8c717-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8c717-109">EXAMPLES</span></span>

### <span data-ttu-id="8c717-110">Példa 1: Web App SCM-webhely frissítése a fő webhelyről való hozzáférési korlátozások használatához</span><span class="sxs-lookup"><span data-stu-id="8c717-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>
```
PS C:\>Set-AzWebAppAccessRestriction -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -ScmSiteUseMainSiteRestrictionConfig
```

<span data-ttu-id="8c717-111">Ez a parancs frissíti a ContosoSite nevű, az erőforráscsoport alapértelmezett verziójához tartozó webalkalmazást, amely az SCM-webhelyen található fő webhely hozzáférés-korlátozási WestUS használja.</span><span class="sxs-lookup"><span data-stu-id="8c717-111">This command updates a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS to use access restriction config of main site on the scm site.</span></span>

## <span data-ttu-id="8c717-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c717-112">PARAMETERS</span></span>

### <span data-ttu-id="8c717-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c717-113">-DefaultProfile</span></span>
<span data-ttu-id="8c717-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c717-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c717-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c717-115">-InputObject</span></span>
<span data-ttu-id="8c717-116">Az Access korlátozási konfigurációs objektuma</span><span class="sxs-lookup"><span data-stu-id="8c717-116">The access restriction config object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c717-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c717-117">-Name</span></span>
<span data-ttu-id="8c717-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="8c717-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c717-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c717-119">-PassThru</span></span>
<span data-ttu-id="8c717-120">Adja vissza a hozzáférési korlátozás config objektumát.</span><span class="sxs-lookup"><span data-stu-id="8c717-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="8c717-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c717-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c717-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="8c717-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c717-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8c717-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="8c717-124">Az SCM-webhely örökli a fő webhelyen beállított szabályokat.</span><span class="sxs-lookup"><span data-stu-id="8c717-124">Scm site inherits rules set on Main site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c717-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="8c717-125">-SlotName</span></span>
<span data-ttu-id="8c717-126">A telepítő tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="8c717-126">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c717-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8c717-127">-Confirm</span></span>
<span data-ttu-id="8c717-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c717-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c717-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c717-129">-WhatIf</span></span>
<span data-ttu-id="8c717-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8c717-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c717-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c717-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c717-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c717-132">CommonParameters</span></span>
<span data-ttu-id="8c717-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c717-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c717-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8c717-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c717-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c717-135">INPUTS</span></span>

### <span data-ttu-id="8c717-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8c717-136">System.String</span></span>

### <span data-ttu-id="8c717-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c717-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8c717-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c717-138">OUTPUTS</span></span>

### <span data-ttu-id="8c717-139">Microsoft. Azure. Command. WebApps. models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8c717-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="8c717-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c717-140">NOTES</span></span>

## <span data-ttu-id="8c717-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c717-141">RELATED LINKS</span></span>

[<span data-ttu-id="8c717-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8c717-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="8c717-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="8c717-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="8c717-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="8c717-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)

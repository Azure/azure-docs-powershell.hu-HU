---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010981"
---
# <span data-ttu-id="fb1d1-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="fb1d1-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="fb1d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="fb1d1-103">Frissíti egy Azure Web App SCM-webhelyére vonatkozó Főwebhely Hozzáférés restiction konfigját.</span><span class="sxs-lookup"><span data-stu-id="fb1d1-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="fb1d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb1d1-104">SYNTAX</span></span>

### <span data-ttu-id="fb1d1-105">InputValuesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb1d1-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb1d1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb1d1-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb1d1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb1d1-107">DESCRIPTION</span></span>
<span data-ttu-id="fb1d1-108">Az **Update-AzWebAppAccessRestrictionConfig** parancsmag frissíti az Azure Web App hozzáférési korlátozási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="fb1d1-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="fb1d1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb1d1-109">EXAMPLES</span></span>

### <span data-ttu-id="fb1d1-110">1. példa: Webalkalmazás SCM-webhelyének frissítése a főwebhely hozzáférési korlátozásait használva</span><span class="sxs-lookup"><span data-stu-id="fb1d1-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="fb1d1-111">Az alábbi példa frissíti az IpRule nevű webalkalmazást, amely a MyResourceGroup erőforráscsoporthoz tartozik, hogy az scm-webhelyen található fő webhely hozzáférési korlátozási konfigurációját használja.</span><span class="sxs-lookup"><span data-stu-id="fb1d1-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="fb1d1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb1d1-112">PARAMETERS</span></span>

### <span data-ttu-id="fb1d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb1d1-113">-DefaultProfile</span></span>
<span data-ttu-id="fb1d1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb1d1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb1d1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb1d1-115">-InputObject</span></span>
<span data-ttu-id="fb1d1-116">Hozzáférés-korlátozási konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="fb1d1-116">The access restriction config object</span></span>

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

### <span data-ttu-id="fb1d1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fb1d1-117">-Name</span></span>
<span data-ttu-id="fb1d1-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="fb1d1-118">WebApp Name</span></span>

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

### <span data-ttu-id="fb1d1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb1d1-119">-PassThru</span></span>
<span data-ttu-id="fb1d1-120">Adja vissza a hozzáférési korlátozás konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="fb1d1-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="fb1d1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb1d1-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb1d1-122">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fb1d1-122">Resource Group Name</span></span>

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

### <span data-ttu-id="fb1d1-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="fb1d1-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="fb1d1-124">Az Scm-webhely örökli a főwebhelyen beállított szabályokat.</span><span class="sxs-lookup"><span data-stu-id="fb1d1-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="fb1d1-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="fb1d1-125">-SlotName</span></span>
<span data-ttu-id="fb1d1-126">Az üzembe helyezési hely neve.</span><span class="sxs-lookup"><span data-stu-id="fb1d1-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="fb1d1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb1d1-127">-Confirm</span></span>
<span data-ttu-id="fb1d1-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fb1d1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb1d1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb1d1-129">-WhatIf</span></span>
<span data-ttu-id="fb1d1-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fb1d1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb1d1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb1d1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb1d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb1d1-132">CommonParameters</span></span>
<span data-ttu-id="fb1d1-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb1d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb1d1-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb1d1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb1d1-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb1d1-135">INPUTS</span></span>

### <span data-ttu-id="fb1d1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fb1d1-136">System.String</span></span>

### <span data-ttu-id="fb1d1-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fb1d1-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fb1d1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb1d1-138">OUTPUTS</span></span>

### <span data-ttu-id="fb1d1-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="fb1d1-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="fb1d1-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb1d1-140">NOTES</span></span>

## <span data-ttu-id="fb1d1-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb1d1-141">RELATED LINKS</span></span>

[<span data-ttu-id="fb1d1-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="fb1d1-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="fb1d1-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="fb1d1-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="fb1d1-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="fb1d1-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)

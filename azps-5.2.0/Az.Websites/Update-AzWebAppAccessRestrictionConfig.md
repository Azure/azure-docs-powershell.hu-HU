---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349326"
---
# <span data-ttu-id="bd459-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="bd459-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="bd459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd459-102">SYNOPSIS</span></span>
<span data-ttu-id="bd459-103">Frissíti egy Azure Web App SCM-webhelyére vonatkozó Főwebhely Hozzáférés restiction konfigját.</span><span class="sxs-lookup"><span data-stu-id="bd459-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="bd459-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd459-104">SYNTAX</span></span>

### <span data-ttu-id="bd459-105">InputValuesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd459-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd459-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd459-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd459-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd459-107">DESCRIPTION</span></span>
<span data-ttu-id="bd459-108">Az **Update-AzWebAppAccessRestrictionConfig** parancsmag frissíti az Azure Web App hozzáférési korlátozási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="bd459-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="bd459-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd459-109">EXAMPLES</span></span>

### <span data-ttu-id="bd459-110">1. példa: Webalkalmazás SCM-webhelyének frissítése a főwebhely hozzáférési korlátozásait használva</span><span class="sxs-lookup"><span data-stu-id="bd459-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="bd459-111">Az alábbi példa frissíti az IpRule nevű webalkalmazást, amely a MyResourceGroup erőforráscsoporthoz tartozik, hogy az scm-webhelyen található fő webhely hozzáférési korlátozási konfigurációját használja.</span><span class="sxs-lookup"><span data-stu-id="bd459-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="bd459-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd459-112">PARAMETERS</span></span>

### <span data-ttu-id="bd459-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd459-113">-DefaultProfile</span></span>
<span data-ttu-id="bd459-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd459-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd459-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd459-115">-InputObject</span></span>
<span data-ttu-id="bd459-116">Hozzáférés-korlátozási konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="bd459-116">The access restriction config object</span></span>

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

### <span data-ttu-id="bd459-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bd459-117">-Name</span></span>
<span data-ttu-id="bd459-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="bd459-118">WebApp Name</span></span>

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

### <span data-ttu-id="bd459-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd459-119">-PassThru</span></span>
<span data-ttu-id="bd459-120">Adja vissza a hozzáférési korlátozás konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="bd459-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="bd459-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd459-121">-ResourceGroupName</span></span>
<span data-ttu-id="bd459-122">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="bd459-122">Resource Group Name</span></span>

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

### <span data-ttu-id="bd459-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="bd459-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="bd459-124">Az Scm-webhely örökli a főwebhelyen beállított szabályokat.</span><span class="sxs-lookup"><span data-stu-id="bd459-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="bd459-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="bd459-125">-SlotName</span></span>
<span data-ttu-id="bd459-126">Az üzembe helyezési hely neve.</span><span class="sxs-lookup"><span data-stu-id="bd459-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="bd459-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd459-127">-Confirm</span></span>
<span data-ttu-id="bd459-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bd459-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd459-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd459-129">-WhatIf</span></span>
<span data-ttu-id="bd459-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bd459-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd459-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd459-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd459-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd459-132">CommonParameters</span></span>
<span data-ttu-id="bd459-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd459-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd459-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd459-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd459-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd459-135">INPUTS</span></span>

### <span data-ttu-id="bd459-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bd459-136">System.String</span></span>

### <span data-ttu-id="bd459-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bd459-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bd459-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd459-138">OUTPUTS</span></span>

### <span data-ttu-id="bd459-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="bd459-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="bd459-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd459-140">NOTES</span></span>

## <span data-ttu-id="bd459-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd459-141">RELATED LINKS</span></span>

[<span data-ttu-id="bd459-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="bd459-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="bd459-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="bd459-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="bd459-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="bd459-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)

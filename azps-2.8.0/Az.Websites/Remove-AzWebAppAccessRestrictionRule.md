---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0631492bf2574fed7a9bb755088d811483504763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840016"
---
# <span data-ttu-id="5433e-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="5433e-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="5433e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5433e-102">SYNOPSIS</span></span>
<span data-ttu-id="5433e-103">Hozzáférés-korlátozási szabály eltávolítása az Azure Web App alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="5433e-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="5433e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5433e-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-TargetScmSite] [-SlotName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5433e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5433e-105">DESCRIPTION</span></span>
<span data-ttu-id="5433e-106">A **Remove-AzWebAppAccessRestrictionRule** parancsmag eltávolítja a hozzáférési korlátozási szabályt egy Azure Web App alkalmazásból</span><span class="sxs-lookup"><span data-stu-id="5433e-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="5433e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5433e-107">EXAMPLES</span></span>

### <span data-ttu-id="5433e-108">Példa 1: webalkalmazás-hozzáférési korlátozási szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5433e-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="5433e-109">Ez a parancs eltávolítja a IpRule hozzáférés korlátozási szabályát a ContosoSite nevű Azure Web App alkalmazásból, amely a Default-Web-WestUS nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="5433e-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="5433e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5433e-110">PARAMETERS</span></span>

### <span data-ttu-id="5433e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5433e-111">-DefaultProfile</span></span>
<span data-ttu-id="5433e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5433e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5433e-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5433e-113">-Name</span></span>
<span data-ttu-id="5433e-114">Hozzáférés korlátozási szabály neve</span><span class="sxs-lookup"><span data-stu-id="5433e-114">Access Restriction Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5433e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5433e-115">-PassThru</span></span>
<span data-ttu-id="5433e-116">Adja vissza a hozzáférési korlátozás config objektumát.</span><span class="sxs-lookup"><span data-stu-id="5433e-116">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="5433e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5433e-117">-ResourceGroupName</span></span>
<span data-ttu-id="5433e-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5433e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="5433e-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="5433e-119">-SlotName</span></span>
<span data-ttu-id="5433e-120">A telepítő tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="5433e-120">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="5433e-121">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="5433e-121">-TargetScmSite</span></span>
<span data-ttu-id="5433e-122">A szabály a fő webhelyre vagy az SCM-webhelyre irányul.</span><span class="sxs-lookup"><span data-stu-id="5433e-122">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="5433e-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="5433e-123">-WebAppName</span></span>
<span data-ttu-id="5433e-124">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="5433e-124">The name of the web app.</span></span>

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

### <span data-ttu-id="5433e-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5433e-125">-Confirm</span></span>
<span data-ttu-id="5433e-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5433e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5433e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5433e-127">-WhatIf</span></span>
<span data-ttu-id="5433e-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5433e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5433e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5433e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5433e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5433e-130">CommonParameters</span></span>
<span data-ttu-id="5433e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5433e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5433e-132">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5433e-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5433e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5433e-133">INPUTS</span></span>

### <span data-ttu-id="5433e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5433e-134">System.String</span></span>

## <span data-ttu-id="5433e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5433e-135">OUTPUTS</span></span>

### <span data-ttu-id="5433e-136">Microsoft. Azure. Command. WebApps. models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="5433e-136">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="5433e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5433e-137">NOTES</span></span>

## <span data-ttu-id="5433e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5433e-138">RELATED LINKS</span></span>

[<span data-ttu-id="5433e-139">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="5433e-139">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="5433e-140">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="5433e-140">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="5433e-141">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="5433e-141">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

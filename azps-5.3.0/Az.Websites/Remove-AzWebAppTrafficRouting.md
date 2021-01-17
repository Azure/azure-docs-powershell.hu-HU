---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466981"
---
# <span data-ttu-id="b3a9b-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b3a9b-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="b3a9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a9b-103">Útválasztási szabály eltávolítása a tárolóhelyről.</span><span class="sxs-lookup"><span data-stu-id="b3a9b-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="b3a9b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3a9b-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3a9b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3a9b-105">DESCRIPTION</span></span>
<span data-ttu-id="b3a9b-106">A **Remove-AzWebAppTrafficRouting** parancsmag eltávolít egy útválasztási szabályt az Azure Web App Slotból.</span><span class="sxs-lookup"><span data-stu-id="b3a9b-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="b3a9b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3a9b-107">EXAMPLES</span></span>

### <span data-ttu-id="b3a9b-108">1. példa: Az adott útválasztási szabály eltávolítása a webapphelyről</span><span class="sxs-lookup"><span data-stu-id="b3a9b-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="b3a9b-109">Ez a parancs eltávolítja egy adott webapphely útválasztási szabályát.</span><span class="sxs-lookup"><span data-stu-id="b3a9b-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="b3a9b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3a9b-110">PARAMETERS</span></span>

### <span data-ttu-id="b3a9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a9b-111">-DefaultProfile</span></span>
<span data-ttu-id="b3a9b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3a9b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a9b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a9b-113">-ResourceGroupName</span></span>
<span data-ttu-id="b3a9b-114">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b3a9b-114">Resource Group Name</span></span>

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

### <span data-ttu-id="b3a9b-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="b3a9b-115">-RuleName</span></span>
<span data-ttu-id="b3a9b-116">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="b3a9b-116">Rule Name</span></span>

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

### <span data-ttu-id="b3a9b-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="b3a9b-117">-WebAppName</span></span>
<span data-ttu-id="b3a9b-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="b3a9b-118">WebApp Name</span></span>

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

### <span data-ttu-id="b3a9b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3a9b-119">-PassThru</span></span>
<span data-ttu-id="b3a9b-120">Adja vissza a hozzáférési korlátozás konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="b3a9b-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="b3a9b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3a9b-121">-Confirm</span></span>
<span data-ttu-id="b3a9b-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b3a9b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3a9b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a9b-123">-WhatIf</span></span>
<span data-ttu-id="b3a9b-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b3a9b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3a9b-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3a9b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3a9b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a9b-126">CommonParameters</span></span>
<span data-ttu-id="b3a9b-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a9b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a9b-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3a9b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a9b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3a9b-129">INPUTS</span></span>

### <span data-ttu-id="b3a9b-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="b3a9b-130">None</span></span>

## <span data-ttu-id="b3a9b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3a9b-131">OUTPUTS</span></span>

### <span data-ttu-id="b3a9b-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="b3a9b-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="b3a9b-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3a9b-133">NOTES</span></span>

## <span data-ttu-id="b3a9b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3a9b-134">RELATED LINKS</span></span>
[<span data-ttu-id="b3a9b-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b3a9b-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b3a9b-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b3a9b-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b3a9b-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b3a9b-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194958"
---
# <span data-ttu-id="48c3e-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="48c3e-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="48c3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="48c3e-103">Útválasztási szabály eltávolítása a bővítőhelyről</span><span class="sxs-lookup"><span data-stu-id="48c3e-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="48c3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48c3e-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48c3e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48c3e-105">DESCRIPTION</span></span>
<span data-ttu-id="48c3e-106">A **Remove-AzWebAppTrafficRouting** parancsmag az Azure Web App-bővítőhelyről eltávolítja az útválasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="48c3e-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="48c3e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48c3e-107">EXAMPLES</span></span>

### <span data-ttu-id="48c3e-108">Példa 1 az adott útválasztási szabály eltávolítása a WebApp bővítőhelyről</span><span class="sxs-lookup"><span data-stu-id="48c3e-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="48c3e-109">Ez a parancs eltávolítja az adott WebApp-bővítőhelyhez tartozó útválasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="48c3e-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="48c3e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48c3e-110">PARAMETERS</span></span>

### <span data-ttu-id="48c3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c3e-111">-DefaultProfile</span></span>
<span data-ttu-id="48c3e-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48c3e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48c3e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48c3e-113">-ResourceGroupName</span></span>
<span data-ttu-id="48c3e-114">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="48c3e-114">Resource Group Name</span></span>

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

### <span data-ttu-id="48c3e-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="48c3e-115">-RuleName</span></span>
<span data-ttu-id="48c3e-116">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="48c3e-116">Rule Name</span></span>

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

### <span data-ttu-id="48c3e-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="48c3e-117">-WebAppName</span></span>
<span data-ttu-id="48c3e-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="48c3e-118">WebApp Name</span></span>

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

### <span data-ttu-id="48c3e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48c3e-119">-PassThru</span></span>
<span data-ttu-id="48c3e-120">Adja vissza a hozzáférési korlátozás config objektumát.</span><span class="sxs-lookup"><span data-stu-id="48c3e-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="48c3e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48c3e-121">-Confirm</span></span>
<span data-ttu-id="48c3e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48c3e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48c3e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48c3e-123">-WhatIf</span></span>
<span data-ttu-id="48c3e-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48c3e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48c3e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48c3e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48c3e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c3e-126">CommonParameters</span></span>
<span data-ttu-id="48c3e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48c3e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c3e-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="48c3e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c3e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48c3e-129">INPUTS</span></span>

### <span data-ttu-id="48c3e-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="48c3e-130">None</span></span>

## <span data-ttu-id="48c3e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48c3e-131">OUTPUTS</span></span>

### <span data-ttu-id="48c3e-132">Microsoft. Azure. Management. WebSites. models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="48c3e-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="48c3e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48c3e-133">NOTES</span></span>

## <span data-ttu-id="48c3e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48c3e-134">RELATED LINKS</span></span>
[<span data-ttu-id="48c3e-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="48c3e-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="48c3e-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="48c3e-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="48c3e-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="48c3e-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)
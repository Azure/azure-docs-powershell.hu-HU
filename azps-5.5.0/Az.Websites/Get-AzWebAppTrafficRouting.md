---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165434"
---
# <span data-ttu-id="03ba1-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="03ba1-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="03ba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="03ba1-103">Routing Rule for the given Slot name.Get a routing Rule for the given Slot name.</span><span class="sxs-lookup"><span data-stu-id="03ba1-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="03ba1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03ba1-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03ba1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03ba1-105">DESCRIPTION</span></span>
<span data-ttu-id="03ba1-106">A **Get-AzWebAppTrafficRouting** parancsmag útválasztási szabálykonfigurációt kap egy Azure Web App Slotból.</span><span class="sxs-lookup"><span data-stu-id="03ba1-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="03ba1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03ba1-107">EXAMPLES</span></span>

### <span data-ttu-id="03ba1-108">1. példa: Az adott útválasztási szabály beolvasója webapphelyről</span><span class="sxs-lookup"><span data-stu-id="03ba1-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="03ba1-109">Ez a parancs útválasztási szabályt kap egy adott webapphelyhez.</span><span class="sxs-lookup"><span data-stu-id="03ba1-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="03ba1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03ba1-110">PARAMETERS</span></span>

### <span data-ttu-id="03ba1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ba1-111">-DefaultProfile</span></span>
<span data-ttu-id="03ba1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03ba1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03ba1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ba1-113">-ResourceGroupName</span></span>
<span data-ttu-id="03ba1-114">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="03ba1-114">Resource Group Name</span></span>

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

### <span data-ttu-id="03ba1-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="03ba1-115">-RuleName</span></span>
<span data-ttu-id="03ba1-116">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="03ba1-116">Rule Name</span></span>
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

### <span data-ttu-id="03ba1-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="03ba1-117">-WebAppName</span></span>
<span data-ttu-id="03ba1-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="03ba1-118">WebApp Name</span></span>

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

### <span data-ttu-id="03ba1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ba1-119">CommonParameters</span></span>
<span data-ttu-id="03ba1-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ba1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ba1-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03ba1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ba1-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03ba1-122">INPUTS</span></span>

### <span data-ttu-id="03ba1-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="03ba1-123">None</span></span>

## <span data-ttu-id="03ba1-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03ba1-124">OUTPUTS</span></span>

### <span data-ttu-id="03ba1-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="03ba1-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="03ba1-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03ba1-126">NOTES</span></span>

## <span data-ttu-id="03ba1-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03ba1-127">RELATED LINKS</span></span>

[<span data-ttu-id="03ba1-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="03ba1-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="03ba1-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="03ba1-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="03ba1-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="03ba1-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
